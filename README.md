# Лабораторные работы по дисципоине "Средства аутентификации и защиты от несанкционированного доступа"

## Студент группы БИСО-03-20 Шаршов И.А.

# Список выполненных лабораторных работ:

## 1. Получение сведений о системе



# Получение сведений о системе

## Цель работы

Получить сведения об используемой системе

## Исходные данные

1. Ноутбук Huawei

2. Windows 



## План

1. Ввод команд в эмулятор терминала

2. Анализ данных

## Ход работы


1. Затем получим сведения о версии ядра:

winver


В результате выполнения данной команды была получена версия ядра - 21H2(сборка ОС 19044.2251)

2. Далее можно получить сведения о процессоре:

```
#1я команда
Get-WmiObject win32_Processor
Caption           : AMD64 Family 23 Model 104 Stepping 1
DeviceID          : CPU0
Manufacturer      : AuthenticAMD
MaxClockSpeed     : 2100
Name              : AMD Ryzen 5 5500U with Radeon Graphics
SocketDesignation : CPU0
#2я команда
WMIC CPU Get DeviceID,NumberOfCores,NumberOfLogicalProcessors
DeviceID  NumberOfCores  NumberOfLogicalProcessors
CPU0      6              12
```

Было определено, что используемый процессор - шестиядерный и двенадцатипоточный AMD Ryzen 5 5500U with Radeon Graphics

3. Далее получим последние 30 строк логов системы:

```Get-EventLog -LogName 'system' -Newest 30

   Index Time          EntryType   Source                 InstanceID Message
   ----- ----          ---------   ------                 ---------- -------
   26630 мар 01 15:01  Information Service Control M...   1073748864 Тип запуска службы "Фоновая интеллектуальная сл...
   26629 мар 01 14:53  Information amdi2scodec            1074141056 Не найдено описание для события с кодом '107414...
   26628 мар 01 14:52  Information amdi2scodec            1074141041 Не найдено описание для события с кодом '107414...
   26627 мар 01 14:52  Information amdi2scodec            1074135041 Не найдено описание для события с кодом '107413...
   26626 мар 01 14:52  Information amdi2scodec            1074141041 Не найдено описание для события с кодом '107414...
   26625 мар 01 14:52  Information amdi2scodec            1074141041 Не найдено описание для события с кодом '107414...
   26624 мар 01 14:52  Information amdi2scodec            1074135041 Не найдено описание для события с кодом '107413...
   26623 мар 01 14:52  Information amdi2scodec            1074141057 Не найдено описание для события с кодом '107414...
   26622 мар 01 14:47  Information amdi2scodec            1074141056 Не найдено описание для события с кодом '107414...
   26621 мар 01 14:47  Information amdi2scodec            1074141041 Не найдено описание для события с кодом '107414...
   26620 мар 01 14:47  Information amdi2scodec            1074135041 Не найдено описание для события с кодом '107413...
   26619 мар 01 14:47  Information amdi2scodec            1074141041 Не найдено описание для события с кодом '107414...
   26618 мар 01 14:47  Information amdi2scodec            1074141041 Не найдено описание для события с кодом '107414...
   26617 мар 01 14:47  Information amdi2scodec            1074135041 Не найдено описание для события с кодом '107413...
   26616 мар 01 14:47  Information amdi2scodec            1074141057 Не найдено описание для события с кодом '107414...
   26615 мар 01 14:36  Information Service Control M...   1073748864 Тип запуска службы "Фоновая интеллектуальная сл...
   26614 мар 01 14:36  Information amdi2scodec            1074141056 Не найдено описание для события с кодом '107414...
   26613 мар 01 14:35  Information amdi2scodec            1074141041 Не найдено описание для события с кодом '107414...
   26612 мар 01 14:35  Information amdi2scodec            1074135041 Не найдено описание для события с кодом '107413...
   26611 мар 01 14:35  Information amdi2scodec            1074135041 Не найдено описание для события с кодом '107413...
   26610 мар 01 14:35  Information amdi2scodec            1074141041 Не найдено описание для события с кодом '107414...
   26609 мар 01 14:35  Information amdi2scodec            1074141057 Не найдено описание для события с кодом '107414...
   26608 мар 01 14:35  Warning     DCOM                        10016 Не найдено описание для события с кодом '10016'...
   26607 мар 01 14:35  Information Microsoft-Windows...           19 Установка завершена: следующее обновление было ...
   26606 мар 01 14:34  Information Microsoft-Windows...           43 Установка начата: ОС Windows начала устанавлива...
   26605 мар 01 14:34  Information Microsoft-Windows...           44 Центр обновления Windows начал скачивать обновл...
   26604 мар 01 14:34  Information Microsoft-Windows...           16 Не найдено описание для события с кодом '16' в ...
   26603 мар 01 14:34  Information Microsoft-Windows...           15 Не найдено описание для события с кодом '15' в ...
   26602 мар 01 14:33  Information Service Control M...   1073748864 Тип запуска службы "Фоновая интеллектуальная сл...
   26601 мар 01 14:33  Warning     Microsoft-Windows...         1014 Разрешение имен для имени t-ring-fallbacks2.mse...
```

## Оценка результата

В результате лабораторной работы была получена базовая информация об используемой системе.

## Вывод

Таким образом. мы научились, используя команды Windows, получать сведения о системе.


