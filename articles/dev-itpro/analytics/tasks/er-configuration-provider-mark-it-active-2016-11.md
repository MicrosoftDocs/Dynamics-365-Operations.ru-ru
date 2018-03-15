--- 
title: "Создание поставщика конфигурации и пометка его как активного для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь с ролью \"Системный администратор\" или \"Разработчик электронной отчетности\" может создать поставщика конфигурации для электронной отчетности."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 018aee917c13f576759ebd812d31cbc9d83e2d1a
ms.contentlocale: ru-ru
ms.lasthandoff: 02/23/2018

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a>Создание поставщика конфигурации и пометка его как активного для электронной отчетности (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать поставщика конфигурации для электронной отчетности. Конфигурация электронной отчетности будет ссылаться на поставщика как автора конфигурации. В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку поставщики конфигурации электронной отчетности используются всеми компаниями.


## <a name="create-a-provider"></a>Создание поставщика
1. Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".
2. Щелкните "Поставщики конфигурации".
3. Щелкните "Создать".
    * Запись поставщика имеет уникальные имя и URL-адрес. Проверьте содержимое этой страницы и пропустите эту процедуру, если запись для Litware, Inc. (`http://www.litware.com`).  
4. В поле "Имя" введите "Litware, Inc.".
    * Litware, Inc.  
5. В поле "Веб-адрес" введите `http://www.litware.com`.
6. Нажмите кнопку "Сохранить".
7. Закройте страницу.

## <a name="select-as-an-active-provider"></a>Выбор поставщика как активного
1. Выберите поставщика Litware, Inc.
2. Щелкните "Установить как активное".


