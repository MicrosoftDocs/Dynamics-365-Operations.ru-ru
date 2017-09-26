---
title: "Требования к системе для облачных развертываний"
description: "В этой теме перечислены требования к системе для текущей версии Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, для облачных сред."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 5230911e1febc66b294f1331846373a472789adf
ms.openlocfilehash: 46eacb2a01c3bfcc7144c7d8c39ee0189fd72e16
ms.contentlocale: ru-ru
ms.lasthandoff: 08/04/2017

---

# <a name="system-requirements-for-cloud-deployments"></a>Требования к системе для облачных развертываний

[!include[banner](../includes/banner.md)]

В этой теме перечислены требования к системе для текущей версии Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, для облачных сред. Перед установкой Finance and Operations при необходимости убедитесь, что система, с которой вы работаете, соответствует минимальным требованиям к сети, оборудованию и программному обеспечению или превышает их.

## <a name="supported-web-browsers"></a>Поддерживаемые веб-браузеры
Веб-приложение может выполняться в любом веб-браузере, который работает в указанных операционных системах:

-   Microsoft Edge (последняя публично доступная версия) в Windows 10
-   Internet Explorer 11 в Windows 10, Windows 8.1 или Windows 7
-   Google Chrome (последняя публично доступная версия) в Windows 10, Windows 8.1, Windows 8, Windows 7 или на планшете Google Nexus 10
-   Apple Safari (последняя публично доступная версия) в Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) или 10.12 (Sierra) или Apple iPad

Чтобы найти последний выпуск для каждого веб-браузера, перейдите на веб-сайт производителя программного обеспечения. 

> [!NOTE]
> -   Чтобы регистратор задач мог захватывать снимки экрана и включать их в формируемые документы Microsoft Word, необходимо установить предварительную версию расширения Chrome. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Редактор workflow-процессов запускается в виде приложения ClickOnce. Только Microsoft Edge и Internet Explorer (на поддерживаемой версии Microsoft Windows) поддерживают приложение ClickOnce. Для приложения ClickOnce редактора workflow-процессов требуется 64-разрядная совместимая операционная система.
> -   Конструктор отчетов для финансовой отчетности запускается в виде приложения ClickOnce. Для него требуется 64-разрядная совместимая операционная система. При использовании браузера Chrome необходимо установить расширение ClickOnce, чтобы можно было загрузить клиент Конструктора отчетов. При работе с Chrome в режиме инкогнито убедитесь, что расширение ClickOnce также включено для работы в режиме инкогнито.
> -   Для предварительного просмотра PDF-файлов рекомендуется использовать такие браузеры, как Microsoft Edge (последней общедоступной версии) в Windows 10 или Google Chrome (последней общедоступной версии) в Windows 10, Windows 8.1, Windows 8, Windows 7 или на планшете Google Nexus 10.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Поддерживаемые веб-браузеры для Retail Cloud POS

Retail Cloud POS может выполняться в любом веб-браузере, который работает в указанных операционных системах:

-   Microsoft Edge (последняя публично доступная версия) в Windows 10
-   Internet Explorer 11 в Windows 10, Windows 8.1 или Windows 7
-   Chrome (последняя общедоступная версия) на Windows 10, Windows 8.1 или Windows 7

## <a name="network-requirements"></a>Требования к сети
-   Система Finance and Operations предназначена для сетей с задержкой не более 250-300 мс. Это задержка от клиента браузера до центра данных Microsoft Azure, на котором размещена система Finance and Operations. Рекомендуется проверить задержку в сети на сайте <http://www.azurespeed.com>.
-   Требования к пропускной способности для Finance and Operations зависят от конкретного сценария. В большинстве типичных сценариев требуется пропускная способность более 50 Кбайт в секунду (КБ/с). Однако для сценариев с высокими требованиями к полезной нагрузке, например при использовании рабочих областей или широкой индивидуальной настройке, рекомендуется большая пропускная способность.

В целом система Finance and Operations оптимизирована для работы в Интернете. Число пересылок данных туда и обратно с клиента браузера до центра данных Azure очень мало, и все полезные данные сжимаются. 

> [!WARNING]
> Не вычисляйте требования к пропускной способности из местоположения клиента путем умножения числа пользователей на минимальные требования к пропускной способности. Параллельное использование для конкретного местоположения очень сложно рассчитать. Клиентам, которых беспокоят требования к пропускной способности, следует воспользоваться предварительной версией Finance and Operations.

