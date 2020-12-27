# Модель ПО для поликлиник

-------
### Оглавление
1. [Старт](#Link0)
2. [Главное окно](#Link1)
3. [Окно регистрации](#Link2)
4. [Окно входа для пациента/врача](#Link3)
5. [Личный кабинет врача](#Link4)
6. [Личный кабинет пациента](#Link5)
7. [О разработчиках](#Link6)
-------

### <a name="Link0"></a> Старт
Для работы с приложением необходимо установить [Python 3](https://www.python.org/downloads/release/python-360/). После установки необходимо дополнительно установить модуль PyQt5 при помощи команды в консоли
> pip install pyqt5


Теперь можно работать с приложением. Для этого запустите файл [project.py](https://github.com/platon-p/polyclinic/blob/main/project.py)
##### Данные для входа врачей:
> bibbob:12345678
> 
> petrov-nevrolog:987654

##### Данные для входа пациентов:
> hotabuchic:qazwsX2005
> 
> Test:Test12345

Полный список данных для входа расположен в файле project.db (таблицы auth_patients и auth_doctors)

-----

### <a name="Link1"></a> Главное окно
Главное окно имеет следующий вид. 
Главное окно содержит кнопки “Зарегистрироваться”, “Войти как пациент”, “Войти как врач”, которые предназначены для определения дальнейших действий
> <img src="https://i.ibb.co/1fv493h/2020-12-27-17-31-18.png" alt="2020-12-27-17-31-18" border="0" style="width: 30%;">

### <a name="Link2"></a> 2. Окно регистрации
Окно регистрации содержит поля для ввода Фамилии, Имени, Отчества, Номера телефона, Адреса, Даты рождения, Логина, Пароля, а также выбора Пола.

Поле “номер телефона” проверяется на правильность, а “пароль” - на безопасность.Если пользователь с указанным логином уже существует, то необходимо придумать другой. Если все введено корректно, то осуществляется регистрация пациента
> <img src="https://i.ibb.co/RT3J12n/unnamed-2.png" alt="unnamed-2" border="0" style="width: 20%;">

### <a name="Link3"></a>3. Окно входа для пациента/врача
В этом окне присутствуют поля для ввода логина и пароля, при чем пароль отображает вводимые символы как точки (в целях безопасности). Если введенные данные корректны и пользователь с такими данными существует, то осуществляется вход.
> <img src="https://i.ibb.co/CBWTW06/2020-12-27-17-56-01.png" alt="2020-12-27-17-56-01" border="0" style="width: 30%">

### <a name="Link4"></a> 4. Личный кабинет врача 
В личном кабинете врача расположены таблица. В этой таблице находятся записи на следующие 2 недели. При этом у каждого врача таблица уникальна, так как при ее заполнении учитывается продолжительность приема и расписание для каждого дня недели. Ячейки, соответствующие времени, когда врач не работает, имеют белый цвет, если же работает - серым, а если в это время назначен прием - желтым.

> <img src="https://i.ibb.co/qdCf5vH/2020-12-27-18-01-26.png" alt="2020-12-27-18-01-26" border="0">

При нажатии на ячейку с записью, всплывает окно, в котором показана информация об этой записи
> <img src="https://i.ibb.co/WBXpLwq/2020-12-27-18-03-48.png" alt="2020-12-27-18-03-48" border="0" style="width: 30%;">

Если нажать дважды по времени, в которое доктор работает и свободен, открывается окно для создания записи. При этом запись создается только в случае нажатия на кнопку. Если окно будет закрыто, запись не создается.
> <img src="https://i.ibb.co/qN1by9W/2020-12-27-18-05-29.png" alt="2020-12-27-18-05-29" border="0" style="width: 30%">


### <a name="Link5"></a> 5. Личный кабинет пациента
После входа открывается окно выбора дальнейшего действия:
> <img src="https://i.ibb.co/4tZBKr8/2020-12-27-19-12-29.png" alt="2020-12-27-19-12-29" border="0" style="width: 30%;">

При нажатии на кнопку “Просмотр моих записей" открывается окно следующего вида, в котором содержится информация о всех предстоящих записях:
> <img src="https://i.ibb.co/zhqCfHL/2020-12-27-19-14-08.png" alt="2020-12-27-19-14-08" border="0" style="width: 30%;">

Если же нажать на “Записаться”, открывается окно для выбора специальности нужного врача:
> <img src="https://downloader.disk.yandex.ru/preview/fa9b559c789f44346e77ea16d3cac7c8c0ac0240d923f3ebc308e45d46cc80ad/5fe8ddbe/RWDL8ngwSlmZFMSjM3iN1nnrVL_sZLfJkVHSoG2-i8-JSF4Lohj83yWnLaGsR5sa9rUu11hWGsmlTSAnccOShg%3D%3D?uid=0&filename=2020-12-27_19-15-47.png&disposition=inline&hash=&limit=0&content_type=image%2Fpng&owner_uid=0&tknv=v2&size=2048x2048" style="width: 70%;">

После выбора специальность можно выбрать к какому конкретно врачу необходимо записаться:

> <img src="https://downloader.disk.yandex.ru/preview/59e974625c07fab804f4943be0f52085bc483b2964486a5fec33663442a0c3b6/5fe8df4a/pwWjgsMEziKpb8qMnwwKwFQJYYESy7MBJRBS8dhHGws-H5Tb1DpuErA77bMo3w4qNx9CVLYXe0-cPd-My_o2PQ%3D%3D?uid=0&filename=2020-12-27_19-19-26.png&disposition=inline&hash=&limit=0&content_type=image%2Fpng&owner_uid=0&tknv=v2&size=2048x2048" style="width: 70%;">

Затем открывается окно с расписанием этого врача
> <img src="https://downloader.disk.yandex.ru/preview/b37085c94b992270da745c485520e08ddeb5d3a815ab30c3438327b1b6cd32b3/5fe8e045/hXk3TVwmFEIXrD5gd83OduCGQarF3p3jYAtfJ3TLdrOcy5VhEGxpSSF-G8zG0DKh-GLGebQVGwP5HDO72_bEOA%3D%3D?uid=0&filename=2020-12-27_19-26-14.png&disposition=inline&hash=&limit=0&content_type=image%2Fpng&owner_uid=0&tknv=v2&size=2048x2048">

Желтым подсвечиваются свои записи, темным - время, которое уже занято. При двойном клике по свободному времени открывается окно для создания записи

> <img src="https://downloader.disk.yandex.ru/preview/ac24020240e9b1408aca32c2ba49f9932c234779408050bffa55dd472960aa06/5fe8e090/fgPoyeY56nnwCEVCMVtb1UAH8t26FFEOH9ICj809lRRFyDTM4lnPOt215u-WpHABvZ1bp8DstgLRfIzLVGsxoA%3D%3D?uid=0&filename=2020-12-27_19-29-01.png&disposition=inline&hash=&limit=0&content_type=image%2Fpng&owner_uid=0&tknv=v2&size=2048x2048">

-------

##### <a name="Link6"></a> 7. О разработчиках
Проект разработали:

[Багров Владимир](https://github.com/Hotabuchic) и
[Печенев Платон](https://github.com/platon-p)
