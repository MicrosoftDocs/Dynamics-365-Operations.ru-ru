---
title: Карточки постоянного клиента и баллы поощрения
description: В этой статье описывается интеграция данных о картах лояльности клиентов и о баллах поощрения при двойной записи.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 399682b3042c32fbf6fa200213f1b4982ed97174
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289125"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Карточки постоянного клиента и баллы поощрения

[!include [banner](../../includes/banner.md)]



Предприятия классифицируют клиентов и предоставляют развитые услуги на основе шаблонов покупок и расходов клиентов. Например, Dynamics 365 Commerce имеет инфраструктуру и функции для обеспечения и обработки карточек постоянного клиента, баллов вознаграждения, ценообразования на основе лояльности и покупок на основе вознаграждения. Когда данные о карточках постоянных клиентов и баллах вознаграждений в модуле Commerce синхронизируются с Dataverse, приложения взаимодействия с клиентами могут использовать эти данные. Например, пользователи Dynamics 365 Customer Service могут использовать эти данные для предоставления тех же развитых услуг в службе поддержки.

## <a name="templates"></a>Шаблоны

Приложения Finance and Operations | Приложения для взаимодействия с клиентами     | описание
|-----------------------------|-----------------------------------|-------------|
[Карта лояльности](mapping-reference.md#149) | msdyn_loyaltycards | Этот шаблон синхронизирует сведения о карточках постоянных клиентов. |
[Уровни лояльности](mapping-reference.md#226) | msdyn_loyaltylevels | Этот шаблон синхронизирует сведения о баллах вознаграждения клиентов. |
[Баллы поощрения по программе лояльности](mapping-reference.md#150) | msdyn_loyaltyrewardpoints | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