## <a name="net-framework-requirements"></a>Требования к .NET Framework
Finance and Operations требует наличия Microsoft .NET Framework версии 4.6.2 для всех приложений ClickOnce, таких как агент маршрутизации документов. Инструкции по установке см. в разделе [Установка .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Поддерживаемые приложения Microsoft Office
Следующие приложения Microsoft Office поддерживаются в облачных и локальных развертываниях Finance and Operations:

-   Для запуска надстроек Microsoft Excel и Word должен быть установлен Microsoft Office 2016 для Windows или Mac. Дополнительные сведения о требованиях к версиям см. в разделе [Устранение неполадок при интеграции Office](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Для просмотра документов, созданных с помощью функции экспорта в Excel или экспорта в Word должен быть установлен пакет Microsoft Office 2007 или более поздняя версия.

## <a name="retail-modern-pos-requirements"></a>Требования для Retail Modern POS

> [!NOTE]
> Если в Retail Modern POS будет использоваться автономная база данных, компьютер должен удовлетворять всем требованиям к системе для Microsoft SQL Server. Автономная база данных Retail Modern POS будет работать в Microsoft SQL Server 2012 с пакетом обновления 3 или более поздним, Microsoft SQL Server 2014 с пакетом обновления 2 или более поздним, а также в Microsoft SQL Server 2016. Рекомендуем всегда использовать последнюю доступную версию и устанавливать все последние пакеты обновления.

### <a name="supported-operating-systems"></a>Поддерживаемые операционные системы

-   Retail Modern POS — это 32-разрядное приложение, но оно будет работать как в архитектуре x86, так и в архитектуре x64.
-   Retail Modern POS поддерживается только в выпусках Windows 10 Pro, Корпоративная и Корпоративная с долгосрочным обслуживанием (LTSB).

### <a name="minimum-system-requirements"></a>Минимальные требования к системе

-   Минимальное поддерживаемое разрешение: 1280 × 1024.
-   Компьютер, на котором будет выполняться Retail Modern POS, должен соответствовать следующим требованиям:

    -   Он должен иметь, как минимум, двухъядерный процессор, работающий на частоте не менее 2 ГГц.
    -   Он должен иметь не менее 3 ГБ ОЗУ.
    -   Он должен быть подключен к Интернету.

## <a name="retail-hardware-station-requirements"></a>Требования для станции оборудования Retail
### <a name="supported-operating-systems"></a>Поддерживаемые операционные системы

-   Станция оборудования Retail — это 32-разрядное приложение, но оно будет работать как в архитектуре x86, так и в архитектуре x64.
-   Станция оборудования Retail поддерживается в следующих операционных системах:

    -   Выпуски Windows 7 Профессиональная, Корпоративная и Максимальная 
    
        > [!NOTE]
        > Windows 7 поддерживается, только если Internet Explorer 11 вручную установлен в системе.

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

-   Для соединителя Microsoft Dynamics AX предусмотрено два отдельных установщика: один для службы Async Server Connector и один для службы Real-time service for Dynamics AX 2012 R3.
-   Оба компонента представляют собой 32-разрядные приложения, но будут работать как в архитектуре x86, так и в архитектуре x64.
-   Оба компонента поддерживаются в следующих операционных системах:

    -   Выпуски Windows 7 Профессиональная, Корпоративная и Максимальная
    -   Windows 8.1 с обновлением 1, выпуски Профессиональная, Корпоративная и Встроенная
    -   Выпуски Windows 10 Pro, Корпоративная и Корпоративная LTSB
    -   Microsoft Windows Server 2012 R2 и Microsoft Windows Server 2016

### <a name="minimum-system-requirements"></a>Минимальные требования к системе
-   2 ГБ ОЗУ (рекомендуется 4 ГБ ОЗУ)
-   Пиковая скорость работы процессора 1,6 ГГц на ядро (Не менее двух ядер.)
-   По крайней мере 10 ГБ свободного места (Для канала базы данных может потребоваться большой объем пространства.)

## <a name="requirements-for-development-on-local-vms"></a>Требования для разработки на локальных виртуальных машинах
Сведения о требованиях к разработке на локальных виртуальных машинах (VM) в разделе [Локальные виртуальные машины](../dev-tools/access-instances.md).


## <a name="see-also"></a>См. также

[Получение ознакомительной версии Dynamics 365 for Finance and Operations, Enterprise edition](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)
