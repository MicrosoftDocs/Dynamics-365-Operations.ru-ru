---
title: Regulatory Configuration Service (RCS) — удаление среды RCS
description: В этой статье объясняется, как системный администратор Regulatory Configuration Service (RCS) может удалить среду RCS и связанные с ней данные.
author: kfend
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, System Admin
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
ms.openlocfilehash: bdcb6820ead72fce0f89bf80cc5e474cb3942724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277251"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) — удаление среды RCS

[!include [banner](../includes/banner.md)]

В этой статье объясняется, как системный администратор Regulatory Configuration Service (RCS) может удалить среду RCS и связанные с ней данные.

Чтобы можно было выполнить процедуру из данной статьи, необходимо выполнить следующие предварительные требования:

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
