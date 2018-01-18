---
title: "Требования к системе и политика обновления Dynamics 365 for Talent"
description: "В этой теме перечислены требования к системе для Dynamics 365 for Talent. Также рассматривается политика обновления."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-talent
ms.technology: 
ms.search.form: Talent, update policy, requirements, system requirements
audience: Application User, IT Pro
ms.reviewer: rschloma
ms.search.scope: Operations, Core
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7bcc8464d34c35423e86c963c6b493fc09db4472
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="microsoft-dynamics-365-for-talent-system-requirements-and-update-policy"></a>Требования к системе и политика обновления Microsoft Dynamics 365 for Talent

[!include[banner](includes/banner.md)]


В этой теме перечислены требования к системе для Microsoft Dynamics 365 for Talent. Также рассматривается политика обновления.

## <a name="supported-web-browsers"></a>Поддерживаемые веб-браузеры

Веб-приложение Microsoft Dynamics 365 for Talent может выполняться в любом веб-браузере, который работает в указанных операционных системах: 

*   Microsoft Edge (последняя публично доступная версия) в Windows 10
*   Internet Explorer 11 в Windows 10, Windows 8.1 или Windows 7
*   Google Chrome (последняя публично доступная версия) в Windows 10, Windows 8.1, Windows 8, Windows 7 или на планшете Google Nexus 10
*   Apple Safari (последняя публично доступная версия) в Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) или 10.12 (Sierra) или Apple iPad

Чтобы найти последний выпуск для каждого веб-браузера, перейдите на веб-сайт производителя программного обеспечения. 

> [!NOTE]
> * Для захвата изображений, создаваемых в регистраторе задач, и включения их в документы Microsoft Word должно быть установлено расширение Chrome. 
> * Редактор workflow-процессов запускается в виде приложения ClickOnce. Только Microsoft Edge и Internet Explorer (на поддерживаемой версии Microsoft Windows) поддерживают приложение ClickOnce. Для приложения ClickOnce редактора workflow-процессов требуется 64-разрядная совместимая операционная система.
> * Для предварительного просмотра PDF-файлов рекомендуется использовать современные браузеры, такие как Microsoft Edge (последней общедоступной версии) в Windows 10 или Google Chrome (последней общедоступной версии) в Windows 10, Windows 8.1, Windows 8, Windows 7 или на планшете Google Nexus 10.
Требования к сети
> * Система Dynamics 365 for Talent предназначена для сетей с задержкой 250-300 миллисекунд (мс) и менее. Это задержка от клиента браузера до центра данных Microsoft Azure, на котором размещена система Dynamics 365 for Talent. Рекомендуется проверить задержку в сети на сайте [www.azurespeed.com] (http://www.azurespeed.com "Azure Latency Test").
> * Требования к пропускной способности для Dynamics 365 for Talent зависят от конкретного сценария. В большинстве типичных сценариев требуется пропускная способность более 50 Кбайт в секунду (КБ/с).

> [!WARNING]
> Не вычисляйте требования к пропускной способности из местоположения клиента путем умножения числа пользователей на минимальные требования к пропускной способности. Параллельное использование для конкретного местоположения очень сложно рассчитать. Клиентам, которых беспокоят требования к пропускной способности, следует использовать пробную версию Dynamics 365 for Talent.

## <a name="supported-microsoft-office-applications"></a>Поддерживаемые приложения Microsoft Office

*   Для запуска надстроек Microsoft Excel и Word должен быть установлен Microsoft Office 2016 для Windows или Mac. Дополнительные сведения о требованиях к версии см. разделе [Устранение неполадок интеграции с Office] (../dev-itpro/office-integration/office-integration-troubleshooting.md "Устранение неполадок интеграции с Office").
*   Для просмотра документов, созданных с помощью функции экспорта в Excel или экспорта в Word должен быть установлен пакет Microsoft Office 2007 или более поздняя версия.

## <a name="update-policy"></a>Политика обновления

Microsoft Dynamics 365 for Talent обслуживается как облачная система. Dynamics 365 for Talent постоянно обновляется, и обновления автоматически применяются корпорацией Майкрософт.

Обновления выпускаются регулярно и применяются ко всем средам.  Dynamics 365 for Talent поддерживается в соответствии с [политикой жизненного цикла поддержки Майкрософт] (https://support.microsoft.com/ru-ru/gp/lifecycle#gp/OSSLpolicy "Политика жизненного цикла поддержки Майкрософт"), которая обеспечивает единообразную и предсказуемую поддержку продукта.

