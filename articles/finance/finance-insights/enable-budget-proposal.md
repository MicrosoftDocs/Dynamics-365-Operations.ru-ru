---
title: Включение предложений по бюджету (предварительная версия)
description: В этой теме объясняется, как включить функцию предложений по бюджету в финансовом анализе.
author: ShivamPandey-msft
ms.date: 07/24/2020
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
ms.openlocfilehash: 7e90a1a2f2a8e7808f03ce9a6ee58c027bd48d8d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818712"
---
# <a name="enable-budget-proposals-preview"></a>Включение предложений по бюджету (предварительная версия)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

В этой теме объясняется, как включить функцию предложений по бюджету в финансовом анализе.

1. Используйте информацию со страницы среды в Microsoft Dynamics Lifecycle Services (LCS) для подключения к основному экземпляру Azure SQL для этой среды. Выполните следующую команду Transact-SQL (T-SQL), чтобы включить фокус-тестирования для среды песочницы. (Возможно, придется включить доступ для своего IP-адреса в LCS, прежде чем можно будет дистанционно подключиться к серверу Application Object Server \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Если развертывание Microsoft Dynamics 365 Finance является развертыванием Service Fabric, этот шаг можно пропустить Рабочая группа финансового анализа уже должна была включить фокус-тестирование для вас. Если эта функция не отображается в рабочей области **Управление функциями** или при попытке ее включения возникают проблемы, отправьте сообщение электронной почты [рабочей группе предварительной версии приложения финансового анализа](mailto:fiap@microsoft.com).

2. Откройте рабочую область **Управление функциями** и выполните следующие действия:

    1. Выберите **Проверить наличие обновлений**.
    2. Выполните поиск **Предложение бюджета** и включите эту функцию.

3. Перейдите в раздел **Бюджетирование \> Настройка \> Базовое бюджетирование \> Предложение бюджета (предварительная версия)** и выберите **Включить функцию**.

#### <a name="privacy-notice"></a>Уведомление о конфиденциальности
Предварительные версии (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 Finance and Operations, (2) не включаются в соглашение об уровне обслуживания (SLA) для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]