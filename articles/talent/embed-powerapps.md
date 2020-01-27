---
title: Внедрение приложений Power Apps в Dynamics 365 - Core HR
description: В этом разделе описан порядок решения проблемы, когда элемент меню Microsoft Power Apps исчезает из модуля "Администрирование системы".
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b1dd1756be349d85af8e6d7159623a2a95e75526
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898720"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a>Внедрение приложений Power Apps в Dynamics 365 - Core HR

**Выдать**

Пункт меню **Power Apps** исчез из модуля **Администрирование системы**.

**Причина**

Дизайн пользовательского интерфейса был изменен, и Microsoft Power Apps теперь включены в стандартную модуль персонализации.

**Приказ**

Был изменен способ внедрения Power Apps. Теперь Power Apps добавляются с помощью модели персонализации. Можно добавить Power Apps почти на все страницы Microsoft Dynamics 365 Talent.

Информацию о том, как внедрить приложения Power Apps в Talent, см. раздел [Внедрение приложений Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Любой клиент Power Apps, который внедрял приложения перед изменением, должен был обновиться до новой модели.

Кнопка **Power Apps** находится в правом верхнем углу почти каждой страницы в Talent. Эту кнопку можно использовать для вставки Power Apps.

Рассмотрим пример:

1. Выберите **Управление персоналом \> Ссылки \> Работники \> Сотрудники**.
2. Выберите кнопку **Power Apps**, затем выберите пункт **Вставить PowerApp**.

    ![Кнопка Power Apps](media/png.png)

3. Заполните поля в диалоговом окне **Вставить PowerApp**.

    ![Диалоговое окно "Вставить PowerApp"](media/insert-powerapp.png)

Можно также выполнить следующие действия.

1. В области действий на странице на вкладке **Параметры** в группе **Персонализация** выберите **Персонализировать эту форму**.

    ![Настройка группы на вкладке "Параметры"](media/options.png)

    Открывается панель инструментов персонализации.

2. На панели инструментов выберите **Вставить \> PowerApp**.

    ![Вставка приложения Power Apps с помощью панели инструментов персонализации](media/powerapp-bar.png)
