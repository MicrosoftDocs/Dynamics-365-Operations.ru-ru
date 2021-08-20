---
title: Regulatory Configuration Service (RCS) — Удаление среды RCS
description: В этой теме объясняется, как системный администратор Regulatory Configuration Service (RCS) может удалить среду RCS и соответствующие данные.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: f9073a14143423676f23f9bf8dc9c17dbae18a6c3ad0d2f6d1e33919fd9162bf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759827"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) — Удаление среды RCS

[!include [banner](../includes/banner.md)]

В этой теме объясняется, как системный администратор Regulatory Configuration Service (RCS) может удалить среду RCS и соответствующие данные.

Прежде чем вы сможете выполнить процедуру из данной темы, необходимо выполнить следующие предварительные требования:

- Пользователю должна быть назначена роль **Системный администратор** для среды RCS.
- Роли **Системный администратор** должна быть назначена роль **RCSDeleteEnvironmentDuty**.

## <a name="delete-an-rcs-environment"></a>Удаление среды RCS

1. Откройте RCS и выберите плитку **Электронная отчетность**.
2. В разделе **Связанные ссылки** выберите **Удалить среду RCS**.

    ![Ссылка на удаление среды RCS в разделе связанных ссылок.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. В появившемся диалоговом окне проверьте сообщения об области удаления среды.

    ![Сообщения в диалоговом окне "Удаление среды RCS".](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > Удаление среды RCS не может быть отменено.
    >
    > Операция удаляет выбранную среду RCS и все связанные с ней данные, включая возможности и конфигурации, хранящиеся в глобальном репозитории. Функции и конфигурации, которые используются совместно с другими организациями, будут отключены от общего доступа и удалены, если они не имеют зависимостей. Функции и конфигурации с зависимостями будут помечены как отключенные.

4. В предоставленном поле введите глобальный уникальный идентификатор (GUID) среды RCS для подтверждения того, что вы хотите ее удалить. GUID среды включен в сообщение об удалении.
5. Выберите **Удалить среду**.
    
Среда RCS и все соответствующие данные будут удалены.

> [!IMPORTANT]
> После удаления среды RCS восстановить данные невозможно. Новую среду RCS можно создать в любом доступном регионе RCS.
