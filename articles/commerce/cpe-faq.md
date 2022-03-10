---
title: Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce
description: Эта тема дает ответы на часто задаваемые вопросы об ознакомительной среде Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e8a3e760353b351d42aff82c0d372d2aca350cd2
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343566"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Вопросы и ответы по среде оценки Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Эта тема дает ответы на часто задаваемые вопросы об ознакомительной среде Microsoft Dynamics 365 Commerce.

## <a name="can-we-use-the-commerce-evaluation-environment-as-an-e-commerce-storefront-for-customers-that-currently-implement-retail"></a>Можем ли мы использовать ознакомительную среду Commerce в качестве магазина электронной коммерции для клиентов, которые в настоящее время реализуют Retail?

№ п/п Ознакомительная среда Commerce предназначена только для ознакомления. Если вам нужна среда для клиента, реализующего Retail, обратитесь в Майкрософт.

## <a name="can-the-commerce-evaluation-environment-be-used-to-provision-the-e-commerce-features-on-top-of-an-existing-applicationenvironment-that-implements-retail"></a>Можно ли использовать ознакомительную среду Commerce для предоставления функций электронной коммерции поверх существующего приложения/среды, которая реализует Retail?

Нет (главным образом). Ознакомительные компоненты Commerce доступны только в тех средах, которые соответствуют конфигурациям, указанным в руководстве по предварительным условиям и подготовке. Кроме того, требуемые базовые демонстрационные данные не будут доступны в средах, которые были развернуты в исходном выпуске ранее 10.0.8. 

## <a name="what-costs-are-involved-in-deploying-the-commerce-evaluation-environment-on-microsoft-azure-via-microsoft-dynamics-lifecycle-services-lcs"></a>Какие затраты связаны с развертыванием ознакомительной среды Commerce в Microsoft Azure через Microsoft Dynamics Lifecycle Services (LCS)?

Традиционная демонстрационная среда Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce Headquarters (виртуальная машина \[VM\]) будет размещена в вашей подписке Azure. Для оценки расходов можно использовать [калькулятор цен Azure](https://azure.microsoft.com/pricing/calculator/).

Другие компоненты, такие как Commerce Scale Unit, конструктор сайта Commerce и сайт электронной коммерции будут доступны как программное обеспечение как услуга (SaaS) и размещены в корпорации Майкрософт.

## <a name="which-azure-geographies-are-currently-supported-for-the-commerce-evaluation-environment"></a>Какие географические регионы Azure в настоящее время поддерживаются для ознакомительной среды Commerce?

Ознакомительная среда Commerce может быть развернута только в Северной Америке.

## <a name="is-there-a-downloadable-virtual-hard-disk-vhd-that-has-the-complete-onebox-virtual-machine-vm-option"></a>Есть ли загружаемый виртуальный жесткий диск (VHD) с вариантом полной виртуальной машины OneBox?

Dynamics 365 Commerce и Commerce Scale Unit — это полностью программное обеспечение как услуга (SaaS) и должны размещать в облаке.

## <a name="how-long-can-the-commerce-evaluation-environment-be-used"></a>Как долго может использоваться ознакомительная среда Commerce?

В ознакомительной среде Commerce имеется предельное время в 30 дней от даты, когда были подготовлены компоненты SaaS, такие как Commerce Scale Unit, конструктор сайтов Commerce site и сайт электронной коммерции.

## <a name="can-i-extend-the-time-limit-for-my-commerce-evaluation-environment"></a>Могу ли я продлить срок для ознакомительной среды Commerce?

Расширение предела времени является исключением из нормы и рассматривается отдельно для каждого случая. Следует обратитесь за помощью к партнеру корпорации Майкрософт.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор ознакомительной среды Dynamics 365 Commerce](cpe-overview.md)

[Подготовка ознакомительной среды Dynamics 365 Commerce](provisioning-guide.md)

[Настройка ознакомительной среды Dynamics 365 Commerce](cpe-post-provisioning.md)

[Настройка BOPIS в ознакомительной среде Dynamics 365 Commerce](cpe-bopis.md)

[Настройка дополнительных функций ознакомительной среды Dynamics 365 Commerce](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
