---
title: Ваучер не создан
description: В этой теме содержатся сведения об устранении неполадок, которые могут помочь, когда ваучер должен быть создан, но не создан.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 82357b7fe00b93715f44eb024ac78d7cc1adca84
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356109"
---
# <a name="voucher-isnt-generated"></a>Ваучер не создан

[!include [banner](../includes/banner.md)]

Если ваучер должна быть сформирован, но на странице **Проводки ваучера** не отображаются ваучеры, выполните действия, указанные в следующих разделах, в соответствии с требованиями для устранения проблемы.

[![Страница проводок ваучера без ваучеров.](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>Проверка применимости налога

1. Перейдите **Налог** \> **Периодические задачи** \> **Записи журнала субкниги еще не переданы**.
2. Если есть запись в журнале, выберите ее, а затем выберите **Перенести сейчас**.

    [![Кнопка "Перенести сейчас" на странице "Записи журнала субкниги еще не переданы".](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. Снова откройте страницу **Проводки ваучера**, чтобы просмотреть, был ли создан данный ваучер.

## <a name="determine-whether-customization-exists"></a>Определение существования настройки

Если вы выполнили шаги в предыдущем разделе, но не смогли решить проблему, определите, существует ли настройка. Если настройки не существует, создайте запрос в службу поддержки Майкрософт для получения дополнительной поддержки.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
