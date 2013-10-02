[Внешняя компонента быстрого поиска в файлах базы данных 1С 7.7] (https://github.com/r72cccp/dbfsearch1C77 "Белевский Сергей. Внешняя компонента быстрого поиска в файлах базы данных 1С 7.7 Перейти на страницу проекта")
##Процедура сверхбыстрого поиска в таблицах БД 1С 
####На входе принимает три значения:
  1. Имя файла DBF, заключённое в кавычки, возможно с путём к нему. Если путь не задан - поиск файла делается в пределах текущего каталога
  2. Регулярное выражение для поиска, заключённое в кавычки.
  3. Имя файла с результатами поиска, заключённое в кавычки.

####Если параметры не заданы осуществляется тестовый прогон. 
  Для тестового прогона обязательно наличие файла cs156.dbf в текущем каталоге, откуда запущена компонента.

  На практике поиск в справочнике со 150000 элементами при нежадной регулярке идёт 2-3 секунды. Такой де поиск, но без регулярок средствами 1С 15-20 сек. (i7 3200)

  В результате поиска компонента должна вернуть массив кодов найденных элементов. 

####Там выложены следующие файлы: 
  search.cs                      - Рабочий исходник поиска. Работает при вызове из командной строки. 
  RegExpSearchInDBF.cs           - Тестовая пустышка, из которой я хочу получить внешнюю компоненту 
  AddIn.RegExpSearchInDBF_01.reg - Как эта компонента зарегестрирована у меня в реестре
