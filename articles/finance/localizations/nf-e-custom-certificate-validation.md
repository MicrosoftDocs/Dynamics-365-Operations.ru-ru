---
title: Проверка пользовательского сертификата NF-e
description: В этой теме приводятся сведения о включении и использовании пользовательского сертификата NF-e.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447136"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="9ab35-103">Проверка пользовательского сертификата NF-e</span><span class="sxs-lookup"><span data-stu-id="9ab35-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ab35-104">При включении функции проверки пользовательских сертификатов NF-e пользовательская проверка разрешает подключение к веб-службам.</span><span class="sxs-lookup"><span data-stu-id="9ab35-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="9ab35-105">Это подключение требуется для передачи NF-e и получения авторизации от SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="9ab35-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="9ab35-106">Свойство **Цель проверки подлинности сервера** из сертификата V5 выдается корневым центром сертификации Бразилии.</span><span class="sxs-lookup"><span data-stu-id="9ab35-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="9ab35-107">По умолчанию это свойство отключено, и оно должно быть включено вручную.</span><span class="sxs-lookup"><span data-stu-id="9ab35-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="9ab35-108">В некоторых обстоятельствах автоматическое обновление сертификатов может переключать это свойство, чтобы оно больше не было включено.</span><span class="sxs-lookup"><span data-stu-id="9ab35-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="9ab35-109">В этом случае виновато TLS-подключение, и оно больше не является доверенным.</span><span class="sxs-lookup"><span data-stu-id="9ab35-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="9ab35-110">Также затрагивается возможность выпуска NF-e в производственных средах для штатов Minas Gerais (MG) и Paraná (PR).</span><span class="sxs-lookup"><span data-stu-id="9ab35-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="9ab35-111">Это обновление предоставляет альтернативное решение для проверки сертификатов, что означает возможность установления безопасного подключения.</span><span class="sxs-lookup"><span data-stu-id="9ab35-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


