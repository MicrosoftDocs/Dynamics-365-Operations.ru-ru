---
title: Проверка настройки двойной записи в приложениях Finance and Operations и Common Data Service
description: В этой теме объясняется, как можно определить, настроена ли двойная запись в приложениях Finance and Operations и в Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997238"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>Проверка настройки двойной записи в приложениях Finance and Operations и Common Data Service

[!include [banner](../../includes/banner.md)]



Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Common Data Service. Конкретно, в ней объясняется, как можно определить, настроена ли двойная запись в приложениях Finance and Operations и в Common Data Service.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Проверка настройки двойной записи в приложении Finance and Operations

Чтобы определить, возникают ли ошибки, отображаемые при попытке сохранить записи для обновления, в результате двойной записи, сначала убедитесь, что двойная запись настроена.

+ Если у вас есть права администратора в приложении Finance and Operations, перейдите к пункту **Рабочие области \> Управление данными** и выберите плитку **Двойная запись**. Если отображаются сведения о связанных средах и список выполняемых сопоставлений объектов, двойная запись настроена.

    ![Проверка подключения приложения Finance and Operations при наличии прав администратора](media/verify_fin_ops_1.png)

+ Если у вас нет прав администратора, вы получите сообщение об ошибке *Невозможно записать данные в объект \<entity name\>*. В примере на следующем рисунке невозможно создать запись клиента в приложении Finance and Operations, так как настроена двойная запись, но отсутствуют ссылочные данные группы клиентов и условий оплаты в Common Data Service.

    ![Проверка подключения приложения Finance and Operations при отсутствии прав администратора](media/verify_fin_ops_2.png)

Сведения об устранении проблем при создании данных в приложениях Finance and Operations см. в разделе [Устранение проблем с синхронизацией в режиме реального времени](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>Проверка настройки двойной записи в Common Data Service

Если при создании данных вы видите поле **Компания** на страницах в Common Data Service, двойная запись настроена.

![Проверка подключения Common Data Service](media/verify_cds.png)

Сведения об устранении проблем при создании данных в Common Data Service см. в разделе [Устранение проблем с синхронизацией в режиме реального времени](dual-write-troubleshooting-live-sync.md).

Сведения о том, как просмотреть подробные сведения об ошибке при возникновении каких-либо ошибок во время создания данных в Common Data Service см. в разделе [Включение и просмотр журнала трассировки подключаемого модуля в Common Data Service для просмотра подробных сведений об ошибке](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).
