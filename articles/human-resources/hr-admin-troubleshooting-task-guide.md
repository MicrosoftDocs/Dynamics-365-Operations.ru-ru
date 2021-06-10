---
title: Сохранение проводников по задачам в LCS и их воспроизведение
description: В этой статье объясняется, как сохранять руководства по задачам в Microsoft Dynamics Lifecycle Services (LCS) и затем воспроизводить их.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a18bb14ba8c3c926065c97b0ee26c38ee86ded2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053283"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Сохранение проводников по задачам в LCS и их воспроизведение

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

    ![Сохраните файл в Lifecycle Services.](media/task-guides.png)

12. Выберите библиотеку BMP и узел, в который требуется сохранить запись задачи.

Выполните следующие действия, чтобы воспроизвести руководство по задаче из LCS.

1. Запустите регистратор задач.
2. Выберите **Открыть из LCS**.
3. Выберите библиотеку и узел BPM, в которых сохранено руководство по задаче.
4. Откройте руководство по задаче.


[!INCLUDE[footer-include](../includes/footer-banner.md)]