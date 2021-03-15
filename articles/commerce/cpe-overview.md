---
title: Обзор ознакомительной среды Dynamics 365 Commerce
description: В этой теме содержится обзор ознакомительной среды Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8e08c2f327771d7731b836840006d63b6ecb7dfc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000958"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a>Обзор ознакомительной среды Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

В этой теме содержится обзор ознакомительной среды Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Ознакомительные среды Commerce не являются общедоступными и предоставляются партнерам и клиентам по запросам по запросу. Для получения дополнительных сведений обратитесь к своему контакту Майкрософт.

## <a name="overview"></a>Обзор

Ознакомительная среда Commerce является необязательной сквозной средой Dynamics 365 Commerce, которая позволяет партнерам и потенциальным клиентам попробовать продукт Commerce.

Ознакомительные среды частично предварительно настроены для уменьшения необходимых действий после подготовки.

Помимо некоторых незначительных ограничений, которые не влияют на функции или функциональность, ознакомительная среда Commerce обеспечивает полное взаимодействие с Commerce и может быть использована клиентами и партнерами по реализации для оценки продукта, предоставления обратной связи и анализа соответствия и несоответствий.

## <a name="limitations-of-the-commerce-evaluation-environment"></a>Ограничения ознакомительной среды Commerce

Хотя ознакомительная среда Commerce предоставляет полный набор функций и функциональных возможностей Commerce, существуют некоторые незначительные ограничения:

- Хотя сама ознакомительная среда Commerce не имеет географических ограничений, компоненты среды, такие как Retail Cloud Scale Unit (RCSU) и приложения электронной коммерции, должны быть предоставлены только в США.
- У ознакомительной среды Commerce есть 30-дневное ограничение с даты предоставления электронной коммерции.
- Ознакомительная среда Commerce может быть успешно развернута и инициализирована только в среде, использующей демо-топологию, где все компоненты среды развертываются на одной виртуальной машине (VM), расположенной в облаке. Основным ограничением этой топологии является количество одновременных пользователей, которое может поддерживать среда.

## <a name="get-started"></a>Начало работы

Для обеспечения ознакомительной среды Commerce см [Обеспечение ознакомительной среды Commerce](provisioning-guide.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Подготовка ознакомительной среды Dynamics 365 Commerce](provisioning-guide.md)

[Настройка ознакомительной среды Dynamics 365 Commerce](cpe-post-provisioning.md)

[Настройка BOPIS в ознакомительной среде Dynamics 365 Commerce](cpe-bopis.md)

[Настройка дополнительных функций ознакомительной среды Dynamics 365 Commerce](cpe-optional-features.md)

[Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]