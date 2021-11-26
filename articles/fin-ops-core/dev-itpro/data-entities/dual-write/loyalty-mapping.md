---
title: Карточки постоянного клиента и баллы поощрения
description: В этом разделе описывается интеграция сведений о карточках постоянного клиента и баллах вознаграждения при двойной записи.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 919ce0d57fb306b39cdcdd8655ac9f0b9e26847e
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781672"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Карточки постоянного клиента и баллы поощрения

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Предприятия классифицируют клиентов и предоставляют развитые услуги на основе шаблонов покупок и расходов клиентов. Например, Dynamics 365 Commerce имеет инфраструктуру и функции для обеспечения и обработки карточек постоянного клиента, баллов вознаграждения, ценообразования на основе лояльности и покупок на основе вознаграждения. Когда данные о карточках постоянных клиентов и баллах вознаграждений в модуле Commerce синхронизируются с Dataverse, приложения взаимодействия с клиентами могут использовать эти данные. Например, пользователи Dynamics 365 Customer Service могут использовать эти данные для предоставления тех же развитых услуг в службе поддержки.

## <a name="templates"></a>Шаблоны

Приложения Finance and Operations | Приложения для взаимодействия с клиентами     | описание
|-----------------------------|-----------------------------------|-------------|
[Карта лояльности](mapping-reference.md#149) | msdyn_loyaltycards | Этот шаблон синхронизирует сведения о карточках постоянных клиентов. |
[Уровни лояльности](mapping-reference.md#226) | msdyn_loyaltylevels | Этот шаблон синхронизирует сведения о баллах вознаграждения клиентов. |
[Баллы поощрения по программе лояльности](mapping-reference.md#150) | msdyn_loyaltyrewardpoints | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
