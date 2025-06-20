# Image Processing Application

## Описание задачи

Данное приложение предназначено для обработки изображений с использованием библиотек Qt и OpenCV. Оно предоставляет функциональность для загрузки изображений, применения морфологической обработки и сглаживания (низкочастотного фильтра). Приложение использует графический интерфейс Qt для взаимодействия с пользователем и OpenCV для обработки изображений.

### Основные функции приложения:

1. **Загрузка изображения** – позволяет пользователю выбрать изображение с диска и отобразить его в приложении.
2. **Морфологическая обработка** – применяет операцию расширения (dilation) с помощью структурирующего элемента прямоугольной формы к изображению.
3. **Сглаживание изображения** – применяет низкочастотный фильтр (Gaussian Blur) для размытия изображения.

---

## Установка

### Требования:
- **Qt**: Минимальная версия 5.x.
- **OpenCV**: Минимальная версия 4.x.
  
### Шаги по установке:

1. **Склонировать репозиторий**:
    ```bash
    git clone <URL репозитория>
    ```
   
2. **Открыть проект в Qt Creator**:
    - Откройте файл `.pro` проекта в Qt Creator.
    - Убедитесь, что OpenCV правильно подключен в проект.

3. **Установить зависимости**:
    - Для работы с OpenCV убедитесь, что установлены все необходимые библиотеки:
    ```bash
    sudo apt-get install libopencv-dev
    ```

4. **Собрать и запустить проект**:
    - Соберите проект через Qt Creator и запустите.

---

## Использование

### Основной интерфейс:
- **Загрузка изображения**: Нажмите кнопку "Загрузить изображение" и выберите файл с изображением.
- **Морфологическая обработка**: После загрузки изображения нажмите кнопку "Применить морфологическую обработку" для применения расширения.
- **Сглаживание изображения**: Нажмите кнопку "Применить фильтр сглаживания" для применения размытия изображения с помощью GaussianBlur.

### Шаги использования:
1. Запустите приложение.
2. Нажмите "Загрузить изображение" и выберите изображение для загрузки.
3. Нажмите "Применить морфологическую обработку" для применения расширения к изображению.
4. Нажмите "Применить фильтр сглаживания" для размытия изображения.

---

## Функции

### Основные функции программы:

1. **loadImage()**:
    - Открывает диалоговое окно для выбора изображения и загружает его в приложение.
    - Использует `QFileDialog` для выбора файла.
   
2. **applyMorphologicalProcessing()**:
    - Применяет морфологическую обработку к изображению с помощью функции `cv::morphologyEx` из OpenCV. Используется операция расширения (dilation).

3. **applySmoothingFilter()**:
    - Применяет фильтр сглаживания с использованием `cv::GaussianBlur` из OpenCV.

4. **QImageToMat(const QImage &image)**:
    - Преобразует объект `QImage` в объект `cv::Mat` для дальнейшей обработки с использованием OpenCV.

5. **MatToQImage(const cv::Mat &mat)**:
    - Преобразует объект `cv::Mat` обратно в `QImage` для отображения в интерфейсе пользователя.

---

## Пример использования

1. Загрузите изображение с вашего устройства.
2. Примените морфологическую обработку, чтобы усилить определенные детали.
3. Примените сглаживание, чтобы уменьшить шумы или размытие на изображении.
4. Отобразите результат после каждой операции.

---

## Зависимости

- **Qt 5.x и выше**: Для создания графического интерфейса и взаимодействия с пользователем.
- **OpenCV 4.x и выше**: Для обработки изображений с помощью различных фильтров и операций.

---

