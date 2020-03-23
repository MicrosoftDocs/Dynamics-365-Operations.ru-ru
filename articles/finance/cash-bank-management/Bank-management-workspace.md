---
title: Рабочая область управления банками
description: В этой теме содержится информация о рабочей области управления банками. В этой рабочей области отображаются сведения, которые связаны с банковскими счетами компании, представление сводки и страница аналитики. Представление сводки показывает сводные плитки, сведения о банковском счете, диаграмму сальдо и связанные данные. Страницы аналитики использует возможности Microsoft Power BI для отображения визуальных объектов, которые относятся к сальдо банковского счета.
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 20847ea4651b816fc95135ca03667ae297cde5be
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188495"
---
# <a name="bank-management-workspace"></a>Рабочая область управления банками

[!include [banner](../includes/banner.md)]

Рабочая область **Управление банками** содержит сведения, которые связаны с банковскими счетами компании. Эта рабочая область содержит представление **Сводка** и страницу **Аналитика**. Представление **Сводка** показывает сводные плитки, сведения о банковском счете, диаграмму сальдо и связанные данные. Страница **Аналитика** использует возможности Microsoft Power BI для отображения визуальных объектов, которые относятся к сальдо банковского счета.

## <a name="summary-view"></a>Представление "Сводка"

### <a name="summary"></a>Сводка

Плитки в разделе **Сводка** дают общий обзор банковских счетов и обеспечивают быстрый доступ к страницам, которые чаще всего используются. Сведения о банковской выверке относятся только к функциям расширенной банковской выверки. Сведения включается только для тех банковских счетов, для которых параметр **Расширенная банковская выверка** задан как **Да** на странице **Банковский счет**. В разделе **Сводка** можно импортировать электронные банковские файлы для банковских счетов во всех юридических лицах.

### <a name="bank-accounts"></a>Банковские счета

Каждый банковский счет юридического лица представлен карточкой в разделе **Банковский счет**. Отображается текущее сальдо и можно выполнить детализацию до проводок, которые составляют эту сумму в итоговом сальдо. Сумма **Проводка по промежуточному счету** также позволяет детализировать до проводок, которые составляют эту сводную сумму. Проводки по промежуточному счету — это ожидающие проводки, которые были разнесены с помощью функций промежуточной проводки, но еще не были очищены. Сумма **Ожидающее сальдо** — это текущее сальдо за вычетом промежуточных или ожидающих проводок.

Карта также показывает последнюю выверку банковского счета. Эта информация отображается, только если расширенная банковская выверка включена для банковского счета.

### <a name="balance"></a>Баланс

Диаграмма **Сальдо** отображает либо исторические сведения по сальдо для банковского счета, выбранного в разделе **Банковские счета**, либо сводку по историческим сведениям по сальдо для всех банковских счетов юридического лица. Эта информация доступна для различных периодов: текущая неделя, текущий месяц, текущий год, последние пять лет и все периоды (полная история банковского счета). 

При просмотре диаграммы **Сальдо** для одного банковского счета исторические данные по сальдо отображаются в валюте банковского счета. При просмотре диаграммы для всех банковских счетов юридического лица исторические данные по сальдо отображаются в валюте учета.

Сведения о последнем обновлении данных отображаются в верхней части диаграммы. Можно обновить данные по мере необходимости.

### <a name="related-information"></a>Связанные сведения

В разделе **Связанные сведения** можно открыть страницу **Общий журнал**, чтобы выполнить банковские переводы. Можно также быстро открыть страницы **Банковские проводки** и **Проводки по промежуточному счету**.

## <a name="analytics-view"></a>Представление аналитики

На странице **Аналитика** содержатся важные показатели банковских счетов в текущей компании. На странице доступны следующие возможности визуализации.

-   Обще банковское сальдо в валюте системы
-   Сальдо по юридическому лицу
-   Фактическое и прогнозируемое сальдо на сегодня в валюте банковского счета
-   Сальдо по банковскому счету
-   Сальдо по валютам

Можно просмотреть аналитики банка для всех компаний в рабочей области **Обзор кассы — все компании**.