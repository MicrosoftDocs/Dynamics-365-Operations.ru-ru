---
title: Изменение или переназначение календаря книги учета
description: В этой статье описывается, как изменить календарь, назначенный книге учета в данный момент, и как назначить новый календарь книге учета.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 751954e0dc5f682b99ab7fe349cd505dc9da7858
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848616"
---
# <a name="change-or-reassign-a-ledger-calendar"></a>Изменение или переназначение календаря книги учета

[!include [banner](../includes/banner.md)]

В этой статье описывается, как изменить календарь, назначенный книге учета в данный момент, и как назначить новый календарь книге учета.

## <a name="issue"></a>Проблема

Иногда компании должны либо изменить существующий календарь, назначенный книге учета, либо назначить новый календарь.

## <a name="resolution"></a>Решение

Существует два сценария изменения или переназначения календаря книги учета. Первый сценарий предполагает изменение существующего календаря, который уже назначен книге учета. Второй сценарий предполагает создание нового календаря и его назначение книге учета. Оба изменения можно выполнить в любое время, даже после разноски проводок в книгу учета.

### <a name="change-an-existing-fiscal-calendar"></a>Изменение существующего финансового календаря

Чтобы изменить существующий календарь, назначенный книге учета, перейдите в раздел **Главная книга \> Настройка книги учета \> Книга учета** и перейдите по ссылке на финансовый календарь, чтобы открыть страницу **Календари книги учета**.

Есть ограничения на изменения, которые могут быть внесены в календарь. Например, можно изменить даты начала и окончания *периодов* в году, но невозможно изменить даты начала и окончания *года* в календаре.

Чтобы изменить периоды в году, выберите соответствующий календарь и год. Во-первых, нажмите кнопку **Удалить период**, чтобы удалить некоторые или все существующие операционные периоды. Можно удалить все операционные периоды, кроме первого. Затем нажмите кнопку **Разделить период**, чтобы разделить оставшийся период или периоды на новые периоды, введя соответствующую дату начала следующего периода.

После изменения периодов в календаре необходимо запустить процесс **Пересчет периодов ГК** в каждом юридическом лице (компании), которой назначен календарь. Хотя вы не получаете предупреждение с напоминанием о необходимости выполнить этот шаг, процесс пересчета требуется для обновления периода, назначенного каждой разнесенной проводке в главной книге. Для запуска процесса пересчета выберите **Пересчет периодов ГК** на странице **Настройка книги учета** в каждой компании.

Если процесс пересчета не выполнить, сальдо проводок в пробном балансе или финансовых отчетах могут быть неправильно включены в периоды. В этом случае вы можете исправить сальдо в любое время, запустив процесс пересчета.

### <a name="assign-a-new-fiscal-calendar"></a>Назначение нового финансового календаря

Чтобы назначить новый финансовый календарь, перейдите в раздел **Главная книга \> Настройка книги учета \> Книга учета** и выберите **Правка**, чтобы перевести страницу **Книга учета** в режим редактирования. Затем в поле **Финансовый календарь** выберите новый финансовый календарь.

После изменения финансового календаря для книги учета необходимо запустить процесс **Пересчет периодов ГК**. При назначении нового финансового календаря книге учета вы получите напоминание о необходимости выполнить этот шаг. Хотя из сообщения вам может показаться, что процесс пересчета является необязательным, это не так. Он необходим для обновления периода, назначенного каждой разнесенной проводке в главной книге. Для запуска процесса пересчета выберите **Пересчет периодов ГК** на странице **Настройка книги учета**.

Если процесс пересчета не выполнить, сальдо проводок в пробном балансе или финансовых отчетах могут быть неправильно включены в периоды. В этом случае вы можете исправить сальдо в любое время, запустив процесс пересчета.
