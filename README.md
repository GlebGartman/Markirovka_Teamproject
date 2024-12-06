Версия Python:
Python 3.12.3


Создание и активация виртуального окружения:
python3 -m venv cv_env
source cv_env/bin/activate

Добавление нового ядра для окружения и установка библиотек:
pip3 install jupyter
pip3 install ipykernel
python3 -m ipykernel install --user --name=cv_env --display-name "Python 3.12 (cv_env)"

Установка зависимостей в созданное виртуальное окружение:
pip3 install -r requirements.txt

FAQ:
В самом начале у меня есть папка datasets с папками test, train и val, причем содержание train и val - одинаковое.

В datasets/test - только картинки (без подпапок)

В datasets/train (и аналогично datasets/val) - подпапки images (с фотографиями в формате .jpg) и labels (с labels в формате .txt). В текстовых файлах формат аннотаций YOLO (разметка прямоугольником MakeSense): <object-class> <x_center> <y_center> <width> <height>

ВАЖНО: наличие любых других папок в datasets сломает код!
