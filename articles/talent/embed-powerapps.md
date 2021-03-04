---
title: Внедрение приложений Power Apps в Dynamics 365 Human Resources
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462311"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a>Внедрение приложений Power Apps в Dynamics 365 Human Resources

**Выдать**

Пункт меню **Power Apps** исчез из модуля **Администрирование системы**.

**Причина**

Дизайн пользовательского интерфейса был изменен, и Microsoft Power Apps теперь включены в стандартную модуль персонализации.

**Приказ**

Был изменен способ внедрения Power Apps. Теперь Power Apps добавляются с помощью модели персонализации. Можно добавить Power Apps почти на все страницы Microsoft Dynamics 365 Talent.

Информацию о том, как внедрить приложения Power Apps в Talent, см. раздел [Внедрение приложений Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Любой клиент Power Apps, который внедрял приложения перед изменением, должен был обновиться до новой модели.

Кнопка **Power Apps** находится в правом верхнем углу почти каждой страницы в Talent. Эту кнопку можно использовать для вставки приложений.

Рассмотрим пример:

1. Выберите **Управление персоналом \> Ссылки \> Работники \> Сотрудники**.
2. Выберите кнопку **Power Apps**, а затем выберите **Добавить приложение из Power Apps**.

    ![Кнопка Power Apps](media/png.png)

3. Заполните поля в диалоговом окне **Добавление приложения из Power Apps**.

    ![Диалоговое окно добавления приложения из Power Apps](media/insert-powerapp.png)

Можно также выполнить следующие действия.

1. В области действий на странице на вкладке **Параметры** в группе **Персонализация** выберите **Персонализировать эту страницу**.

    ![Настройка группы на вкладке "Параметры"](media/options.png)

    Открывается панель инструментов персонализации.

2. На панели инструментов выберите **Добавить приложение из Power Apps**.

    ![Добавьте приложение из Power Apps с помощью панели инструментов персонализации](media/powerapp-bar.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]