---
title: Личные расходы в отчете о расходах
description: В этом разделе рассматриваются два метода обработки личных расходов сотрудника в Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6b6c505e7dc5e6544658b00d9f59e6062353608
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "344900"
---
# <a name="personal-expenses-on-an-expense-report"></a>Личные расходы в отчете о расходах

[!include [banner](../includes/banner.md)]

Во время командировок работники могут иногда расплачиваться за личные расходы по корпоративным кредитным картам. Если процедура для обработки личных расходов не определена, процесс утверждения отчетов о расходах может быть нарушен, когда работники представляют детализированные отчеты о расходах. 

В Microsoft Dynamics 365 for Finance and Operations есть два метода обработки личных расходов работника:

- **Оплачивается сотрудником** — организация не оплачивает личные расходы, которые отображаются в счете по корпоративной кредитной карте. Организация вместо этого создает отчет, в котором личные и корпоративные расходы, оплаченные по корпоративной кредитной карте, показаны вместе.
- **Оплачивается компанией** — организация оплачивает весь счет по корпоративной кредитной карте целиком, а затем дебетует личные расходы со счета работника.

Можно выбрать метод, который используется в вашей организации, на странице **Параметры управления расходами**.
