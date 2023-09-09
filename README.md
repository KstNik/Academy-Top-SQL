# Academy-Top-SQL

#### Экзаменационные работы

## ExaminationWork 01

Создать базу данных Книжный магазин (BookShop), описание структуры таблиц.  
1. Авторы (Authors)    
• Идентификатор (Id). Уникальный идентификатор автора: тип данных – int, авто приращение, не может содержать null­значения, первичный ключ.    
• Имя (Name). Имя автора: тип данных – nvarchar(max), не может содержать null­значения, не может быть пустым.    
• Фамилия (Surname). Фамилия автора: тип данных – nvarchar(max), не может содержать null­значения, не может быть пустым.    
• Идентификатор страны (CountryId). Страна, из которой родом автор: тип данных – int, не может содержать null­значения, внешний ключ.    
2. Книги (Books)    
• Идентификатор (Id). Уникальный идентификатор книги: тип данных – int, авто приращение, не может содержать null­значения, первичный ключ.    
• Название (Name). Название книги: тип данных – nvarchar(max), не может содержать null­значения, не может быть пустым.    
• Страницы (Pages). Количество страниц в книге: тип данных – int, не может содержать null­значения, не может быть меньше либо равно 0.    
• Цена (Price). Цена книги: тип данных – money, не может содержать null­значения, не может быть меньше 0.    
• Дата публикации (PublishDate). Дата публикации книги: тип данных – date, не может содержать null­значения, не может быть больше текущей даты.    
• Идентификатор автора (AuthorId). Автор книги: тип данных – int, не может содержать null­значения, внешний ключ.    
• Идентификатор тематики (ThemeId). Тематика книги: тип данных – int, не может содержать null­значения, внешний ключ.    
3. Страны (Countries)    
• Идентификатор (Id). Уникальный идентификатор страны: тип данных – int, авто приращение, не может содержать null­значения, первичный ключ.    
• Название (Name). Название страны: тип данных – nvarchar(50), не может содержать null­значения, не может быть пустым, должно быть уникальным.    
4. Продажи (Sales)    
• Идентификатор (Id). Уникальный идентификатор продажи: тип данных – int, авто приращение, не может содержать null­значения, первичный ключ.    
• Цена (Price). Цена продажи одного экземпляра книги: тип данных – money, не может содержать null­значения, не может быть меньше 0.    
• Количество (Quantity). Количество проданных экземпляров книги: тип данных – int, не может содержать null­значения, не может быть меньше либо равно 0.    
• Дата продажи (SaleDate). Дата продажи: тип данных – date, не может содержать null­значения, не может быть больше текущей даты, значение по умолчанию – текущая дата.    
• Идентификатор книги (BookId). Проданная книга: тип данных – int, не может содержать null­значения, внешний ключ.    
• Идентификатор магазина (ShopId). Магазин, в котором была совершена продажа: тип данных – int, не может содержать null­значения, внешний ключ.    
5. Магазины (Shops)    
• Идентификатор (Id). Уникальный идентификатор магазина: тип данных – int, авто приращение, не может содержать null­значения, первичный ключ.    
• Название (Name). Название магазина: тип данных – nvarchar(max), не может содержать null­значения, не может быть пустым.    
• Идентификатор страны (CountryId). Страна, в которой находится магазин: тип данных – int, не может содержать null­значения, внешний ключ.    
6. Тематики (Themes)    
• Идентификатор (Id). Уникальный идентификатор тематики: тип данных – int, авто приращение, не может содержать null­значения, первичный ключ.    
• Название (Name). Название тематики: тип данных – nvarchar(100), не может содержать null­значения, не может быть пустым, должно быть уникальным.

