---
title: Требования к системе
description: В этой статье описаны требования для Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 52ef0176926fd6c5c5d2bc852080dde5273d05d0f2edd20e091d97c71e503dce
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761100"
---
# <a name="system-requirements"></a>Требования к системе

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описаны требования для Microsoft Dynamics 365 Human Resources. Кроме того, в ней описываются страны и регионы, в которых доступно Human Resources, а также сведения о языках и локализации для данных Human Resources.

## <a name="supported-web-browsers"></a>Поддерживаемые веб-браузеры

Human Resources может выполняться в любом веб-браузере, который работает в указанных операционных системах: 

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
> * Human Resources предназначено для сетей с задержкой не более 250-300 мс. Это задержка от клиента браузера до центра данных Microsoft Azure, на котором размещено Human Resources. Рекомендуется проверить задержку в сети на сайте [www.azurespeed.com](https://www.azurespeed.com "Проверка задержки для Azure").
> * Требования к пропускной способности для Human Resources зависят от конкретного сценария реализации. В большинстве типичных сценариев требуется пропускная способность более 50 Кбайт в секунду (КБ/с).
> 
> [!WARNING]
> Не вычисляйте требования к пропускной способности из местоположения клиента путем умножения числа пользователей на минимальные требования к пропускной способности. Параллельное использование для конкретного местоположения очень сложно рассчитать. Клиентам, которых беспокоят требования к пропускной способности, следует использовать пробную версию Human Resources.

## <a name="supported-microsoft-office-applications"></a>Поддерживаемые приложения Microsoft Office

* Для запуска надстроек Microsoft Excel и Word должен быть установлен Microsoft Office 2016 для Windows или Mac. Дополнительные сведения о требованиях к версии см. в разделе [Устранение неполадок при интеграции Office](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Устранение неполадок интеграции с Office").
* Для просмотра документов, созданных с помощью функции экспорта в Excel или экспорта в Word должен быть установлен пакет Microsoft Office 2007 или более поздняя версия.

## <a name="regional-availability-languages-and-localization"></a>Региональная доступность, языки и локализация

Можно загрузить PDF-файл для стран, регионов и языков, которые поддерживаются в Human Resources, из [международной доступности Microsoft Dynamics 365](/dynamics365/get-started/availability). 

> [!NOTE]
> Хотя интерфейса пользователя локализован на другие языки, все пользовательские данные хранятся на том языке, на котором они были введены. Можно создавать сообщения и шаблоны на других языках, но на данный момент такие данные, как сведения о планировании, доступны только на английском языке.

Если вы являетесь разработчиком, заинтересованным в создании настроек, связанных со страной или регионом, или в создании решения для страны или региона, которые в настоящее время не поддерживаются корпорацией Майкрософт, см. раздел [Глобализация](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).


[!INCLUDE[footer-include](../includes/footer-banner.md)]