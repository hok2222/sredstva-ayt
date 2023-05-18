# Получение сведений о системе
Шаршов Иван

# Получение сведений о системе

## Цель работы

Получить сведения об используемой системе

## Исходные данные

1.  Ноутбук Huawei

2.  Windows

## План

1.  Ввод команд в эмулятор терминала

2.  Анализ данных

## Ход работы

1.  Затем получим сведения о версии ядра:

``` bash
uname -r
```

    5.15.90.1-microsoft-standard-WSL2

1.  Далее можно получить сведения о процессоре:

``` bash
cat /proc/cpuinfo | grep "model name"
```

    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics
    model name  : AMD Ryzen 5 5500U with Radeon Graphics

1.  Далее получим последние 30 строк логов системы:

``` bash
dmesg | tail -n 30
```

    [    3.345775] 9pnet_virtio: no channels available for device drvfs
    [    3.346484] WSL (1) WARNING: mount: waiting for virtio device drvfs
    [    3.402518] hv_pci 49786306-0138-4071-b67b-8673d60914c5: PCI host bridge to bus 0138:00
    [    3.403208] pci_bus 0138:00: root bus resource [mem 0xbffe10000-0xbffe12fff window]
    [    3.403914] pci_bus 0138:00: No busn resource found for root bus, will use [bus 00-ff]
    [    3.406310] pci 0138:00:00.0: [1af4:1049] type 00 class 0x010000
    [    3.408506] pci 0138:00:00.0: reg 0x10: [mem 0xbffe10000-0xbffe10fff 64bit]
    [    3.410286] pci 0138:00:00.0: reg 0x18: [mem 0xbffe11000-0xbffe11fff 64bit]
    [    3.412663] pci 0138:00:00.0: reg 0x20: [mem 0xbffe12000-0xbffe12fff 64bit]
    [    3.418523] pci_bus 0138:00: busn_res: [bus 00-ff] end is updated to 00
    [    3.419251] pci 0138:00:00.0: BAR 0: assigned [mem 0xbffe10000-0xbffe10fff 64bit]
    [    3.420466] pci 0138:00:00.0: BAR 2: assigned [mem 0xbffe11000-0xbffe11fff 64bit]
    [    3.421834] pci 0138:00:00.0: BAR 4: assigned [mem 0xbffe12000-0xbffe12fff 64bit]
    [    3.452555] hv_pci 993351d5-75e8-42bc-aad7-d83cadbfbb25: PCI VMBus probing: Using version 0x10003
    [    3.511256] hv_pci 993351d5-75e8-42bc-aad7-d83cadbfbb25: PCI host bridge to bus 75e8:00
    [    3.511976] pci_bus 75e8:00: root bus resource [mem 0xbffe14000-0xbffe16fff window]
    [    3.512603] pci_bus 75e8:00: No busn resource found for root bus, will use [bus 00-ff]
    [    3.514580] pci 75e8:00:00.0: [1af4:1049] type 00 class 0x010000
    [    3.516419] pci 75e8:00:00.0: reg 0x10: [mem 0xbffe14000-0xbffe14fff 64bit]
    [    3.517983] pci 75e8:00:00.0: reg 0x18: [mem 0xbffe15000-0xbffe15fff 64bit]
    [    3.519457] pci 75e8:00:00.0: reg 0x20: [mem 0xbffe16000-0xbffe16fff 64bit]
    [    3.525196] pci_bus 75e8:00: busn_res: [bus 00-ff] end is updated to 00
    [    3.525772] pci 75e8:00:00.0: BAR 0: assigned [mem 0xbffe14000-0xbffe14fff 64bit]
    [    3.527224] pci 75e8:00:00.0: BAR 2: assigned [mem 0xbffe15000-0xbffe15fff 64bit]
    [    3.528481] pci 75e8:00:00.0: BAR 4: assigned [mem 0xbffe16000-0xbffe16fff 64bit]
    [    3.633370] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    3.634204] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    3.634930] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    3.635584] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    3.636240] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -2

## Оценка результата

В результате лабораторной работы была получена базовая информация об
используемой системе.

## Вывод

Таким образом. мы научились, используя команды Windows, получать
сведения о системе.
