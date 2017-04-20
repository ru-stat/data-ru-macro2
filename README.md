# Доступные данные

Обозначение   | Источник                   | Название
--------------|----------------------------|--------------------------------------------
KEP           | [Росстат][kep-src]         | [Краткосрочные макроэкономические показатели РФ][kep]
806           | [Росстат][806-src]         | [Социально-экономическое положение регионов РФ][806]
FX            | [ЦБ РФ][806-src]           | <https://github.com/epogrebnyak/data-fx-oil>
OIL           | Quandl                     | <https://github.com/epogrebnyak/data-fx-oil>
UST           | [US Treasury][ust-src]     | [Кривые дохоности гособлигаций США][ust]
CB_SOAP       | ЦБ РФ                      | [Различные данные ЦБ через SOAP](https://github.com/epogrebnyak/cbr-soap-py)
BANKSTAT      | ЦБ РФ                      | Балансы банковской системы
BANKSTAT      | ЦБ РФ                      | [Статистика индивидуальных банков](https://github.com/epogrebnyak/cbr-db)
BOP           | ЦБ РФ                      | Платежный баланс
...           | ФTC                        |  ...
...           | Казначейство               |  ...

[kep-src]: http://www.gks.ru/wps/wcm/connect/rosstat_main/rosstat/ru/statistics/publications/catalog/doc_1140080765391
[kep]: https://github.com/epogrebnyak/data-rosstat-kep

[806-src]: http://www.gks.ru/wps/wcm/connect/rosstat_main/rosstat/ru/statistics/publications/catalog/doc_1246601078438
[806]: https://github.com/epogrebnyak/rosstat-806-regional

[ust-src]: https://www.treasury.gov/resource-center/data-chart-center/interest-rates/Pages/TextView.aspx?data=yield
[ust]: https://github.com/epogrebnyak/ust

# Способы визуализации

- <https://github.com/epogrebnyak/viz_demo>
- <https://github.com/epogrebnyak/additional/tree/master/plotting>

# Задачи 

1. Как сделать данные российской макроэкономической статистики такими же доступными и удобными для скачивания и обработки, как [FRED](https://fred.stlouisfed.org/)? *#dataset, #api, #quick_update*

2. Сезонное сглаживание, пересмотры статистики, длинные ряды:  
 - откуда получить сезонно сглаженные временные ряды макроэкономической статистики с известной, 
   воспроизводимой процедурой сглаживания? *#sa* 
 - как отследить пересмотры статистики? *#vintages*
 - взять длинные данные по РФ с 1990-1992 года? *#1992+*

3. Как компактно отразить текущие макроэкономические показатели - например, по аналогии с [NY FED full charts](https://www.newyorkfed.org/medialibrary/media/research/directors_charts/global_all.pdf) *#databook, #dashboard*

4. Как сделать результаты макроэконометрических моделей доступными и воспроизводимыми? *#jupiter_notebook*

5. Как получить быстрые периодические обновления российских и глобальных макроэкономических показателей? *#quick_update, #this_data, #as_if_bloomberg*
   
6. Какими аналогичными сервисами можно воспользоваться для этих же задач? *#not_just_here*

TODO (2017-04-18): уточнить актуальность задач на основе опроса

# Задача "Наборы данных"

*#dataset, #api, #quick_update*

## 1. Краткосрочные макроэкономические показатели (KEP)

Краткосрочные макроэкономические показатели - основная публикация Росстата с рядами данных. Росстат распространяет публикацию [в виде файлов Word][rosstat-src], мы вывешиваем эти данные в виде временных рядов в свободном доступе в CSV И Excel. 

- Источник: [Росстат](http://www.gks.ru/wps/wcm/connect/rosstat_main/rosstat/ru/statistics/publications/catalog/doc_1140080765391)
- Данные в CSV и Excel: [output][tab-output]
- Скачивание и парсинг:
 - [ ] код скачивания: нет
 - [X] код парсинга: <https://github.com/epogrebnyak/data-rosstat-kep/tree/master/kep>
 - [X] development: <https://github.com/epogrebnyak/data-rosstat-kep/tree/master/kep2>

- Прочее
 - [ ] Архив релизов: Нет
 - [ ] API: нет

[rosstat-src]: http://www.gks.ru/wps/wcm/connect/rosstat_main/rosstat/ru/statistics/publications/catalog/doc_1140080765391
[tab-output]: https://github.com/epogrebnyak/data-rosstat-kep/tree/master/output

TODO (2017-04-18): 
- [ ] убрать графику из output в отдельный каталог, оставить только Excel и CSV
- [ ] показать отличия данных по релизам  



# Комментарии

Собраны ссылки на открытые источники исходных макроэкономических данных, а также наборы данных, преобразованные с целью упрощения их импорта и использования. 

Основные задачи:

- построить согласованную систему описания экономики РФ на основе открытых данных
- преобразовать источники исходных данных в лекго импортируемые и периодически обновляемые наборы данных 
- указать на пробелы в открытом статистическом обеспечении
- показать возможности стыковки и взимной верификации различных источников и наборов данных 

Текущие работы:
- [ ] упростить и обобщить механизм скачивания файлов на основе [ru-macro-src](https://github.com/epogrebnyak/ru-macro-src/tree/master/files) и элементов 
[cbr-db](https://github.com/epogrebnyak/cbr-db) используя ```requests```
- [ ] стандартизация сбора и хранения данных между пакетами
- [ ] данные на R по "зеркальным" балансам ЦБ и банков выложить в репозитарий 
- [ ] оформление графиков в R - ```ccorp``` выложить
- [ ] optional: старый код, замещенный новым, дать в архивные ветки репозитариев


Репозитарии в разработке:

- <https://github.com/epogrebnyak/rosstat-kep-data>
- <https://github.com/epogrebnyak/rosstat-806-regional>
- <https://github.com/epogrebnyak/cbr-soap-py>
- <https://github.com/epogrebnyak/cbr-db>
- <https://github.com/epogrebnyak/fx-oil>
- <https://github.com/epogrebnyak/additional/tree/master/plotting>

## 1. Цены на нефть и другие товары 
 - Brent, EIA: см. <https://github.com/epogrebnyak/fx-oil>
 - Urals - хорошего открытого источника нет
 - другие товары биржевые товары

## 2. Росстат

2.1 Россия в цифрах 

2.2 Оперативная статистика:

 - Краткосрочные эконимические показатели РФ (КЭП): см. <https://github.com/epogrebnyak/rosstat-kep-data>
 - Социально-экономическое положежние РФ (СЭП)

2.3 СНС и информация по темам 
 
2.4 Региональная статистика:
 - постановление 806: см. <https://github.com/epogrebnyak/rosstat-806-regional>
 - годовой сборник региональной статистики (с отраслями)

## 3. Бюджет
- данные казначейства по исполнению бюджета
- данные Минфина
- ФНС - поступления налогов

## 4. ФTC - таможенная статистика

## 5. Банк России

Ежедневные данные - см.<https://github.com/epogrebnyak/cbr-soap-py>: 
- процентные ставки
- валютный курс
- операции Банка России 
- отдельные позиций баланса банков

Месячные данные:
- сводная банковская статистика см. <https://github.com/epogrebnyak/cbr-db>
- платежный баланс

# Сводная информация

## Презентации по экономической статистике
 - NY FED [Global Economic Indicators](https://www.newyorkfed.org/research/global_economy/globalindicators.html) and [full charts](https://www.newyorkfed.org/medialibrary/media/research/directors_charts/global_all.pdf)
 - ЦМАКП: Макроэкономические индикаторы (http://www.forecast.ru/Indicators.aspx)
 - ИКСИ: [Основные социально-экономические показатели](http://www.icss.ac.ru/macro/)

## Статистика, собранная в одном месте
 - sophist
 - fedstat
 
## Провайдеры данных
- CEIC
- Bloomberg econ data
