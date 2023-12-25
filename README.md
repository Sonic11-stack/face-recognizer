# face-recognizer
Face Recognition
Данная программа с помощью обучения модели может распознавать знаменитость на фото. 

Чтобы ее запустить, необходимо выполнить следующие шаги: 


                                                          Запуск программы без интерфейса
1)	Скачать zip файл базы данных, которая была взята из kaggle (переименуйте её в archive_1.zip)
Ссылка на базу данных (https://www.kaggle.com/datasets/hereisburak/pins-face-recognition
)

2)	Также скачать файл model_weights.h5(это сохраненная модель обучения)


3)	Скачать фото 32.jpg(он нужен для обработки с моделью)

4)	Открыть гугл диск

5)	Открыть папку Collab Notebooks

6)	Установить внутри папки скачанные файлы


7)	Запустить файл Face_Recognition.ipynb

8)	Подключить первый блок кода (
from google.colab import drive
drive.mount('/content/drive')) – Это нужно для подключения гугл диска с файлами, которые были установлены в нём

9)	Теперь необходимо запускать каждый блок кода по порядку

10)	Когда дойдете этого блока: 
(from tensorflow.keras.callbacks import ModelCheckpoint

checkpoint_callback = ModelCheckpoint("model_weights.h5",
                                      monitor='val_loss',
                                      save_best_only=True,
                                      mode='min',
                                      verbose=1)

result=model.fit(train_generator,
                 validation_data=test_generator,
                 epochs=50,
                 callbacks=[checkpoint_callback],
                 verbose=1) 

Его можно пропустить(т.к. здесь происходит обучение и сохранение модели, а у нас уже есть файл с обученной моделью). Если захотите запустить, то модель будет с нуля обучаться в течение нескольких часов.

11)	Запустить последний блок кода(в качестве примера здесь вставлена работа с изображением из гугл диска, а также здесь будет загружаться готовая модель). В конце программы будет выводиться результат с именем и фамилией знаменитости.




 
                                                       Запуск программы с интерфейсом
1)	Выполнить первые восемь пунктов из предыдущего раздела
2)	Запустить все блоки кода по порядку
3)	Когда дойдете до блока get_link(), его необходимо запустить два раза, чтобы получить ссылку на интерфейс
4)	Запустить последний блок кода и перейти по ссылке, которую получили от блока get_link()















