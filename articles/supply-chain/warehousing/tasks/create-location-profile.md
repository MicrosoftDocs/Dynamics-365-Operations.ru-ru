---
title: Создание профиля ячейки
description: В этом разделе описывается, как создать профиль местонахождения в Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46aa1001c21ae39c158062444303ca02c0f41a45
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866987"
---
# <a name="create-a-location-profile"></a>Создание профиля ячейки

[!include [task guide banner](../../includes/task-guide-banner.md)]

В этом разделе описывается, как создать профиль местонахождения в Dynamics 365 for Finance and Operations. Каждое местоположение склада должно иметь связанный с ним профиль местоположения, описывающий свойства местоположения, например, допускает ли местоположение смешанные номенклатуры. В этой процедуре мы создадим профиль для местоположения, который не требует управления грузоместом. Мы разрешим смешанные номенклатуры и смешанные состояния запасов, а также разрешим цикличный подсчет. Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.


1. В области перехода выберите **Модули > Управление складом > Настройка > Склад > Профили местонахождения**.
2. Выберите **Создать**.
3. В поле **Код профиля местонахождения** введите значение.
4. В поле **Имя** введите значение.
5. В поле **Формат местонахождения** введите или выберите значение.
6. В поле **Тип местоположения** введите или выберите значение.
7. В поле **Код профиля управления доком** введите или выберите значение.
8. Выберите значение **Да** в поле **Разрешить смешанные номенклатуры**.
9. Выберите значение **Да** в поле **Разрешить смешанные статусы запасов**.
10. Выберите **Да** в поле **Разрешить цикличный подсчет**.
11. Нажмите **Сохранить**.

