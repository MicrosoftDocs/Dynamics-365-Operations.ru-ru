---
title: Открытие шаблонов финансового журнала в Office
description: В этой статье описываются проблемы, которые могут возникнуть при создании настраиваемых финансовых журналов с помощью шаблона Microsoft Excel.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a29ab1cb2980ebfed6c6fa6409538bc802849156
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896357"
---
# <a name="open-financial-journal-templates-in-office"></a>Открытие шаблонов финансового журнала в Office

[!include [banner](../includes/banner.md)]

В этой статье описываются проблемы, которые могут возникнуть при создании настраиваемых финансовых журналов с помощью шаблона Microsoft Excel.

## <a name="symptom"></a>Симптом

Создан пользовательский шаблон Excel для финансовых журналов, но он не отображается в меню **Открыть строки в Excel**. Либо он отображается в меню, но при его выборе открывается другой шаблон.

## <a name="resolution"></a>Решение

Функция "Открыть в Excel" по умолчанию использует корневой источник данных (таблицу) текущей страницы, чтобы определить, какие шаблоны или информационные объекты Office отображаются в виде параметров в меню **Открыть в Excel**. Это не является идеальным поведением для финансовых журналов, поскольку финансовые журналы используют те же таблицы (LedgerJournalTable и LedgerJournalTrans), что и корневой источник данных многих других типов журналов.

Для финансовых журналов функция "Открыть строки в Excel" предназначена для отображения шаблонов, разработанных для журнала, в контексте которого в данный момент ведется работа, например общего журнала или журнала платежей. Например, шаблон, предназначенный для использования с журналом платежей поставщика, будет разработан таким образом, чтобы обязывать использовать основной счет в качестве счета поставщика.

Если требуется повысить уровень шаблона, чтобы он был доступен в меню **Открыть строки в Excel** и **Открыть в Excel**, простым выходом будет реализовать интерфейс **LedgerIJournalExcelTemplate** и расширить класс **DocuTemplateRegistrationBase**. Многие примеры этого подхода реализованы в системе. Одним из примеров, который можно использовать для справки, является интерфейс **LedgerDailyJournalExcelTemplate**, который был создан для общего журнала (или ежедневного журнала).

Если для шаблона реализован интерфейс **LedgerIJournalExcelTemplate**, в меню **Открыть строки в Excel** будут фильтроваться шаблоны по типу журнала и будут отображаться только шаблоны, доступные для этого журнала. Интерфейс также предоставляет метод проверки, гарантирующий, что шаблон невозможно открыть для журнала, если он не соответствует требованиям типа счета. Например, можно указать, что типом счета должен быть **Поставщик** или **Книга учета**.

Дополнительные сведения об этих функциях см. в разделе [Добавление шаблонов в меню открытия строк в Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).
