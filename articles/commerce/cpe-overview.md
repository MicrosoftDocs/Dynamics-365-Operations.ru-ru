---
title: Обзор среды предварительного просмотра Commerce
description: В этой теме содержится обзор среды предварительного просмотра Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
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
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906078"
---
# <a name="commerce-preview-environment-overview"></a>Обзор среды предварительного просмотра Commerce

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

В этой теме содержится обзор среды предварительного просмотра Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Обзор

Среда предварительного просмотра Commerce является необязательной сквозной средой предварительного просмотра Dynamics 365 Commerce, которая позволяет потенциальным клиентам попробовать продукт Commerce до его общего выпуска.

Помимо некоторых незначительных ограничений, которые не влияют на функции или функциональность, среда предварительного просмотра Commerce обеспечивает полное взаимодействие с Commerce и может быть использована клиентами и партнерами по реализации для оценки продукта, предоставления обратной связи и анализа соответствия и несоответствий.

## <a name="limitations-of-the-commerce-preview-environment"></a>Ограничения среды предварительного просмотра Commerce

Хотя среда предварительного просмотра Commerce предоставляет полный набор функций и функциональных возможностей Commerce, существуют некоторые незначительные ограничения:

- Хотя сама среда предварительного просмотра Commerce не имеет географических ограничений, компоненты среды, такие как Retail Cloud Scale Unit (RCSU) и приложения электронной коммерции, могут быть предоставлены только в США.
- У среды предварительного просмотра Commerce есть 30-дневное ограничение с даты предоставления электронной коммерции.
- Среда предварительного просмотра Commerce может быть успешно развернута и инициализирована только в среде, использующей демо-топологию, где все компоненты среды развертываются на одной виртуальной машине (VM). Основным ограничением этой топологии OneBox VM является количество одновременных пользователей, которое может поддерживать среда предварительного просмотра.
- Среду предварительного просмотра Commerce можно оценивать только до общего выхода продукта Commerce. Новые демо-среды будут доступны после общего выхода.

## <a name="get-started"></a>Начало работы

Для обеспечения среды предварительного просмотра Commerce см [Обеспечение среды предварительного просмотра Commerce](provisioning-guide.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обеспечение среды предварительного просмотра Commerce](provisioning-guide.md)

[Настройка среды предварительного просмотра Commerce](cpe-post-provisioning.md)

[Настройка дополнительных функций для среды предварительного просмотра Commerce](cpe-optional-features.md)

[Вопросы и ответы среды предварительного просмотра Commerce](cpe-faq.md)
