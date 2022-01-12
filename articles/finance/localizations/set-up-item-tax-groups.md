---
title: Настройка налоговых групп номенклатур
description: В этой теме описывается, как настроить налоговые группы номенклатур в службе расчета налогов.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 88dd8e2fd9d4d4e5172dcc7b1bd27a70a2f59f03
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883875"
---
# <a name="set-up-item-tax-groups"></a>Настройка налоговых групп номенклатур

[!include [banner](../includes/banner.md)]

В этой теме описывается, как настроить налоговые группы номенклатур в службе расчета налогов. Здесь также объясняется порядок настройки матрицы правил применимости налоговой группы номенклатур и настройки строк в матрице.

Концепция налоговых групп номенклатур в службе расчета налогов напоминает концепцию налоговых групп номенклатур в Microsoft Dynamics 365 Finance. Они являются группами налоговых кодов. Для определения налоговых кодов служба расчета налога использует пересечение налоговой группы и налоговой группы номенклатур.

> [!IMPORTANT]
> Настройка налоговых групп номенклатур в службе расчета налогов не зависит от юридического лица. Эту настройку можно выполнить в Regulatory Configuration Service (RCS) только один раз. При включении службы расчета налогов в Finance налоговые группы номенклатур автоматически синхронизируются для выбранного юридического лица.

## <a name="set-up-an-item-tax-group"></a>Настройка налоговой группы номенклатур 

Чтобы настроить налоговую группу номенклатур, выполните следующие действия.

1. Выполните вход в [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).
2. Перейдите в раздел **Рабочие области** \> **Функции глобализации** \> **Расчет налога**.
3. Выберите функцию и версию, которые необходимо настроить, затем выберите **Изменить**.
4. На вкладке **Общие** выберите **Версия конфигурации**.
5. На вкладке **Налоговая группа номенклатур** выберите **Управление столбцами**. Если налоговая группа номенклатур настраивается в первый раз, поля в диалоговом окне **Управление столбцами** автоматически настраиваются.
6. В списке слева разверните узел **Строки** и установите флажок для **Налоговая группа номенклатур**.

    ![Налоговая группа номенклатур, выбранная в узле строк в диалоговом окне управления столбцами.](media/select-item-tax-group.png)

7. Выберите кнопку со стрелкой вправо, чтобы добавить пункт **Налоговая группа номенклатур** в список **Выбранные столбцы** справа.

    ![Налоговая группа номенклатур добавлена в список выбранных столбцов.](media/add-item-tax-group.png)

8. Нажмите **ОК**.

## <a name="configure-an-item-tax-group"></a>Настройка налоговой группы номенклатур

После настройки налоговой группы ном номенклатур создается матрица правил применимости. Для настройки налоговой группы номенклатур можно добавить строки в матрицу.

1. На вкладке **Налоговая группа номенклатур** выберите **Добавить**.
2. В поле **Налоговая группа номенклатур** введите имя налоговой группы номенклатур.

    > [!IMPORTANT]
    > Рекомендуется ограничить имя налоговой группы номенклатур 10 символами. Это имя синхронизируется с Finance, в котором имеется ограничение 10 символов для названий налоговых групп номенклатур.

3. В поле **Налоговые коды** установите флажок для каждого налогового кода, который необходимо включить в налоговую группу номенклатур. В одну налоговую группу номенклатур можно включить несколько налоговых кодов.

    ![Несколько налоговых кодов выбрано в поле налоговых кодов.](media/multiple-tax-codes-selection.png)

4. Повторите шаги 1–3, чтобы добавить другие налоговые группы номенклатур.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]