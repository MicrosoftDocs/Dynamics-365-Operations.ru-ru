---
title: Удаленные или устаревшие функции Dynamics 365 Finance
description: В этом разделе описываются возможности, который удалены или которые планируется удалить из Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ec13076e6a05c3402af566487f7921f6971da215
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127985"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Удаленные или устаревшие функции Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

В этом разделе описываются возможности, который удалены или которые планируется удалить из Dynamics 365 Finance.

- *Удаленная* функция больше недоступна в продукте.
- *Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.

Этот список поможет вам учитывать эти удаления и устаревания при своем собственном планировании. 

> [!NOTE]
> Подробные сведения об объектах в приложениях Finance and Operations можно найти в документе [Технический справочник по отчетам](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Можно сравнить различные версии этих отчетов, чтобы получить сведения об объектах, которые были изменены или были исключены в каждой версии приложений Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.12

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Польский отчеты SSRS: Регистр НДС по продажам, Регистр НДС по покупкам, сводный отчет ЕС по НДС – Справочник по функциям PL-00014

|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Юридически не требуется.  |
| **Заменена другой функцией?**   | Да (формат Excel для стандартного файла аудита с декларацией НДС — JPK_VDEK) |
| **Затрагиваемые области продукта**         | Приложение |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: 1 июля 2021 г. планируется больше не поддерживать отчеты SSRS: **Регистр НДС по продажам, Регистр НДС по покупкам, сводный отчет ЕС по НДС — справочник по функциямPL-00014**. Вместо этого будет представлен пример формата Excel для стандартного файла аудита с декларацией НДС (JPK_VDEK). |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.7

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Диалоговое окно "запрос на изменение бизнес-правила" больше не включает раскрывающийся список выбора пользователя
|   |  |
|------------|--------------------|
| **Причина устаревания/удаления** | Изменение функции с выбором группы счетов.  |
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Рабочий процесс |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: на 1 декабря 2020 г. корпорация Майкрософт не планирует поддерживать настройку китайских типов ваучеров без выбора групп счетов. Более подробные сведения о новом дизайне можно найти в разделе [Что нового в 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Предыдущие объявления об удаленных или устаревших функциях
Для получения дополнительных сведений о функциях, которые были удалены или устарели в предыдущих выпусках, см [Удаленные или устаревшие функции в предыдущих выпусках](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).