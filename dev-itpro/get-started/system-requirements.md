---
title: "Требования к системе"
description: "В этой теме перечислены требования к системе для текущей версии Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 724ee7ec29f8a9c4e8cc0b244193cd6c83c37f03
ms.contentlocale: ru-ru
ms.lasthandoff: 06/13/2017


---

# <a name="system-requirements"></a>Требования к системе

[!include[banner](../includes/banner.md)]


В этой теме перечислены требования к системе для текущей версии Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

<a name="supported-web-browsers"></a>Поддерживаемые веб-браузеры
----------------------

Веб-приложение может выполняться в любом веб-браузере, который работает в указанных операционных системах:

-   Microsoft Edge (последняя публично доступная версия) в Windows 10
-   Internet Explorer 11 в Windows 10, Windows 8.1 или Windows 7
-   Google Chrome (последняя публично доступная версия) в Windows 10, Windows 8.1, Windows 8, Windows 7 или на планшете Google Nexus 10
-   Apple Safari (последняя публично доступная версия) в Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) или 10.12 (Sierra) или Apple iPad

Чтобы найти последний выпуск для каждого веб-браузера, перейдите на веб-сайт производителя программного обеспечения. 

**Примечания.**

-   Для захвата изображений, создаваемых в регистраторе задач, и включения их в документы Microsoft Word должна быть установлена предварительная версия расширения Chrome. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
-   Редактор workflow-процессов запускается в виде приложения ClickOnce. Только Microsoft Edge и Internet Explorer (на поддерживаемой версии Microsoft Windows) поддерживают приложение ClickOnce. Для приложения ClickOnce редактора workflow-процессов требуется 64-разрядная совместимая операционная система.
-   Конструктор отчетов для финансовой отчетности запускается в виде приложения ClickOnce. Для него требуется 64-разрядная совместимая операционная система. При использовании браузера Chrome необходимо установить расширение ClickOnce, чтобы можно было загрузить клиент конструктора отчетов. При работе с Chrome в режиме инкогнито убедитесь, что расширение ClickOnce также включено для работы в режиме инкогнито.
-   Для предварительного просмотра PDF-файлов рекомендуется использовать такие браузеры, как Microsoft Edge (последней общедоступной версии) в Windows 10 или Google Chrome (последней общедоступной версии) в Windows 10, Windows 8.1, Windows 8, Windows 7 или на планшете Google Nexus 10.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Поддерживаемые веб-браузеры для Retail Cloud POS

Retail Cloud POS может выполняться в любом веб-браузере, который работает в указанных операционных системах:

-   Microsoft Edge (последняя публично доступная версия) в Windows 10
-   Internet Explorer 11 в Windows 10, Windows 8.1 или Windows 7
-   Chrome (последняя общедоступная версия) на Windows 10, Windows 8.1 или Windows 7

## <a name="network-requirements"></a>Требования к сети
-   Система Dynamics 365 for Finance and Operations, Enterprise edition предназначена для сетей с задержкой 250-300 миллисекунд (мс) и менее. Это задержка от клиента браузера до центра данных Microsoft Azure, на котором размещена система Finance and Operations. Рекомендуется проверить задержку в сети на сайте <http://www.azurespeed.com>.
-   Требования к пропускной способности зависят от конкретного сценария реализации. В большинстве типичных сценариев требуется пропускная способность более 50 Кбайт в секунду (КБ/с). Однако для сценариев с высокими требованиями к полезной нагрузке, таким как рабочие области, или для сценариев, которые включают широкую индивидуальную настройку, рекомендуется большая пропускная способность.

В целом система Finance and Operations оптимизирована для работы в Интернете. Число пересылок данных туда и обратно с клиента браузера до центра данных Azure достаточно невелико, и все полезные данные сжимаются. 

**Предупреждение:** Не вычисляйте требования к пропускной способности из местоположения клиента путем умножения числа пользователей на минимальные требования к пропускной способности. Параллельное использование для конкретного местоположения рассчитать сложно. Клиентам, которых беспокоят требования к пропускной способности, следует воспользоваться предварительной версией Finance and Operations.