Необходимо написать следующие запросы к базе данных «Книжный магазин»:    
1. Показать все книги, количество страниц в которых больше 500, но меньше 650.    
2. Показать все книги, в которых первая буква названия либо «А», либо «З».    
3. Показать все книги жанра «Детектив», количество проданных книг более 30 экземпляров.    
4. Показать все книги, в названии которых есть слово «Microsoft», но нет слова «Windows».    
5. Показать все книги (название, тематика, полное имя автора в одной ячейке), цена одной страницы которых меньше 65 копеек.    
6. Показать все книги, название которых состоит из 4 слов.    
7. Показать информацию о продажах в следующем виде:    
• Название книги, но, чтобы оно не содержало букву «А».    
• Тематика, но, чтобы не «Программирование».    
• Автор, но, чтобы не «Герберт Шилдт».    
• Цена, но, чтобы в диапазоне от 10 до 20 гривен.    
• Количество продаж, но не менее 8 книг.    
• Название магазина, который продал книгу, но он не должен быть в Украине или России.    
8. Показать следующую информацию в два столбца (числа в правом столбце приведены в качестве примера):    
• Количество авторов: 14    
• Количество книг: 47    
• Средняя цена продажи: 85.43 грн.    
• Среднее количество страниц: 650.6.    
9. Показать тематики книг и сумму страниц всех книг по каждой из них.    
10. Показать количество всех книг и сумму страниц этих книг по каждому из авторов.    
11. Показать книгу тематики «Программирование» с наибольшим количеством страниц.    
12. Показать среднее количество страниц по каждой тематике, которое не превышает 400.    
13. Показать сумму страниц по каждой тематике, учитывая только книги с количеством страниц более 400, и чтобы тематики были Программирование», «Администрирование» и «Дизайн».    
14. Показать информацию о работе магазинов: что, где, кем, когда и в каком количестве было продано.    
15. Показать самый прибыльный магазин.

#### Решения домашних заданий SQL

## Homework 01

### Тема: "Основы взаимодействия с MySQL Server"

Задание. Необходимо создать базу данных Академия (Academy), которая будет содержать информацию о сотрудниках и внутреннем устройстве академии. Преподаватели, читающие лекции в академии представлены в виде таблицы.    
Преподаватели (Teachers), в которой собрана основная информация, такая как: имя, фамилия, данные о зарплате, а также дата приёма на работу.    
Также в базе данных присутствует информация о группах, хранимая в таблице Группы (Groups). Данные об факультетах и кафедрах содержатся в таблицах Факультеты (Faculties) и Кафедры (Departments) соответственно.    
Ниже представлено детальное описание структуры каждой таблицы.    
A) Группы (Groups)    
• Идентификатор (Id) – уникальный идентификатор группы: тип данных – int, авто приращение, не может содержать null-значения, первичный ключ.    
• Название (Name) – название группы: тип данных – nvarchar(10), не может содержать null-значения, не может быть пустым, должно быть уникальным.    
• Рейтинг (Rating) – рейтинг группы: тип данных – int, не может содержать null-значения, должно быть в диапазоне от 0 до 5.    
• Курс (Year) – курс (год) на котором обучается группа: тип данных – int, не может содержать null-значения, должно быть в диапазоне от 1 до 5.    
B) Кафедры (Departments)    
• Идентификатор (Id) – уникальный идентификатор кафедры: тип данных – int, авто приращение, не может содержать null-значения, первичный ключ.    
• Финансирование (Financing) – фонд финансирования кафедры: тип данных – money, не может содержать null-значения, не может быть меньше 0, значение по умолчанию – 0.    
• Название (Name) – название кафедры: тип данных – nvarchar(100), не может содержать null-значения, не может быть пустым, должно быть уникальным.    
C) Факультеты (Faculties)    
• Идентификатор (Id) – уникальный идентификатор факультета: тип данных – int, авто приращение, не может содержать null-значения, первичный ключ.    
• Название (Name) – название факультета: тип данных – nvarchar(100), не может содержать null-значения, не может быть пустым, должно быть уникальным.    
D) Преподаватели (Teachers)    
• Идентификатор (Id) – уникальный идентификатор преподавателя: тип данных – int, авто приращение, не может содержать null-значения, первичный ключ.    
• Дата трудоустройства (EmploymentDate) – дата приёма преподавателя на работу: тип данных – date, не может содержать null-значения, не может быть меньше 01.01.1990.    
• Имя (Name) – имя преподавателя: тип данных – nvarchar(max), не может содержать null-значения, не может быть пустым.    
• Надбавка (Premium) – надбавка преподавателя: тип данных – money, не может содержать null-значения, не может быть меньше 0, значение по умолчанию – 0.    
• Ставка (Salary) – ставка преподавателя: тип данных – money, не может содержать null-значения, не может быть меньше либо равно 0.    
• Фамилия (Surname) - фамилия преподавателя: тип данных – nvarchar(max), не может содержать null-значения, не может быть пустым.    

