Ниже представлен код для создания виртуального окружения и установки необходимых зависимостей. Код для MacOS, если будешь открывать на Win - нужно будет чуть изменить написание.
  
<details><summary><b>Версия Python</b></summary>   
Python 3.12.3  
  
</details>   
  
<details><summary><b>Создание и активация виртуального окружения</b></summary>  
  
`python3 -m venv cv_env`  
`source cv_env/bin/activate`  
  
</details> 

<details><summary><b>Добавление нового ядра для окружения и установка библиотек</b></summary> 

`pip3 install jupyter`  
`pip3 install ipykernel`  
`python3 -m ipykernel install --user --name=cv_env --display-name "Python 3.12 (cv_env)"`   
  
После этой команды виртуальное окружение cv_env будет доступно в Jupyter Notebook и мы можем выбрать его при создании или открытии ноутбука  

</details> 

<details><summary><b>Установка зависимостей в созданное виртуальное окружение</b></summary> 
  
`pip3 install -r requirements.txt`  
  
</details>

<details><summary><b>FAQ</b></summary>  
     
В самом начале у меня есть папка datasets с папками `test`, `train` и `val`, причем содержание `train` и `val` - одинаковое.
  
В `datasets/test` - только картинки (без подпапок)
  
В `datasets/train` (и аналогично `datasets/val`) - подпапки `images` (с фотографиями в формате .jpg) и `labels` (с labels в формате .txt). В текстовых файлах формат аннотаций YOLO (разметка прямоугольником MakeSense): `<object-class> <x_center> <y_center> <width> <height>`  
  
**ВАЖНО:**  наличие любых других папок в datasets сломает код!
  
</details> 