## <a name="net-framework-requirements"></a>Требования к .NET Framework
Для всех приложений ClickOnce, таких как агент маршрутизации документов, требуется наличие .NET Framework version 4.6.2. Инструкции по установке см. в разделе [Установка .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Поддерживаемые приложения Microsoft Office
-   Для запуска надстроек Microsoft Excel и Word должен быть установлен Microsoft Office 2016 для Windows или Mac. Дополнительные сведения о требованиях к версии см. в разделе [Устранение неполадок при интеграции Office](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Для просмотра документов, созданных с помощью функции экспорта в Excel или экспорта в Word должен быть установлен пакет Microsoft Office 2007 или более поздняя версия.

## <a name="retail-modern-pos-requirements"></a>Требования для Retail Modern POS
### <a name="supported-operating-systems"></a>Поддерживаемые операционные системы

-   Retail Modern POS — это 32-разрядное приложение, но оно будет работать как в архитектуре x86, так и в архитектуре x64.
-   Retail Modern POS поддерживается только в выпусках Windows 10 Pro, Корпоративная и Корпоративная с долгосрочным обслуживанием (LTSB).

### <a name="minimum-system-requirements"></a>Минимальные требования к системе

-   Минимальное поддерживаемое разрешение: 1280 × 1024.
-   Компьютер, на котором будет выполняться Retail Modern POS, должен соответствовать следующим требованиям:
    -   Он должен иметь, как минимум, двухъядерный процессор, работающий на частоте не менее 2 ГГц.
    -   Он должна иметь не менее 3 ГБ ОЗУ.
    -   Он должен быть подключен к Интернету.

## <a name="retail-hardware-station-requirements"></a>Требования для станции оборудования Retail
### <a name="supported-operating-systems"></a>Поддерживаемые операционные системы

-   Станция оборудования Retail — это 32-разрядное приложение, но оно будет работать как в архитектуре x86, так и в архитектуре x64.
-   Станция оборудования Retail поддерживается в следующих операционных системах:
    -   Выпуски Windows 7 Профессиональная, Корпоративная и Максимальная **Примечание.** Windows 7 поддерживается только в том случае, если Internet Explorer 11 вручную установлен в системе.
    -   Windows 8.1 с обновлением 1, выпуски Профессиональная, Корпоративная и Встроенная
    -   Выпуски Windows 10 Pro, Корпоративная и Корпоративная LTSB

### <a name="minimum-system-requirements"></a>Минимальные требования к системе

Компьютер должен удовлетворять всем требованиям к системе для установки и использования следующих элементов:

-   Службы IIS (Internet Information Services)
-   Оборудование независимых производителей

## <a name="retail-store-scale-unit-requirements"></a>Требования к модулю весов для розничного магазина Retail Store Scale Unit
### <a name="supported-operating-systems"></a>Поддерживаемые операционные системы

-   Retail Store Scale Unit — это 32-разрядное приложение, но оно будет работать как в архитектуре x86, так и в архитектуре x64.
-   Retail Store Scale Unit поддерживается в следующих операционных системах:
    -   Выпуски Windows 7 Профессиональная, Корпоративная и Максимальная
    -   Windows 8.1 с обновлением 1, выпуски Профессиональная, Корпоративная и Встроенная
    -   Выпуски Windows 10 Pro, Корпоративная и Корпоративная LTSB

### <a name="minimum-system-requirements"></a>Минимальные требования к системе

-   4 ГБ ОЗУ
-   Пиковая скорость работы процессора 1,6 ГГц на ядро (Не менее двух ядер.)
-   По крайней мере 10 ГБ свободного места (Для канала базы данных может потребоваться большой объем пространства.)

### <a name="recommended-system-requirements"></a>Рекомендуемые требования к системе

-   6 ГБ ОЗУ
-   Процессор i7 (или аналогичный) с пиковой скоростью работы 2,4 ГГц на ядро (Рекомендуется четыре ядра.)
-   По крайней мере 10 ГБ свободного места (Для канала базы данных может потребоваться большой объем пространства.)

## <a name="connector-requirements"></a>Требования соединителя
### <a name="supported-operating-systems"></a>Поддерживаемые операционные системы

-   Для соединителя Microsoft Dynamics AX предусмотрено два отдельных установщика: **служба Async Server Connector** и **служба Real-time service for Dynamics AX 2012 R3**.
-   Оба компонента представляют собой 32-разрядные приложения, но будут работать как в архитектуре x86, так и в архитектуре x64.
-   Оба компонента поддерживаются в следующих операционных системах:
    -   Выпуски Windows 7 Профессиональная, Корпоративная и Максимальная
    -   Windows 8.1 с обновлением 1, выпуски Профессиональная, Корпоративная и Встроенная
    -   Выпуски Windows 10 Pro, Корпоративная и Корпоративная LTSB
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Минимальные требования к системе

-   2 ГБ ОЗУ, рекомендуется 4 ГБ ОЗУ
-   Пиковая скорость работы процессора 1,6 ГГц на ядро (Не менее двух ядер.)
-   По крайней мере 10 ГБ свободного места (Для канала базы данных может потребоваться большой объем пространства.)

## <a name="requirements-for-development-on-local-vms"></a>Требования для разработки на локальных виртуальных машинах
Сведения о требованиях к разработке на локальных виртуальных машинах (VM) в разделе [Локальные виртуальные машины](../dev-tools/access-instances.md).

<a name="see-also"></a>См. также
--------

[Получение ознакомительной версии Dynamics 365 for Finance and Operations, Enterprise edition](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)





