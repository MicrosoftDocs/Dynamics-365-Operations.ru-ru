---
title: "Домашняя страница управления затратами"
description: "Управление затратами позволяет обрабатывать оценку и учет сырья, незаконченных товаров, готовых изделий и средств незавершенного производства."
author: AndersGirke
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cab2f165a70e5ce8f09f0391282e055e51afb225
ms.openlocfilehash: b1513e5a7cb3a19fd3743a5aac8efd211aa02ce8
ms.contentlocale: ru-ru
ms.lasthandoff: 02/21/2018

---

# <a name="cost-management-home-page"></a>Домашняя страница управления затратами

[!include [banner](../includes/banner.md)]

[Управление затратами (видео)](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be) позволяет работать с оценкой и учетом сырья, незаконченных товаров, готовых изделий и средств незавершенного производства. Это процесс определения, управления и отчетности для [складского учета](cost-object.md) и [учета производства](bom-calculations.md).

Можно определить политики затрат в следующих областях: 
-  [Заранее определенные затраты](costing-versions.md)
-  [Учет запасов](cost-object.md)
-  [Учет производства](bom-calculations.md)
-  [Учет косвенных затрат](costing-sheets.md)
-  [Интеграция с ГК](production-order-cost-analysis.md)

Например, можно определить, какие методы оценки запасов, такие как [ФИФО](fifo-physical-value-marking.md), [взвешенное среднее](weighted-average-physical-value-marking.md), [стандартная себестоимость](prerequisites-standard-costs.md) или [скользящее среднее](moving-average.md), требуется применить к продуктам в [группе моделей номенклатуры](../inventory/reserve-inventory-quantities.md) в складском учете.

Доступ к учету запасов и учету производства возможен из рабочих областей **Администрирование затрат** и **Анализ затрат**. Эти рабочие области дают полный обзор текущего состояния, ключевых индикаторов производительности (KPI) и обнаружения отклонения. 

Учет производства позволяет обрабатывать [позаказную калькуляцию себестоимости](production-order-cost-analysis.md) в производственных заказах и заказах партий, а также [backflush-расчет себестоимости](backflush-costing.md) для бережливого производства.

[Содержимое Power BI "Управление затратами"](../../dev-itpro/analytics/cost-management-content-pack.md) предоставляет управленческие сведения о запасах и запасах по незавершенному производству (НЗП), а также о потоках затрат через них по категориям с течением времени. Информация может также использоваться как подробное приложение к финансовой отчетности.

### <a name="additional-resources"></a>Дополнительные ресурсы

#### <a name="whats-new-and-in-development"></a>Новые возможности и текущие разработки

Перейдите в раздел [Дорожная карта Microsoft Dynamics 365](https://roadmap.dynamics.com/), чтобы узнать, какие новые функции уже выпущены, а какие еще находятся в разработке. 

#### <a name="white-paper"></a>Информационный документ
В разделе [Расчет спецификации с использованием схемы калькуляции](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/white-papers/365operationsbomcalsheet) описывается, как настроить схему калькуляции, включающую материал и производство, и как настройка влияет на результаты расчета спецификации. Для более подробного объяснения этих тем предоставлены конкретные сценарии и данные, которые демонстрируются влияние различных параметров и конфигураций. Не ожидается, что вы будете следовать всем этим сценариям, поскольку этот документ не предоставляет достаточно сведений для их настройки. Тем не менее, если имеются основные знания, вы можете попробовать воспроизвести перечисленные ниже руководства по задачам в порядке их расположения. Используйте знания, полученные при ознакомлении с этим документом, чтобы провести анализ расчета спецификации. 

-  [Создание готовой продукции](tasks/create-finished-product-2016-02.md)
-  [Создание полуфабриката](tasks/create-semi-finished-product-2016-02.md)
-  [Создание сырья](tasks/create-raw-materials-2016-02.md)
-  [Создание спецификаций](tasks/create-boms-2016-02.md)
-  [Создать маршруты](tasks/create-routes-2016-02.md)
-  [Расчет спецификации с помощью одноуровневой структуры](tasks/calculate-bom-single-level-structure-2016-02.md)
-  [Расчет спецификации с помощью многоуровневой структуры](tasks/calculate-bom-multilevel-structure-2016-02.md)


#### <a name="blogs"></a>Блоги
В [блоге группы исследований производства Dynamics AX](https://blogs.msdn.microsoft.com/axmfg) и в [блоге группы исследований управления цепочками поставок Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm) можно найти мнения, новости и другие сведения об управлении затратами. Хотя некоторые из этих записей посвящены предыдущей версии модуля "Управление затратами", обсуждаемые в них понятия по-прежнему применяются, а процедуры аналогичны процедурам в текущей версии.

#### <a name="task-guides"></a>Проводники по задачам
Проводники по задачам в Finance and Operations — это еще один источник справочной информации. Чтобы перейти к проводникам по задачам, нажмите кнопку "Справка" на любой странице.


