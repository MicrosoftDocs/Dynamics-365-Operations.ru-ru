---
title: Внедрение приложений PowerApps в Core HR
description: В этом разделе описан порядок решения проблемы, когда элемент меню PowerApps исчезает из модуля "Администрирование системы".
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
ms.openlocfilehash: e3b20e1d0a873c32b8f6f5e28f786febf62db355
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518980"
---
# <a name="embed-powerapps-apps-in-core-hr"></a>Внедрение приложений PowerApps в Core HR

[!include [banner](includes/banner.md)]

**Расход**

Пункт меню **PowerApps** исчез из модуля **Администрирование системы**.

**Причина**

Дизайн пользовательского интерфейса был изменен, и Microsoft PowerApps теперь включены в стандартную модуль персонализации.

**Разрешение**

Был изменен способ внедрения приложений PowerApps. Теперь приложения PowerApps добавляются с помощью модели персонализации. Можно добавить приложения PowerApps почти на все страницы Microsoft Dynamics 365 for Talent.

Информацию о том, как внедрить приложения PowerApps в Talent, см. раздел [Внедрение приложений PowerApps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Любой клиент PowerApps, который внедрял приложения перед изменением, должен был обновиться до новой модели.

Кнопка **PowerApps** находится в правом верхнем углу почти каждой страницы в Talent. Эту кнопку можно использовать для вставки приложения PowerApps.

Рассмотрим пример:

1. Выберите **Управление персоналом \> Ссылки \> Работники \> Сотрудники**.
2. Выберите кнопку **PowerApps**, затем выберите пункт **Вставить PowerApp**.

    ![Кнопка PowerApps](media/png.png)

3. Заполните поля в диалоговом окне **Вставить PowerApp**.

    ![Диалоговое окно "Вставить PowerApp"](media/insert-powerapp.png)

Можно также выполнить следующие действия.

1. В области действий на странице на вкладке **Параметры** в группе **Персонализация** выберите **Персонализировать эту форму**.

    ![Настройка группы на вкладке "Параметры"](media/options.png)

    Открывается панель инструментов персонализации.

2. На панели инструментов выберите **Вставить \> PowerApp**.

    ![Вставка приложения PowerApps с помощью панели инструментов персонализации](media/powerapp-bar.png)
