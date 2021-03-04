---
title: Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce
description: Эта тема дает ответы на часто задаваемые вопросы об ознакомительной среде Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 637714e28b9f8f4aa66e251e709d8f78bff2739d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415136"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Эта тема дает ответы на часто задаваемые вопросы об ознакомительной среде Microsoft Dynamics 365 Commerce.

**Можем ли мы использовать ознакомительную среду Commerce в качестве магазина электронной коммерции для клиентов, которые в настоящее время реализуют Retail?**

№ п/п Ознакомительная среда Commerce предназначена только для ознакомления. Если вам нужна среда для клиента, реализующего Retail, обратитесь в Майкрософт.

**Можно ли использовать ознакомительную среду Commerce для предоставления функций электронной коммерции поверх существующего приложения/среды, которая реализует Retail?**

Нет (главным образом). Ознакомительные компоненты Commerce доступны только в тех средах, которые соответствуют конфигурациям, указанным в руководстве по предварительным условиям и подготовке. Кроме того, требуемые базовые демонстрационные данные не будут доступны в средах, которые были развернуты в исходном выпуске ранее 10.0.8. 

**Какие затраты связаны с развертыванием ознакомительной среды Commerce в Microsoft Azure через Microsoft Dynamics Lifecycle Services (LCS)?**

Традиционная демонстрационная среда Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce Headquarters (виртуальная машина \[VM\]) будет размещена в вашей подписке Azure. Для оценки расходов можно использовать [калькулятор цен Azure](https://azure.microsoft.com/pricing/calculator/).

Другие компоненты, такие как Commerce Scale Unit, конструктор сайта Commerce и сайт электронной коммерции будут доступны как программное обеспечение как услуга (SaaS) и размещены в корпорации Майкрософт.

**Какие географические регионы Azure в настоящее время поддерживаются для ознакомительной среды Commerce?**

Ознакомительная среда Commerce может быть развернута только в Северной Америке.

**Есть ли загружаемый виртуальный жесткий диск (VHD) с вариантом полной виртуальной машины OneBox?**

Dynamics 365 Commerce и Commerce Scale Unit — это полностью программное обеспечение как услуга (SaaS) и должны размещать в облаке.

**Как долго может использоваться ознакомительная среда Commerce?**

В ознакомительной среде Commerce имеется предельное время в 30 дней от даты, когда были подготовлены компоненты SaaS, такие как Commerce Scale Unit, конструктор сайтов Commerce site и сайт электронной коммерции.

**Могу ли я продлить срок для ознакомительной среды Commerce?**

Расширение предела времени является исключением из нормы и рассматривается отдельно для каждого случая. Следует обратитесь за помощью к партнеру корпорации Майкрософт.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор ознакомительной среды Dynamics 365 Commerce](cpe-overview.md)

[Подготовка ознакомительной среды Dynamics 365 Commerce](provisioning-guide.md)

[Настройка ознакомительной среды Dynamics 365 Commerce](cpe-post-provisioning.md)

[Настройка BOPIS в ознакомительной среде Dynamics 365 Commerce](cpe-bopis.md)

[Настройка дополнительных функций ознакомительной среды Dynamics 365 Commerce](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]