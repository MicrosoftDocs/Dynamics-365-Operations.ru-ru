---
title: Сохранение проводников по задачам в LCS и их воспроизведение
description: В этом разделе объясняется, как сохранять руководства по задачам в Microsoft Dynamics Lifecycle Services (LCS) и затем воспроизводить их.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 54251aed1a54f626e5cd6cbd983e3eb4589a02e8
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068367"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Сохранение проводников по задачам в LCS и их воспроизведение


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Сведения среды** 

Microsoft Dynamics 365 Human Resources, который был развернут с помощью Microsoft Dynamics Lifecycle Services (LCS)

**Расход**

Клиент хочет сохранить новые записи задач в своем проекте LCS и затем воспроизводить сохраненные руководства по задачам.

**Приказ**

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

    ![Сохраните в Lifecycle Services.](media/task-guides.png)

12. Выберите библиотеку BMP и узел, в который требуется сохранить запись задачи.

Выполните следующие действия, чтобы воспроизвести руководство по задаче из LCS.

1. Запустите регистратор задач.
2. Выберите **Открыть из LCS**.
3. Выберите библиотеку и узел BPM, в которых сохранено руководство по задаче.
4. Откройте руководство по задаче.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
