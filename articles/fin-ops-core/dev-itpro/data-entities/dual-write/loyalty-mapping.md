---
title: Карточки постоянного клиента и баллы поощрения
description: В этом разделе описывается интеграция сведений о карточках постоянного клиента и баллах вознаграждения между приложениями Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172977"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Карточки постоянного клиента и баллы поощрения

[!include [banner](../../includes/banner.md)]



Предприятия классифицируют клиентов и предоставляют развитые услуги на основе шаблонов покупок и расходов клиентов. В пакете приложений Microsoft Dynamics 365 приложение Dynamics 365 Commerce имеет инфраструктуру и функции для обеспечения и обработки карточек постоянного клиента, баллов вознаграждения, ценообразования на основе лояльности и покупок на основе вознаграждения. Когда данные о карточках постоянных клиентов и баллах вознаграждений в модуле Commerce синхронизируются со службой Common Data Service, приложения на основе модели в Dynamics 365 могут использовать эти данные. Например, пользователи Dynamics 365 Customer Service могут использовать эти данные для предоставления тех же развитых услуг в службе поддержки.

## <a name="templates"></a>Шаблоны

| Приложения Finance and Operations | Приложения на основе модели в Dynamics 365 | описание |
|-----------------------------|-----------------------------------|-------------|
| Карта постоянного клиента                | msdyn\_loyaltycards               | Этот шаблон синхронизирует сведения о карточках постоянных клиентов. |
| Баллы поощрения по программе лояльности       | msdyn\_loyaltyrewardpoints        | Этот шаблон синхронизирует сведения о баллах вознаграждения клиентов. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
