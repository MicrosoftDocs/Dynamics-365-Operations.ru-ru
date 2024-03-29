---
title: Планирование в смешанном режиме — совмещение дискретного производства, непрерывного производства и бережливый выбор источников материалов
description: Эта статья содержит сведения о планировании в смешанном режиме.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 335bdc9690b3111f4a04adc7e82d62de36ff4caf
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065999"
---
# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Планирование в смешанном режиме — совмещение дискретного производства, непрерывного производства и бережливый выбор источников материалов

[!include [banner](../includes/banner.md)]

Эта статья содержит сведения о планировании в смешанном режиме. В планировании в смешанном режиме, можно смоделировать цепь поставок на основе потока материалов. Dynamics 365 Supply Chain Management следит, чтобы убедитесь, что поток материалов следует вашим моделям, независимо от выбранной политики поставки (канбаны, производственных заказов, заказов на покупку, заказы партии или заказы на перемещение). 

Вы можете выбрать свою общую стратегию поставки продукта, вне зависимости от структуры продукта.  

Например, вы можете использовать управление по системе канбан в сборочном цехе, где материалы поступают на сборку посредством производственных заказов, канбанов, перемещений, партионных заказов или любого их сочетания, подходящего к характеристикам вашей цепочки поставок, но в то же время сохранить полную прозрачность всех поставок. Эта возможность позволяет получить оптимизированные процессы цепочки поставок и увеличить просматриваемость вашей цепочки поставок.  

Степень детализации политик поставки, которые используются в сводном планировании, зависит от аналитик хранения, включенных в качестве аналитик покрытия. Чтобы можно было использовать сводное планирование для управления пополнением и поставок в различных типах месторасположений (например, путем разделения производственного цеха для различных производственных подразделений или путем разделения различных типов складов материалов и готовой продукции), рекомендуется включить "Сайт" и "Склад" в качестве аналитик покрытия. Другой вариант — опустить "Склад" в качестве аналитики покрытия. В таком случае, когда вы используете процессы управления складом (WMS), всеми перемещениями в пределах склада управляет работа склада, а управлять всеми перемещениями с одного склада на другой можно с помощью канбанов изъятия.

## <a name="supply-policies"></a>Политики поставки
Планирование в смешанном режиме управляет тем, как поставляется продукт и, в зависимости от поставки, как происходит выдача производных требований (потребление номенклатур из спецификации \[BOM\]). Исходя из типа заказа, система автоматически выбирает источники материалов для удовлетворения потребностей.  

Политики поставки могут быть определены на уровне продукта или на любом уровне детализации, соответствующей вашим требованиям. Степень детализации политик поставки определяется на странице **Параметры заказа по умолчанию**.  

Политики поставки могут определяться продуктом, аналитиками номенклатур (конфигурацией, цветом и размером), сайтом и складом. Это настраивается на странице **Покрытие номенклатуры**.  

Тип заказа значения по умолчанию определяет результаты, формируемые сводным планированием заказов.  

Вне зависимости от того, как смоделирована цепочка поставок, Supply Chain Management будет поддерживать ваше сочетание политик поставки. У вас могут быть производственные заказы, для которых материалы берутся из канбанов. Другой вариант — у вас может быть партионный заказ, для которого требуется продукт, поставляемый посредством перемещений или посредством канбанов.  

Supply Chain Management обеспечивает, что движение материала следует модели.  

Склад для комплектации материала назначается динамически во время выполнения, после определения политики поставки.  

Как правило, канбаны не создаются на будущие даты, потому что канбан имеет короткий жизненный цикл. Чтобы обеспечить полную просмариваемость цепочки поставок, мы внедрили новую концепцию планирования — "спланированный канбан", которая используется для расчета производных потребностей и помогает гарантировать, что выбор источников материалов для удовлетворения потребностей будет основан на той же логике, которая используется при создании фактического канбана.  

Такая же логика присутствует для всех других типов политики поставки. Следовательно, долгосрочное планирование материалов основано на той же логике, которую вы ожидаете использовать для фактических заказов после утверждения производства и поставок.

## <a name="materials-allocation-cross-supply-policy--resource-consumption-on-boms"></a>Политика взаимных поставок при распределении материалов — потребление ресурсов в спецификациях
Потребление ресурсов — важная функциональность. Потребление ресурсов обеспечивает возможность динамического выбора склада для комплектации материалов на основании политики поставки (типа заказа), а также облегчает ведение базовых данных.  

Потребление ресурсов требует, чтобы склад, с которого комплектуются материалы, назначался в зависимости от способа поставки продукта. Другими словами, во время выполнения система находит ресурсы, которые должны использоваться для производства. На основании этих ресурсов система затем находит склад комплектации.  

Для работы, которая не зависит от политики поставки, вам не нужно изменять информацию в спецификации, если изменяется поставка. При разовых изменениях Supply Chain Management обеспечивает, что материалы берутся с правильного склада.

## <a name="process-manufacturing--the-production-type"></a>Непрерывное производство — производственный тип
Для полной гибкости в смешанном режиме мы рекомендуем использовать спецификации производственного типа для всех продуктов. В этом случае для поставки продукта можно будет использовать производственные заказы, канбаны, заказы на перемещение или заказы на покупку. Для непрерывного производства необходимо использовать производственный тип **Формула**, **Сопутствующий продукт**, **Побочный продукт** или **Плановая номенклатура**. Использовать для этих производственных типов канбаны и производственные заказы нельзя.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]