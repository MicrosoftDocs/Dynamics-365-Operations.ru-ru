---
title: Проверка конфигурации двойной записи в приложениях Finance and Operations и Dataverse
description: В этой теме объясняется, как можно определить, настроена ли двойная запись в приложениях Finance and Operations и в Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0a1da32713f3d4d19b4d343c5b67b416a6c4ffbb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566773"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Проверка конфигурации двойной записи в приложениях Finance and Operations и Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Dataverse. Конкретно, в ней объясняется, как можно определить, настроена ли двойная запись в приложениях Finance and Operations и в Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Проверка настройки двойной записи в приложении Finance and Operations

Чтобы определить, возникают ли ошибки, отображаемые при попытке сохранить строки для обновления, в результате двойной записи, сначала убедитесь, что двойная запись настроена.

+ Если у вас есть права администратора в приложении Finance and Operations, перейдите к пункту **Рабочие области \> Управление данными** и выберите плитку **Двойная запись**. Если отображаются сведения о связанных средах и список выполняемых сопоставлений таблиц, двойная запись настроена.

    ![Проверка подключения приложения Finance and Operations при наличии прав администратора](media/verify_fin_ops_1.png)

+ Если у вас нет прав администратора, вы получите сообщение об ошибке *Невозможно записать данные в объект \<entity name\>*. В примере на следующем рисунке невозможно создать строку клиента в приложении Finance and Operations, так как настроена двойная запись, но отсутствуют ссылочные данные группы клиентов и условий оплаты в Dataverse.

    ![Проверка подключения приложения Finance and Operations при отсутствии прав администратора](media/verify_fin_ops_2.png)

Сведения об устранении проблем при создании данных в приложениях Finance and Operations см. в разделе [Устранение проблем с синхронизацией в режиме реального времени](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Проверка настройки двойной записи в Dataverse

Если при создании данных вы видите столбец **Компания** на страницах в Dataverse, двойная запись настроена.

![Проверка подключения Dataverse](media/verify_cds.png)

Сведения об устранении проблем при создании данных в Dataverse см. в разделе [Устранение проблем с синхронизацией в режиме реального времени](dual-write-troubleshooting-live-sync.md).

Сведения о том, как просмотреть подробные сведения об ошибке при возникновении каких-либо ошибок во время создания данных в Dataverse см. в разделе [Включение и просмотр журнала трассировки подключаемого модуля в Dataverse для просмотра подробных сведений об ошибке](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]