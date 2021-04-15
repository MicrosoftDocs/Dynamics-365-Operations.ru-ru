---
title: Карточки постоянного клиента и баллы поощрения
description: В этом разделе описывается интеграция сведений о карточках постоянного клиента и баллах вознаграждения при двойной записи.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: d2c3845c1a7371d9e992495246e8dd0eb8631020
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747995"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Карточки постоянного клиента и баллы поощрения

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Предприятия классифицируют клиентов и предоставляют развитые услуги на основе шаблонов покупок и расходов клиентов. Например, Dynamics 365 Commerce имеет инфраструктуру и функции для обеспечения и обработки карточек постоянного клиента, баллов вознаграждения, ценообразования на основе лояльности и покупок на основе вознаграждения. Когда данные о карточках постоянных клиентов и баллах вознаграждений в модуле Commerce синхронизируются с Dataverse, приложения взаимодействия с клиентами могут использовать эти данные. Например, пользователи Dynamics 365 Customer Service могут использовать эти данные для предоставления тех же развитых услуг в службе поддержки.

## <a name="templates"></a>Шаблоны

| Приложения Finance and Operations | Приложения на основе модели в Dynamics 365 | описание |
|-----------------------------|-----------------------------------|-------------|
| Карта постоянного клиента                | msdyn\_loyaltycards               | Этот шаблон синхронизирует сведения о карточках постоянных клиентов. |
| Баллы поощрения по программе лояльности       | msdyn\_loyaltyrewardpoints        | Этот шаблон синхронизирует сведения о баллах вознаграждения клиентов. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]