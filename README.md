# Открытые макроэкономические данные

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
- [ ] оформление графиков в R - ccorp выложить


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
