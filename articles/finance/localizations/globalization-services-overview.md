---
title: Службы глобализации Dynamics 365
description: В этом разделе представлен обзор служб глобализации Microsoft Dynamics 365.
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2ef942f7f6dac2c321a51800ade0bf25f2162304
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018815"
---
# <a name="dynamics-365-globalization-services"></a>Службы глобализации Dynamics 365

[!include [banner](../includes/banner.md)]

Следующие службы глобализации могут быть настроены для расширения возможностей, которые существуют в некоторых веб-службах Microsoft Dynamics 365:

- **Служба Regulatory Configuration Service (RCS)** поддерживает настройку различных типов электронных документов и отчетов. RCS предоставляет улучшенную версию конструктора электронной отчетности (ER), когда репозиторий конфигураций является автономной службой. Дополнительные сведения см. в [Regulatory Configuration Service](rcs-overview.md).
- **Электронное выставление накладных** объединяет в себе настраиваемые форматы преобразований, цифровых подписей и настраиваемых интеграций для связи с внешними веб-службами, включая обработку сертификатов и откликов. Дополнительные сведения см. в [Электронное выставление накладных](e-invoicing-service-overview.md).
- **Расчет налогов** обеспечивает расширенную гибкость за счет поддержки нескольких налоговых кодов, определения кода налога, конструктора расчета налога и ядра среды выполнения для обеспечения соответствия сложным налоговым нормам по всему миру. Дополнительные сведения см. в [Расчет налогов](global-tax-calcuation-service-overview.md).

Эти службы глобализации обеспечивают интеграцию со следующими веб-службами Dynamics 365.

| Веб-служба | RCS | Электронное выставление накладных | Расчет налогов (предварительная версия) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | Да | Да | Да | 
| Dynamics 365 Supply Chain Management | Да | Да | Да | 
| Dynamics 365 Project Operations | Да | Да | Неприменимо | 
| Dynamics 365 Commerce | Да | Неприменимо | Неприменимо | 

> [!NOTE]
> Из-за различий в доступности географического местоположения Azure (георепликации) для RCS, настройка этой службы может привести к тому, что данные клиента будут переданы вне георепликации, выбранной для применимой веб-службы Dynamics 365. Дополнительные сведения см. в [Dynamics 365 и Power Platform: доступность, расположение данных, язык и локализация](https://aka.ms/rcs/D365Productavailabilityguide).