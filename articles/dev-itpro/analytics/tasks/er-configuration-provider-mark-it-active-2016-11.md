---
title: Создание поставщиков конфигураций и пометка их как активных
description: В этой теме поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать поставщика конфигурации для электронной отчетности в Dynamics 365 for Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e02cd51478528db56a4f50b134fabf7f9e1dc8ea
ms.sourcegitcommit: a1354c6218b328d4d7dcc149d1339a7af10c48bf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "1723128"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Создание поставщиков конфигураций и пометка их как активных

[!include [task guide banner](../../includes/task-guide-banner.md)]

В этой теме поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать поставщика конфигурации для электронной отчетности в Dynamics 365 for Finance and Operations. Конфигурация электронной отчетности будет ссылаться на поставщика как автора конфигурации. В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку поставщики конфигурации электронной отчетности используются всеми компаниями.

## <a name="create-a-provider"></a>Создание поставщика
1. Перейдите в **область навигации** в верхнем левом углу и выберите **Администрирование организации**.
2. Перейдите в раздел **Рабочие области > Электронная отчетность**.
3. Перейдите в раздел **Связанные ссылки > Поставщики конфигурации**.
4. Выберите **Создать**.
    - Запись поставщика имеет уникальные имя и URL-адрес. Проверьте содержимое этой страницы и пропустите эту процедуру, если запись для Litware, Inc. (https://www.litware.com).  
5. В поле "Имя" введите `Litware, Inc.`.
6. В поле веб-адреса введите `https://www.litware.com`.
7. Нажмите **Сохранить**.
8. Закройте страницу.

## <a name="select-as-an-active-provider"></a>Выбор поставщика как активного
1. Выберите поставщика Litware, Inc.
2. Выберите **Установить активные**.

