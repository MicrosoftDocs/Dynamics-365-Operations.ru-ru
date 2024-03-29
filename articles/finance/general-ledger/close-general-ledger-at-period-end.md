---
title: Закрытие ГК в конце периода
description: В этой статье описаны задачи, которые обычно выполняются при закрытии периода для главной книги.
author: aprilolson
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42a5df1cd1a73462c93012b26f9b9b5c1631f2ce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878051"
---
# <a name="close-the-general-ledger-at-period-end"></a>Закрытие ГК в конце периода

[!include [banner](../includes/banner.md)]

В этой статье описаны задачи, которые обычно выполняются при закрытии периода для главной книги. 

В главной книге можно выполнять процедуры закрытия для периода или года. Процессы закрытия подготавливают систему к новому периоду. Чтобы подготовить систему к новому году, необходимо выполнить процесс закрытия на конец года. Каждая организация имеет разные процессы и шаги, выполняемые на конец периода. Ниже приведены некоторые необязательные шаги для окончания периода.

-   Завершите все задачи для всех других модулей, например Расчеты с поставщиками, Расчеты с клиентами и Запасы.
-   Проверьте, что все журналы разнесены.
-   Выполните переоценку в иностранной валюте для создания любых сумм внереализационной прибыли или убытков.
-   Сопоставьте проводки для каждого счета ГК.
-   Обработайте все требуемые распределения.
-   Вручную разнесите корректировки на конец периода.
-   Учтите в субкниге проводки и просмотрите отчет **Журнал ГК**.
-   Выполните консолидацию, используя консолидированную компанию или финансовую отчетность.
-   Создайте финансовые отчеты на конец периода с помощью финансовой отчетности.
-   Задайте для периодов ГК статус **Заблокировано**, чтобы было невозможно выполнить разноску. Также можно ограничить период определенной группой пользователей, пока выполняются действия на конец периода, для более эффективного управления. Не рекомендуется задавать для периодов статус **Закрытый на постоянной основе**, поскольку невозможно повторно открыть период, который был закрыт.

Рабочая область **закрытия финансового периода** может использоваться для организации и отслеживания задач, необходимых для различных процессов на конец периода. 


Дополнительные сведения см. в следующих темах:
- [Рабочая область закрытия финансового периода](financial-period-close-workspace.md) 
- [Закрытие на конец года](Year-end-close.md)  
- [Массовое закрытие финансовых периодов](tasks/mass-financial-period-close.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
