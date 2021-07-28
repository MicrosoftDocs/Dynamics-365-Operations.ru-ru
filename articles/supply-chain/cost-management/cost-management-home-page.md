---
title: Домашняя страница управления затратами
description: Управление затратами позволяет обрабатывать оценку и учет сырья, незаконченных товаров, готовых изделий и средств незавершенного производства.
author: AndersGirke
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d36a064fe8773dae36fe5beabcd675a82cfaba66
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337680"
---
# <a name="cost-management-home-page"></a>Домашняя страница управления затратами

[!include [banner](../includes/banner.md)]

[Управление затратами (видео)](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be) позволяет работать с оценкой и учетом сырья, незаконченных товаров, готовых изделий и средств незавершенного производства. Это процесс определения, управления и отчетности для [складского учета](cost-object.md) и [учета производства](bom-calculations.md).

Можно определить политики затрат в следующих областях:

- [Заранее определенные затраты](costing-versions.md)
- [Учет запасов](cost-object.md)
- [Учет производства](bom-calculations.md)
- [Учет косвенных затрат](costing-sheets.md)
- [Интеграция с ГК](production-order-cost-analysis.md)

Например, можно определить, какие методы оценки запасов, такие как [ФИФО](fifo-physical-value-marking.md), [взвешенное среднее](weighted-average-physical-value-marking.md), [стандартная себестоимость](prerequisites-standard-costs.md) или [скользящее среднее](moving-average.md), требуется применить к продуктам в [группе моделей номенклатуры](../inventory/reserve-inventory-quantities.md) в складском учете.

Доступ к учету запасов и учету производства возможен из рабочих областей **Администрирование затрат** и **Анализ затрат**. Эти рабочие области дают полный обзор текущего состояния, ключевых индикаторов производительности (KPI) и обнаружения отклонения. 

Учет производства позволяет обрабатывать [позаказную калькуляцию себестоимости](production-order-cost-analysis.md) в производственных заказах и заказах партий, а также [backflush-расчет себестоимости](backflush-costing.md) для бережливого производства.

[Содержимое Power BI "Управление затратами"](../../fin-ops-core/dev-itpro/analytics/cost-management-content-pack.md) предоставляет управленческие сведения о запасах и запасах по незавершенному производству (НЗП), а также о потоках затрат через них по категориям с течением времени. Информация может также использоваться как подробное приложение к финансовой отчетности.

### <a name="additional-resources"></a>Дополнительные ресурсы

#### <a name="whats-new-and-in-development"></a>Новые возможности и текущие разработки

Перейдите в раздел [Дорожная карта Microsoft Dynamics 365](https://roadmap.dynamics.com/), чтобы узнать, какие новые функции уже выпущены, а какие еще находятся в разработке.

#### <a name="white-paper"></a>Информационный документ

В разделе [Расчет спецификации с использованием схемы калькуляции](https://www.microsoft.com/download/details.aspx?id=101937) описывается, как настроить схему калькуляции, включающую материал и производство, и как настройка влияет на результаты расчета спецификации. Для более подробного объяснения этих тем предоставлены конкретные сценарии и данные, которые демонстрируются влияние различных параметров и конфигураций.

#### <a name="blogs"></a>Блоги

В [блоге группы исследований производства Dynamics AX](/archive/blogs/axmfg/) и в [блоге группы исследований Supply Chain Management в Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm) можно найти мнения, новости и другие сведения об управлении затратами. Хотя некоторые из этих записей посвящены предыдущей версии модуля "Управление затратами", обсуждаемые в них понятия по-прежнему применяются, а процедуры аналогичны процедурам в текущей версии.

#### <a name="task-guides"></a>Проводники по задачам

Дополнительная справка доступна в виде руководств по задачам. Чтобы перейти к проводникам по задачам, нажмите кнопку "Справка" на любой странице.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]