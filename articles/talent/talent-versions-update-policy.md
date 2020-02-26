---
title: Системные требования Talent
description: В этом разделе перечислены требования к Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 509827d5736887f56e7754a0760af7dea76277f7
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006063"
---
# <a name="talent-system-requirements"></a>Системные требования Talent

[!include [banner](includes/banner.md)]

В этом разделе описываются требования для Microsoft Dynamics 365 Talent, включая Attract и Onboard. Кроме того, в нем описываются страны и регионы, в которых доступно приложение Talent, а также сведения о языках и локализации для данных Talent. В дополнение этот раздел представляет политику обновления для Talent.

## <a name="supported-web-browsers"></a>Поддерживаемые веб-браузеры

Microsoft Dynamics 365 Talent может выполняться в любом веб-браузере, который работает в указанных операционных системах: 

*   Microsoft Edge (последняя публично доступная версия) в Windows 10
*   Internet Explorer 11 в Windows 10, Windows 8.1 или Windows 7
*   Google Chrome (последняя публично доступная версия)
*   Apple Safari (последняя публично доступная версия)

Чтобы найти последний выпуск для каждого веб-браузера, перейдите на веб-сайт производителя программного обеспечения. 

> [!NOTE]
> * Для захвата изображений, создаваемых в регистраторе задач, и включения их в документы Microsoft Word должно быть установлено расширение Chrome. 
> * Редактор workflow-процессов запускается в виде приложения ClickOnce. Только Microsoft Edge и Internet Explorer (на поддерживаемой версии Microsoft Windows) поддерживают приложения ClickOnce. Для приложения ClickOnce редактора workflow-процессов требуется 64-разрядная совместимая операционная система.
> * Для предварительного просмотра PDF-файлов рекомендуется использовать современные браузеры, такие как Microsoft Edge (последней общедоступной версии) в Windows 10 или Google Chrome (последней общедоступной версии) в Windows 10, Windows 8.1, Windows 8, Windows 7 или на планшете Google Nexus 10.
>   Требования к сети
> * Приложение Dynamics 365 Talent предназначено для сетей с задержкой не более 250-300 мс. Это задержка от клиента браузера до центра данных Microsoft Azure, на котором размещено приложение Talent. Рекомендуется проверить задержку в сети на сайте [www.azurespeed.com](https://www.azurespeed.com "Проверка задержки для Azure").
> * Требования к пропускной способности для Talent зависят от конкретного сценария реализации. В большинстве типичных сценариев требуется пропускная способность более 50 Кбайт в секунду (КБ/с).
> 
> [!WARNING]
> Не вычисляйте требования к пропускной способности из местоположения клиента путем умножения числа пользователей на минимальные требования к пропускной способности. Параллельное использование для конкретного местоположения очень сложно рассчитать. Клиентам, которых беспокоят требования к пропускной способности, следует использовать пробную версию Talent.

## <a name="supported-microsoft-office-applications"></a>Поддерживаемые приложения Microsoft Office

* Для запуска надстроек Microsoft Excel и Word должен быть установлен Microsoft Office 2016 для Windows или Mac. Дополнительные сведения о требованиях к версии см. в разделе [Устранение неполадок при интеграции Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "Устранение неполадок интеграции с Office").
* Для просмотра документов, созданных с помощью функции экспорта в Excel или экспорта в Word должен быть установлен пакет Microsoft Office 2007 или более поздняя версия.

## <a name="regional-availability-languages-and-localization"></a>Региональная доступность, языки и локализация

Можно загрузить PDF-файл для стран, регионов и языков, которые поддерживаются в Talent, из [международной доступности Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability). 

> [!NOTE]
> Хотя интерфейса пользователя локализован на другие языки, все пользовательские данные хранятся на том языке, на котором они были введены. Можно создавать сообщения и шаблоны на других языках, но на данный момент такие данные, как сведения о планировании, доступны только на английском языке.

Если вы являетесь разработчиком, заинтересованным в создании настроек, связанных со страной или регионом, или в создании решения для страны или региона, которые в настоящее время не поддерживаются корпорацией Майкрософт, см. раздел [Глобализация](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).