## Homework 02

### Тема: "Запросы Select, Insert, Update, Delete"

1. Вывести таблицу кафедр, но расположить её поля в обратном порядке.    
2. Вывести названия групп и их рейтинги с уточнением имён полей именем таблицы.    
3. Вывести для преподавателей их фамилию, процент ставки по отношению к надбавке и процент ставки по отношению к зарплате (сумма ставки и надбавки).    
4. Вывести таблицу факультетов в виде одного поля в следующем формате: "The dean of faculty [faculty] is [dean].".    
5. Вывести фамилии преподавателей, которые являются профессорами и ставка которых превышает 1050.    
6. Вывести названия кафедр, фонд финансирования которых меньше 11000 или больше 25000.    
7. Вывести названия факультетов кроме факультета "Computer Science".    
8. Вывести фамилии и должности преподавателей, которые не являются профессорами.    
9. Вывести фамилии, должности, ставки и надбавки ассистентов, у которых надбавка в диапазоне от 160 до 550.    
10. Вывести фамилии и ставки ассистентов.    
11. Вывести фамилии и должности преподавателей, которые были приняты на работу до 01.01.2000.    
12. Вывести названия кафедр, которые в алфавитном порядке располагаются до кафедры "Software Development". Выводимое поле должно иметь название "Name of Department".    
13. Вывести фамилии ассистентов, имеющих зарплату (сумма ставки и надбавки) не более 1200.    
14. Вывести названия групп 5-го курса, имеющих рейтинг в диапазоне от 2 до 4.    
15. Вывести фамилии ассистентов со ставкой меньше 550 или надбавкой меньше 200.

## Homework 03

### Тема: "Многотабличные базы данных"

1. Вывести все возможные пары строк преподавателей и групп.    
2. Вывести названия факультетов, фонд финансирования кафедр которых превышает фонд финансирования факультета.    
3. Вывести фамилии кураторов групп и названия групп, которые они курируют.    
4. Вывести имена и фамилии преподавателей, которые читают лекции у группы "P107".    
5. Вывести фамилии преподавателей и названия факультетов на которых они читают лекции.    
6. Вывести названия кафедр и названия групп, которые к ним относятся.    
7. Вывести названия дисциплин, которые читает преподаватель "Samantha Adams".    
8. Вывести названия кафедр, на которых читается дисциплина "Database Theory".    
9. Вывести названия групп, которые относятся к факультету "Computer Science".    
10. Вывести названия групп 5-го курса, а также название факультетов, к которым они относятся.    
11. Вывести полные имена преподавателей и лекции, которые они читают (названия дисциплин и групп), причём отобрать только те лекции, которые читаются в аудитории "B103".

## Homework 04

### Тема: "Подзапросы"

1. Вывести номера корпусов, если суммарный фонд финансирования расположенных в них кафедр превышает 100000.    
2. Вывести названия групп 5-го курса кафедры "Software Development", которые имеют более 10 пар в первую неделю.    
3. Вывести названия групп, имеющих рейтинг (средний рейтинг всех студентов группы) больше, чем рейтинг группы "D221".    
4. Вывести фамилии и имена преподавателей, ставка которых выше средней ставки профессоров.    
5. Вывести названия групп, у которых больше одного куратора.    
6. Вывести названия групп, имеющих рейтинг (средний рейтинг всех студентов группы) меньше, чем минимальный рейтинг групп 5-го курса.    
7. Вывести названия факультетов, суммарный фонд финансирования кафедр которых больше суммарного фонда финансирования кафедр факультета "Computer Science".    
8. Вывести названия дисциплин и полные имена преподавателей, читающих наибольшее количество лекций по ним.    
9. Вывести название дисциплины, по которому читается меньше всего лекций.    
10. Вывести количество студентов и читаемых дисциплин на кафедре "Software Development".

## Homework 05

### Тема: "Объединения"

