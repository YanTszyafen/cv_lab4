# Улучшение яркости изображения
## Описание задачи
* Задача - улучшение яркости изображения
* Язык программирования Python
* Ограничений по использованию библиотек и сторонних функций нет

## Датасет
Набор данных содержит содержит 745 примеров тёмных картинок. В каталоге low хранятся тёмные изображения, в каталоге high - соответсвующие им яркие изображения. Пример загрузки датасета в PyTorch приведён в файле dataset.py       
[Ссылка на датасет](https://drive.google.com/file/d/1ThoPb1flnfXDpRIytgBd7_e9Kv_lPnbo/view) 

## Метрики
Пример расчёта метрик представлен в файле evaluation.py. Для оценки качества используются следующие метрики:
* [PSNR](https://ru.wikipedia.org/wiki/Пиковое_отношение_сигнала_к_шуму) - Пиковое отношение сигнала к шуму;
* [SSIM](https://ru.wikipedia.org/wiki/SSIM) - Индекс структурного сходства;
* [LPIPS](https://github.com/richzhang/PerceptualSimilarity#c-about-the-metric) - Learned Perceptual Image Patch Similarity.  

## Результаты
* Архитектура - **SurroundNet** ["SurroundNet: Towards effective low-light image enhancement"](https://linkinghub.elsevier.com/retrieve/pii/S0031320323003035)
* Оптимизатор - Adam, 50 эпох, batch size = 4, learning rate = 1e-5. 
* На обработку одного изображения у нашего решения уходит 0.11 (мс).
|PSNR|SSIM|LPIPS|
:---:|:---:|:---:
6.10|0.036|0.78
