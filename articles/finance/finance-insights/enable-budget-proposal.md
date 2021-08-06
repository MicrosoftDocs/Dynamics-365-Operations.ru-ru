---
title: Включение предложений по бюджету (предварительная версия)
description: В этой теме объясняется, как включить функцию предложений по бюджету в финансовом анализе.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: d3fac4cbb80493c7cf94e3d9f4a4f544a749fb64
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638640"
---
# <a name="enable-budget-proposals-preview"></a>Включение предложений по бюджету (предварительная версия)

[!include [banner](../includes/banner.md)]

В этой теме объясняется, как включить функцию предложений по бюджету в финансовом анализе.

1. Используйте информацию со страницы среды в Microsoft Dynamics Lifecycle Services (LCS) для подключения к основному экземпляру Azure SQL для этой среды. Выполните следующую команду Transact-SQL (T-SQL), чтобы включить фокус-тестирования для среды песочницы. (Возможно, придется включить доступ для своего IP-адреса в LCS, прежде чем можно будет дистанционно подключиться к серверу Application Object Server \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Пропустите этот шаг, если используется версия 10.0.20 или более поздняя либо используется развертывание с помощью Service Fabric. Рабочая группа финансового анализа уже должна была включить доступ для вас. Если вы не видите эту функцию в рабочей области **Управления функциями** или у вас возникают проблемы при попытке ее включения, обратитесь по адресу <fiap@microsoft.com>.

2. Откройте рабочую область **Управление функциями** и выполните следующие действия:

    1. Выберите **Проверить наличие обновлений**.
    2. Выполните поиск **Предложение бюджета** и включите эту функцию.

3. Перейдите в раздел **Бюджетирование \> Настройка \> Базовое бюджетирование \> Предложение бюджета (предварительная версия)** и выберите **Включить функцию**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
