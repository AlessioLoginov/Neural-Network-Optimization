# Neural-Network-Optimization

## 📚 Описание проекта
**Neural-Network-Optimization** — это проект, направленный на создание и оптимизацию сверточной нейронной сети для задачи классификации изображений из набора данных **CIFAR-10**. 

Проект включает:
- **Разработку архитектуры** глубоких нейронных сетей с использованием нескольких сверточных слоев.
- **Оптимизацию гиперпараметров**, таких как learning rate, количество фильтров, размер ядра и Dropout.
- **Применение аугментации данных** для улучшения обобщающей способности модели.
- **Использование современных методов обучения**, включая раннюю остановку и сохранение лучших моделей.
- **Детальный анализ результатов** с визуализацией обучения и проверки.

Итоговая модель достигла **точности 80.76%** на тестовых данных CIFAR-10.

---

## 📂 Структура проекта

Проект состоит из следующих файлов:
- **`Neural_Network_Optimization.ipynb`** — основной Jupyter Notebook, включающий:
  - Загрузку и предобработку данных CIFAR-10.
  - Применение аугментации изображений (повороты, сдвиги, отражения).
  - Построение и обучение сверточной нейронной сети.
  - Визуализацию процесса обучения и проверку точности модели.
  - Финальные результаты с сохранением лучшей модели в формате `.keras`.

- **`README.md`** — описание проекта, его целей и результатов.

---

## 🚀 Основные этапы работы

### 1. Предобработка данных
- Загрузка набора данных CIFAR-10.
- Нормализация изображений и преобразование меток в формат one-hot encoding.

### 2. Аугментация данных
Используются различные методы для увеличения объема данных и улучшения обобщающей способности модели:
- Поворот изображений (rotation).
- Сдвиг по ширине и высоте (width/height shift).
- Горизонтальное отражение (horizontal flip).

### 3. Архитектура модели
Модель состоит из:
1. Трех блоков **сверточных слоев** с увеличением количества фильтров:
   - 128, 256, 512 фильтров с ядром 3x3.
2. **MaxPooling2D** для уменьшения пространственных размеров.
3. **Dropout** для предотвращения переобучения.
4. Полносвязных слоев:
   - 512, 256, 128 нейронов.
5. Выходного слоя с 10 классами (softmax).

**Ключевые особенности:**
- Оптимизация с использованием Adam с learning rate = 0.0003.
- Использование `Dropout` с коэффициентом 0.5 для борьбы с переобучением.
- Применение `BatchNormalization` для ускорения обучения.

### 4. Методы обучения
- **Ранняя остановка (EarlyStopping)**: обучение завершается, если валидационная точность не улучшается в течение 10 эпох.
- **Сохранение лучшей модели (ModelCheckpoint)**: сохраняется только модель с максимальной точностью на валидационном наборе.

---

## 📈 Результаты

Итоговая модель показала следующие метрики:
- **Точность на тестовых данных**: 80.76%.
- **Значительные улучшения** достигнуты благодаря:
  - Глубокой архитектуре модели.
  - Эффективной аугментации данных.
  - Тщательной настройке гиперпараметров.

---

## 💻 Установка

### 1. Установка зависимостей
Убедитесь, что установлены следующие библиотеки:
- Python 3.x
- TensorFlow
- Keras
- NumPy
- Matplotlib
- scikit-learn

Установить зависимости можно командой:
```bash
pip install tensorflow keras numpy matplotlib scikit-learn 



📊 Используемые технологии

TensorFlow/Keras: Построение и обучение модели.
Python: Основной язык программирования.
Matplotlib: Визуализация обучения и результатов.
scikit-learn: Оценка точности модели.




