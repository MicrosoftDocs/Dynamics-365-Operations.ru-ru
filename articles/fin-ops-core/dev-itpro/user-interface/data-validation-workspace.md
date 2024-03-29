---
title: Рабочая область контрольного списка проверки данных
description: Рабочая область контрольного списка проверки данных позволяет отслеживать процессы проверки данных между компаниями, областями и людьми.
author: bking
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: bking
ms.assetid: ''
ms.search.form: DataValidationWorkspace
ms.openlocfilehash: fb8999815e96c0aa7d1a054073de77a382c14263
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272493"
---
# <a name="data-validation-checklist-workspace"></a>Рабочая область "Контрольный список проверки данных"

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Эта статья предоставляет обзор **Рабочей области контрольного списка проверки данных** и соответствующей конфигурации.

Рабочая область **Контрольный список проверки данных** позволяет отслеживать процессы проверки данных между компаниями, областями и людьми. Контрольный список можно использовать во время новой реализации, после обновления или после миграции. В зависимости от представления рабочей области **Контрольный список проверки данных** отображаются либо все задачи и статусы для проекта проверки данных, либо только задачи, которые назначены вам.

Необходимо сначала выбрать проект проверки данных в верхней части рабочей области. Все данные, которые отображаются в рабочей области, затем фильтруются по проекту проверки данных.

## <a name="summary-tiles"></a>Плитки сводки

Плитки **Сводка** предоставляют обзор процесса и содержат индикаторы, которые помогают следить за процессом проверки данных. Можно просмотреть все оставшиеся задачи, завершенные задачи, выполняющиеся задачи и неначатые задачи для процесса. Эти сведения отображаются для всех компаний, включенных в выбранный проект проверки данных.

## <a name="tasks-and-status-section"></a>Раздел задач и статуса

В разделе **Задачи и статус** отображается статус всего проекта проверки данных различными способами: статус по юридическому лицу, по области и по списку задач. Можно выбрать фильтр для просмотра статуса для конкретной компании. Каждая вкладка статуса дает детализацию как по проценту, который был завершен, так и по числу задач, которые остаются.

Последняя вкладка — для детального списка задач. В этом списке задач показан полный список задач. Вы можете фильтровать список задач несколькими способами. Щелкните **Изменить задачу**, чтобы изменить статус задачи или назначить задачу. Щелкните **Вложения** для просмотра вложений для задачи.

Имя задачи представляет собой гиперссылку на страницу, куда пользователь должен пойти, чтобы выполнить работу. Эту гиперссылку можно настроить с помощью поля **Имя пункта меню** при редактировании или создании задачи из формы **Настройка проекта проверки данных**.

Можно прикреплять файлы, примечания, изображения и URL-адреса к задаче с помощью действия **Вложения**. Например можно присоединить файл отчета, который был распечатан для задачи. Значок появляется в столбце **Вложение** для задачи, если вложение присутствует.

Параметр **Кем выполнено** будет автоматически заполнен после выполнения задачи именем работника, который выполнил задачу. Когда задача отмечена как завершенная, поле **Дата выполнения** автоматически обновляется до текущих даты и времени.

## <a name="configure-data-validation-project-page"></a>Страница настройки проекта проверки данных

Прежде чем можно будет использовать рабочую область **Контрольный список проверки данных** необходимо настроить процесс с помощью страницы **Настройка проекта проверки данных**. (Щелкните **Рабочие области** \> **Контрольный список проверки данных** \> **Настройка проекта проверки данных**.)

## <a name="task-areas"></a>Области задач

Вы используете зоны задач для того, чтобы группировать задачи проверки данных в логические зоны владения в пределах своей организации. Например, расчеты с поставщиками, Расчеты с клиентами, или главную книгу могли быть использованы как зоны задачи.

**Имя пункта меню** связано с работой по задаче и может быть использовано для того, чтобы перейти сразу к связанной странице по ссылке на задачу в рабочей области. Например, задача проверки данных для выполнения отчета **Сроки оплаты для расчетов с поставщиками** модуля "Расчеты с поставщиками" может быть связана со страницей **Отчет по срокам оплаты для расчетов с поставщиками**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