1. Вывести названия аудиторий, в которых читает лекции преподаватель “Edward Hopper”.
2. Вывести фамилии ассистентов, читающих лекции в группе “F505”.
3. Вывести дисциплины, которые читает преподаватель “Alex Carmack” для групп 5-го курса.
4. Вывести фамилии преподавателей, которые не читают лекции по понедельникам.
5. Вывести названия аудиторий, с указанием их корпусов, в которых нет лекций в среду второй недели на третьей паре.
6. Вывести полные имена преподавателей факультета “Computer Science”, которые не курируют группы кафедры “Software Development”.
7. Вывести список номеров всех корпусов, которые имеются в таблицах факультетов, кафедр и аудиторий.
8. Вывести полные имена преподавателей в следующем порядке: деканы факультетов, заведующие кафедрами, преподаватели, кураторы, ассистенты.
9. Вывести дни недели (без повторений), в которые имеются занятия в аудиториях “A311” и “A104” корпуса 6.

## Homework 06

### Тема: "Работа с таблицами и представлениями"

Задание 1. Все задания необходимо выполнить по отношению к базе данных «Музыкальная коллекция», описанной в практическом задании для этого модуля. Создайте следующие представления:    
1. Представление отображает названия всех исполнителей.    
2. Представление отображает полную информацию о всех песнях: название песни, название диска, длительность песни, музыкальный стиль песни, исполнитель.    
3. Представление отображает информацию о музыкальных дисках конкретной группы. Например, The Beatles.    
4. Представление отображает название самого популярного в коллекции исполнителя. Популярность определяется по количеству дисков в коллекции.    
5. Представление отображает топ-3 самых популярных в коллекции исполнителей. Популярность определяется по количеству дисков в коллекции.    
6. Представление отображает самый долгий по длительности музыкальный альбом.    

Задание 2. Все задания необходимо выполнить по отношению к базе данных «Музыкальная коллекция», описанной в практическом задании для этого модуля:    
1. Создайте обновляемое представление, которое позволит вставлять новые стили.    
2. Создайте обновляемое представление, которое позволит вставлять новые песни.    
3. Создайте обновляемое представление, которое позволит обновлять информацию об издателе.    
4. Создайте обновляемое представление, которое позволит удалять исполнителей.    
5. Создайте обновляемое представление, которое позволит обновлять информацию о конкретном исполнителе. Например, Muse.    

Задание 3. Все задания необходимо выполнить по отношению к базе данных «Продажи», описанной в практическом задании для этого модуля:    
1. Создайте обновляемое представление, которое отображает информацию о всех продавцах.    
2. Создайте обновляемое представление, которое отображает информацию о всех покупателях.    
3. Создайте обновляемое представление, которое отображает информацию о всех продажах конкретного товара. Например, яблок.    
4. Создайте представление, отображающее все осуществлённые сделки.    
5. Создайте представление, отображающее информацию о самом активном продавце. Определяем самого активного продавца по максимальной общей сумме продаж.    
6. Создайте представление, отображающее информацию о самом активном покупателе. Определяем самого активного покупателя по максимальной общей сумме покупок.

Используйте опции CHECK OPTION, SCHEMABINDING, ENCRYPTION там, где это необходимо или полезно.

## LaboratoryWork 01

### Тема: "Работа с таблицами и представлениями"

Обращаем ваше внимание, что при именовании баз данных, таблиц, столбцов и других объектов необходимо придерживаться рекомендаций по именованию объектов в базах данных. Наименования объектов в заданиях даны только для объяснения поставленной задачи.

Задание 1. Создайте базу данных «Телефонный справочник». Эта база данных должна содержать одну таблицу «Люди». В таблице нужно хранить: ФИО человека, дату рождения, пол, телефон, город проживания, страна проживания, домашний адрес. Для создания базы данных используйте запрос CREATE DATABASE. Для создания таблицы используйте запрос CREATE TABLE.

Задание 2. Создайте базу данных «Продажи». База данных должна содержать информацию о продавцах, покупателях, продажах. Необходимо хранить следующую информацию:    
1. О продавцах: ФИО, email, контактный телефон.    
2. О покупателях: ФИО, email, контактный телефон.    
3. О продажах: покупатель, продавец, название товара, цена продажи, дата сделки.    

