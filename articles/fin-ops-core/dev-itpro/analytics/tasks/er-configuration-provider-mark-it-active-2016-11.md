---
title: Создание поставщиков конфигураций и пометка их как активных
description: В этой теме поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать поставщика конфигурации для электронной отчетности.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5f238a492dbc3f9318b1bd1d3ea5657e92b33fb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142117"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Создание поставщиков конфигураций и пометка их как активных

[!include [banner](../../includes/banner.md)]

В этой теме поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать поставщика конфигурации для электронной отчетности. Конфигурация электронной отчетности будет ссылаться на поставщика как автора конфигурации. В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку поставщики конфигурации электронной отчетности используются всеми компаниями.

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

![Страница рабочей области электронной отчетности](../media/GER-Task-ActiveProvider-1.png)
