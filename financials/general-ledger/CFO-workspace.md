---
title: "Добавление финансовых аналитик в рабочую область финансового директора"
description: "В этой теме объясняется, как добавить финансовые аналитики в рабочую область финансового директора, чтобы их можно было использовать для отчетов по ГК и бюджету."
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: ru-ru
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Добавление финансовых аналитик в рабочую область финансового директора

[!include[banner](../includes/banner.md)]

В этой теме объясняется, как добавить финансовые аналитики в рабочую область финансового директора, чтобы их можно было использовать для отчетов по ГК и бюджету. Рабочая область финансового директора содержит вкладки **Обзор** и **Финансы**. Отчеты на этих двух вкладках обеспечиваются двумя измерениями: LedgerActivityMeasure и BudgetActivityMeasure. В Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, , обновление от июля 2017 г., существует связь между этими двумя измерениям и объектом DimensionCombinationEntity. Следовательно, можно выбрать аналитики.

1. В Finance and Operations на странице **Entity Store** обновите измерения **LedgerActivityMeasure** и **BudgetActivityMeasure**.
2. В Microsoft Visual Studio откройте обозреватель приложений и выполните поиск по слову **LedgerCFO**.
3. В разделе **Ресурсы** откройте **LedgerCFOWorkspacePBIX**.
4. Когда ресурс откроется в Microsoft Power BI Desktop выберите **Получить данные**, выберите **База данных SQL Server**, а затем выберите **Подключиться**.
5. Введите имя сервера и введите **AxDW** в качестве базы данных. Выберите **DirectQuery** и выберите **ОК**.
6. Найдите и выберите **LedgerActivityMeasure\_DimensionCombination**, а затем выберите **Загрузить**.

    > [!TIP]
    > В списке **Поля** переименуйте таблицу в **Финансовые аналитики**, чтобы ее было легко идентифицировать.

7. Выберите **Управление связями**, а затем выберите **Создать**.
8. В первом поле выберите **Действия ГК**, а затем выберите **LedgerDimension**.
9. Во втором поле выберите **LedgerActivityMeasure\_DimensionCombination** (или **Финансовые аналитики**, если вы переименовали таблицу). Выберите заголовок **DimensionCombinationRECID**.
10. В поле **Кратность** выберите **Многие к одному**.
11. Изменение значение в поле **Направление кросс-фильтра** на **Один**.
12. Выберите и **Активировать связь**, и **Предполагать целостность данных**, выберите **ОК**, а затем выберите **Закрыть**.

    [![Создание связи](./media/Create-relationship.png)](./media/Create-relationship.png)

13. В списке **Поля** вы должны видеть таблицу и доступные финансовые аналитики. Перетащите нужные финансовые аналитики на фильтры уровня отчета.
14. Сохраните изменения.
15. В репозитории прикладных объектов (AOT) щелкните свой проект правой кнопкой мыши и выберите **Синхронизировать**.
16. Соберите проект, а затем откройте приложение для просмотра результатов.

    [![Готовая рабочая область](./media/workspace.png)](./media/workspace.png)