Для создания базы данных используйте запрос CREATE DATABASE. Для создания таблицы используйте запрос CREATE TABLE. Обязательно при создании таблиц задавать связи между ними.

Задание 3. Создайте базу данных «Музыкальная коллекция». База данных должна содержать информацию о музыкальных дисках, исполнителях, стилях. Необходимо хранить следующую информацию:    
1. О музыкальном диске: название диска, исполнитель, дата выпуска, стиль, издатель.    
2. О стилях: названия стилей.    
3. Об исполнителях: название.    
4. Об издателях: название, страна.    
5. О песнях: название песни, название диска, длительность песни, музыкальный стиль песни, исполнитель.    

Продумайте правильную структуру базы данных. Для создания базы данных используйте запрос CREATE DATABASE. Для создания таблицы используйте запрос CREATE TABLE. Обязательно при создании таблиц задавать связи между ними.

Задание 4. Все задания необходимо выполнить по отношению к базе данных из третьего задания:    
1. Добавьте к уже существующей таблице с информацией о музыкальном диске столбец с краткой рецензией на него.    
2. Добавьте к уже существующей таблице с информацией об издателе столбец с юридическим адресом главного офиса.    
3. Измените в уже существующей таблице с информацией о песнях размер поля, хранящий название песни.    
4. Удалите из уже существующей таблицы с информацией об издателе столбец с юридическим адресом главного офиса.    
5. Удалите связь между таблицами «музыкальных дисков» и «исполнителей».    
6. Добавьте связь между таблицами «музыкальных дисков» и «исполнителей».

Задание 5. Создайте следующие представления. В качестве базы данных используйте базу данных из третьего задания:    
1. Представление отображает названия всех стилей.    
2. Представление отображает названия всех издателей.    
3. Представление отображает полную информацию о диске: название диска, исполнитель, дата выпуска, стиль, издатель.

## LaboratoryWork 02

### Тема: "Триггеры"

Обращаем ваше внимание, что при именовании баз данных, таблиц, столбцов и других объектов необходимо придерживаться рекомендаций по именованию объектов в базах данных. Наименования объектов в заданиях даны только для объяснения поставленной задачи.

Задание 1. Создайте базу данных «Спортивный магазин». Эта база данных должна содержать информацию о товарах, продажах, сотрудниках, клиентах. Необходимо хранить следующую информацию:    
1. О товарах: название товара, вид товара (одежда, обувь, и т.д.), количество товара в наличии, себестоимость, производитель, цена продажи.    
2. О продажах: название проданного товара, цена продажи, количество, дата продажи, информация о продавце (ФИО сотрудника, выполнившего продажу), информация о покупателе (ФИО покупателя, если купил зарегистрированный покупатель).    
3. О сотрудниках: ФИО сотрудника, должность, дата приёма на работу, пол, зарплата.    
4. О клиентах: ФИО клиента, email, контактный телефон, пол, история заказов, процент скидки, подписан ли на почтовую рассылку.    
Продумайте правильную структуру базы данных. Для создания базы данных используйте запрос CREATE DATABASE. Для создания таблицы используйте запрос CREATE TABLE. Обязательно при создании таблиц задавать связи между ними.

Задание 2. Для базы данных из первого задания создайте триггеры, которые будут решать задачи ниже:    
1. При продаже товара, заносить информацию о продаже в таблицу «История». Таблица «История» используется для дубляжа информации о всех продажах.    
2. Если после продажи товара не осталось ни одной единицы данного товара, необходимо перенести информацию о полностью проданном товаре в таблицу «Архив».    
3. Не позволять регистрировать уже существующего клиента. При вставке проверять наличие клиента по ФИО и email.    
4. Запретить удаление существующих клиентов.    
5. Запретить удаление сотрудников, принятых на работу до 2015 года.    
6. При новой покупке товара нужно проверять общую сумму покупок клиента. Если сумма превысила 50000 грн, необходимо установить процент скидки в 15%.    
7. Запретить добавлять товар конкретной фирмы. Например, товар фирмы «Спорт, солнце и штанга».    
8. При продаже проверять количество товара в наличии. Если осталась одна единица товара, необходимо внести информацию об этом товаре в таблицу «Последняя Единица».
