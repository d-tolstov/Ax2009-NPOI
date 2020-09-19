# Обёртка для NPOI в Ax2009

Если в Ax2009 включить поддержку .NET Framework 4, то появляется возможность использовать пакет [NPOI](https://github.com/tonyqus/npoi).  
Для чтения файлов `Excel` в форматах `xls` и `xlsx`. В данном репозитории речь будет идти о работе этого пакета именно с файлами Excel.  
По понятным причинам его можно использовать только в серверных классах. Всем клиентам тяжело копировать эту библиотеку.

## Список dll

Путь к nuget-пакету - https://www.nuget.org/packages/NPOI/  
Из пакета нужно вынуть и скопировать в каталог bin на сервере и на компьютеры разработчиков следующие dll :
* NPOI.dll
* NPOI.OOXML.dll
* NPOI.OpenXml4Net.dll
* NPOI.OpenXmlFormats.dll

И подключить их в виде референсов в аксапте.

## Необходимые дополнительные референсы в аксапте

Также необходимо в аксапте подключить в качестве референсов dll из следующих nuget-пакетов :
* https://www.nuget.org/packages/Portable.BouncyCastle/
* https://www.nuget.org/packages/SharpZipLib/

## Class diagram

<img src="schema\Ax2009-NPOI.png" alt="схема">

## Dependencies

* [.Net Framework 4 Support](https://github.com/d-tolstov/Ax2009-NetFramework4-Support)
* [NPOI](https://github.com/tonyqus/npoi)