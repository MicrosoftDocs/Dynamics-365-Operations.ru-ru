---
title: "Создайте workflow-процесс"
description: "В этом разделе объясняется, как создать workflow-процесс."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, UnifiedOperations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 138cf8d60f5a6e1ec1e46837a516e981c8ff4c19
ms.contentlocale: ru-ru
ms.lasthandoff: 06/13/2017

---

# <a name="create-a-workflow"></a>Создайте workflow-процесс

[!include[banner](../includes/banner.md)]


В этом разделе объясняется, как создать workflow-процесс.

<a name="open-the-workflow-editor"></a>Откройте редактор workflow-процесса
------------------------

Модуль Microsoft Dynamics 365 for Finance and Operations, в котором вы работаете, определяет типы workflow-процессов, которые можно создать. Выполните следующие действия, чтобы выбрать тип workflow-процесса для создания и открытия редактора workflow-процесса.

1.  Откройте модуль, для которой требуется создать новый workflow-процесс. Например, чтобы создать workflow-процесс для заявок на покупку, нажмите кнопку **Закупки и источники**.
2.  Щелкните **Настройка** &gt; **Workflow-процессы \[имя модуля\]**.
3.  На открывшейся странице списка в области операций щелкните **Создать**.
4.  На странице **Создать workflow-процесс** выберите тип создаваемого workflow-процесса, затем нажмите **Создать workflow-процесс**. Открывается редактор workflow-процессов. Теперь можно использовать следующие процедуры для разработки workflow-процесса.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Перетащите элементы workflow-процесса на холст
Зона **Элементы workflow-процесса** редактора workflow-процесса содержит элементы, которые могут быть добавлены к вашему workflow-процессу. Чтобы добавить элементы в workflow-процесс, перетащите их на холст.

## <a name="connect-the-elements"></a>Подключите элементы
Для того, чтобы подключить один элемент workflow-процесса к другому, наведите курсор на элемент, пока не появятся точки подключения. Щелкните точку подключения и перетащите ее к другому элементу. Не забудьте подключить все элементы.

## <a name="configure-the-properties-of-the-workflow"></a>Настроить свойства workflow-процесса
Следуйте этим действиям для настройки свойств для workflow-процесса.

1.  Щелкните холст, чтобы убедиться в том, что ни один элемент workflow-процесс не выбран.
2.  Щелкните **Свойства**, чтобы открыть страницу **Свойства** для workflow-процесса.
3.  Следуйте процедурам из раздела [Настроить свойства workflow-процесса](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>Настроить элементы документооборота
Настройте каждый элемент, который вы перетащили на холст. Сведения о конфигурировании каждого элемента workflow-процесса см. в следующих разделах:

-   [Настройка задачи вручную](configure-manual-task-workflow.md)
-   [Настройка автоматизированной задачи](configure-automated-task-workflow.md)
-   [Настройка процесса утверждения](configure-approval-process-workflow.md)
-   [Настройка стадии утверждения](configure-approval-step-workflow.md)
-   [Настройка принятия решений вручную](configure-manual-decision-workflow.md)
-   [Настройте зависимое решение](configure-conditional-decision-workflow.md)
-   [Настройте параллельное действие](configure-parallel-activity-workflow.md)
-   [Настройка параллельной ветви](configure-parallel-branch-workflow.md)
-   [Настройка документооборота элемента строки](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Разрешение любых ошибок или предупреждений
Область **Ошибки/предупреждения** в нижней части редактора workflow-процессов отображает сообщения, созданные для workflow-процесса. Чтобы найти элемент, в котором появилась ошибка или предупреждение, дважды щелкните ошибка или предупреждение. Необходимо разрешить все ошибки и предупреждения, прежде чем можно будет активировать workflow-процесс.

## <a name="save-and-activate-the-workflow"></a>Сохранить и активировать workflow-процесс
Когда вы готовы сохранить и активировать workflow-процесс, выполните следующие действия.

1.  Щелкните **Сохранить и закрыть**, чтобы закрыть редактор workflow-процессов и открыть страницу **Сохранение workflow-процесса**.
2.  Введите комментарии об изменениях, внесенных в workflow-процесс, затем нажмите **ОК**.
3.  Если все ошибки и предупреждения были устранены, открывается страница **Активировать workflow-процесс**. Выберите один из следующих вариантов:
    -   Чтобы активировать эту версию workflow-процесса, нажмите **Активировать новую версию**. Когда workflow-процесс станет активным, пользователи смогут представлять документы на обработку.
    -   Если вы не хотите активировать данную версию, нажмите **Не активировать новую версию**. workflow-процесс можно активировать позднее.






