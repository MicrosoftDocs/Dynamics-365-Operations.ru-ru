---
title: "Обзор положительного платежа"
description: "В этой статье приводятся сведения о положительном плате, используемом для формирования электронного списка чеков, которые можно предоставить банку."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 1fd606817b06a05b9abaaedf20ea9872bd7edd5d
ms.openlocfilehash: cb4806a1f023c1e60311ff9d8facb4ef5717ad94
ms.lasthandoff: 03/31/2017


---

# <a name="positive-pay-overview"></a>Обзор положительного платежа

[!include[banner](../includes/banner.md)]


В этой статье приводятся сведения о положительном плате, используемом для формирования электронного списка чеков, которые можно предоставить банку. 

Положительный платеж используется для формирования электронного списка чеков, которые можно предоставить банку. Файлы положительных платежей помогут помочь банкам предотвратить мошенничество с чеками. Можно настроить положительный платеж для формирования электронного списка чеков при каждой печати чеков. Затем, когда чек передается в банк, банк сравнивает чек со списком чеков, представленным ранее. Если чек соответствует чеку в списке, банк производит клиринг чека. Если чек не соответствует чеку в списке, банк отправляет чек на рассмотрение.

Положительная оплата также называется SafePay. 

Файлы положительных платежей могут содержать конфиденциальные сведения о получателях и суммах чеков. Поэтому убедитесь, что вы используете соответствующие меры безопасности со времени создания файлов и до получения файлов банком. Файлы положительных платежей загружаются согласно инструкциям по загрузке для веб-браузера. 

Файлы положительных платежей создаются с помощью записей данных. Перед созданием файла положительного платежа необходимо настроить форматы преобразования для XML, который переводит данные в формат, который банк может использовать. 

Для каждого банковского счета, для которого требуется создать информацию о положительных платежах, необходимо назначить формат положительных платежей. После создания платежей можно создать файл положительных платежей для одного юридического лица и одного банковского счета. Можно также одновременно создать файлы положительных платежей для нескольких юридических лиц и банковских счетов. 

После оплаты чеков, перечисленных в файле положительных платежей, вы получаете номер подтверждения из банка. Затем можно подтвердить файл положительных платежей в Microsoft Dynamics 365 for Operations. 

Если необходимо изменить файл положительных платежей, можно отозвать его. Затем для каждого чека в файле положительных платежей сбрасывается поле, которое указывает, что чек включен в файл положительных платежей.

Дополнительные сведения см. в разделе [Настройка и создание файлов положительных платежей](set-up-generate-positive-pay-files.md).



