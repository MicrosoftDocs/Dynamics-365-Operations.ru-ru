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
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f13e8b8229bbd9e174e5bde7858a468048ba309b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990094"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="ea927-103">Проверка пользовательского сертификата NF-e</span><span class="sxs-lookup"><span data-stu-id="ea927-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea927-104">При включении функции проверки пользовательских сертификатов NF-e пользовательская проверка разрешает подключение к веб-службам.</span><span class="sxs-lookup"><span data-stu-id="ea927-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="ea927-105">Это подключение требуется для передачи NF-e и получения авторизации от SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="ea927-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="ea927-106">Свойство **Цель проверки подлинности сервера** из сертификата V5 выдается корневым центром сертификации Бразилии.</span><span class="sxs-lookup"><span data-stu-id="ea927-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="ea927-107">По умолчанию это свойство отключено, и оно должно быть включено вручную.</span><span class="sxs-lookup"><span data-stu-id="ea927-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="ea927-108">В некоторых обстоятельствах автоматическое обновление сертификатов может переключать это свойство, чтобы оно больше не было включено.</span><span class="sxs-lookup"><span data-stu-id="ea927-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="ea927-109">В этом случае виновато TLS-подключение, и оно больше не является доверенным.</span><span class="sxs-lookup"><span data-stu-id="ea927-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="ea927-110">Также затрагивается возможность выпуска NF-e в производственных средах для штатов Minas Gerais (MG) и Paraná (PR).</span><span class="sxs-lookup"><span data-stu-id="ea927-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="ea927-111">Это обновление предоставляет альтернативное решение для проверки сертификатов, что означает возможность установления безопасного подключения.</span><span class="sxs-lookup"><span data-stu-id="ea927-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


