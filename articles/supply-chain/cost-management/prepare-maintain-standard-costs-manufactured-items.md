---
title: Подготовка к поддержке стандартных затрат по произведенной номенклатуре
description: В этой статье описываются шаги для подготовки к ведению затрат для произведенных номенклатур.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 423da8022faf8066c5aa524c49c5071d0871de04
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886025"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Подготовка к поддержке стандартных затрат по произведенной номенклатуре

[!include [banner](../includes/banner.md)]

В этой статье описываются шаги для подготовки к ведению затрат для произведенных номенклатур. Шаги для произведенных номенклатур немного отличаются от шагов для приобретенных номенклатур.

Политики, которые назначены произведенным номенклатурам, могут влиять на расчет затрат по родительским произведенным номенклатурам. Для подготовки к ведению затрат по произведенным номенклатурам выполните следующие действия.

1. Назначьте производимой номенклатуре группу номенклатурных моделей. 

   Группа номенклатурных моделей определяет, какие стандартные затраты будут использованы.

2. Назначьте произведенной номенклатуре номенклатурную группу. 

   Номенклатурная группа содержит счета ГК, которые относятся к произведенной номенклатуре. Счета ГК для произведенной номенклатуры, которая имеет складскую модель стандартных затрат, включают несколько отклонений цены производства от себестоимости, расхождение изменения себестоимости и переоценку себестоимости запасов.

3. Назначьте для номенклатуры единицу измерения складского учета. 

   Затраты по номенклатуре всегда выражаются в единицах измерения складского учета номенклатуры.

4. Не назначайте производимой номенклатуре группу затрат, если эта номенклатура не будет рассматриваться как приобретаемая номенклатура.

5. Назначьте произведенной номенклатуре группу расчета спецификации. 

   Группа расчета спецификации номенклатуры определяет действующие условия предупреждений. Таким образом после завершения расчета спецификации могут создаваться предупреждающие сообщения о возможных источниках ошибок при расчете. Например, предупреждающее сообщение может указать на то, что не существует активной спецификации или активного маршрута. Группа расчета спецификации содержит политику развертывания, которая определяет, когда произведенную номенклатуру следует рассматривать как приобретенную номенклатуру.

6. Если произведенная номенклатура имеет постоянные затраты, назначьте ей стандартное количество заказа. 

   Стандартное количество заказа — это размер учетного лота для амортизации постоянных затрат. Примеры постоянных затрат включают время настройки в операциях маршрутизации и постоянное количество компонентов в спецификации.

7. Определите спецификацию для произведенной номенклатуры. 

   Для произведенной номенклатуры можно определить одну или несколько версий спецификации. Убедитесь в том, что версии, которые планируется использовать, утверждены и активны, а также в том, что даты действия этих версий соответствуют требуемым. Версия спецификации может использоваться в масштабе компании или в рамках конкретного узла.

8. Определите маршрут для произведенной номенклатуры. 

   Для произведенной номенклатуры можно определить одну или несколько версий маршрута. Убедитесь в том, что версии, которые планируется использовать, утверждены и активны, а также в том, что даты действия этих версий соответствуют требуемым. Версия маршрута должна использоваться в рамках конкретного узла.

Если требуется использовать информации о маршруте для целей калькуляции затрат, требуются дополнительные подготовительные шаги. Например, потребуется обеспечить правильность и полноту категорий затрат, назначаемых операциям маршрутизации.

## <a name="related-articles"></a>Связанные статьи

[Амортизации постоянных затрат для производимой номенклатуры](amortize-constant-costs-manufactured-item.md)

[Настройка продуктов, которые можно произвести или приобрести](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]