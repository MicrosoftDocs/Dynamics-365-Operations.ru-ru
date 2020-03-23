---
title: Настройка категорий счетов ГК
description: В этой теме описывается, как настроить категории счетов ГК в Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8e2ba1d900f5d87a76fa93bf53f2970320e7d84c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186011"
---
# <a name="set-up-main-account-categories"></a>Настройка категорий счетов ГК

[!include [task guide banner](../../includes/task-guide-banner.md)]

В этой теме описывается, как настроить категории счетов ГК. Категории счетов ГК используются для отчетов по умолчанию в финансовой отчетности и в Power BI. Категории счетов ГК, созданные по умолчанию, могут быть переименованы, но не могут быть удалены. Дополнительные категории счетов можно создавать и использовать для отчетности и анализа. В этой теме используется демонстрационная компания USMF.

## <a name="create-a-main-account-category"></a>Создание категории счета ГК
1. В области перехода выберите **Модули > Главная книга > План счетов > Счета > Категории счета ГК**.
2. Выберите **Создать**.
3. В поле **Категория счета ГК** введите уникальное имя.
4. В поле **Описание** введите описание категории счета ГК.
5. В поле **Тип счета ГК** выберите тип счета ГК, который будет связан с категорией.

## <a name="link-main-accounts-to-account-category"></a>Связывание счетов ГК с категорией счета
1. Щелкните **Связать счета ГК**.
2. В списке выберите счета ГК для назначения категории счетов ГК, установив флажки в столбце **Связано**. При назначении счетов ГК для категории счета ГК суммируются сальдо счетов, когда эта категория используется для финансовой отчетности и анализа.  
3. Выберите или отмените выбор параметра **Связано**, чтобы выбрать счета ГК.
4. Нажмите **ОК**.
5. Выберите **Да**.