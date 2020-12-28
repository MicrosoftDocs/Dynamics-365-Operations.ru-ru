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
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 25c0574e8d4502bcb846fba0ddf913d81eded87b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415132"
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
