---
title: Сохранение проводников по задачам в LCS и их воспроизведение
description: В этой статье объясняется, как сохранять руководства по задачам в Microsoft Dynamics Lifecycle Services (LCS) и затем воспроизводить их.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b55937c0867117809471f50f1987f7bf12a4b25d
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010406"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Сохранение проводников по задачам в LCS и их воспроизведение

**Сведения среды** 

Microsoft Dynamics 365 Human Resources, который был развернут с помощью Microsoft Dynamics Lifecycle Services (LCS)

**Расход**

Клиент хочет сохранить новые записи задач в своем проекте LCS и затем воспроизводить сохраненные руководства по задачам.

**Разрешение**

Выполните эти действия для сохранения записей задач в LCS.

1. Выполните вход в LCS, затем выберите проект.
2. Выберите плитку **Средство моделирования бизнес-процессов**.
3. Просмотрите эту страницу в обновленном средстве моделирования бизнес-процессов.
4. Выберите библиотеку, затем выберите **Копировать**.
5. Введите имя для модели средства моделирования бизнес-процессов (BPM).
6. Выполните вход в Human Resources из LCS.
7. В поле **Поиск** введите **справка**. Открывается справка Lifecycle Services.
8. Выберите кнопку **Обновить** для конфигурации справки Lifecycle Services.

    Должна появиться ваша новая библиотека BPM, и она должна быть активной.

9. Закройте страницу.
10. Создайте запись задачи.
11. После завершения выберите **Сохранить файл в Lifecycle Services**.

    ![Сохраните файл в Lifecycle Services.](media/task-guides.png)

12. Выберите библиотеку BMP и узел, в который требуется сохранить запись задачи.

Выполните следующие действия, чтобы воспроизвести руководство по задаче из LCS.

1. Запустите регистратор задач.
2. Выберите **Открыть из LCS**.
3. Выберите библиотеку и узел BPM, в которых сохранено руководство по задаче.
4. Откройте руководство по задаче.