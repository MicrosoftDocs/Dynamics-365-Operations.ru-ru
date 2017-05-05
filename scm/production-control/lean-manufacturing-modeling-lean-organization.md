---
title: "Моделирование бережливой организации"
description: "Статья представляет информацию о ключевых понятиях в моделировании бережливый организации."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 08 - 43
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 536b20d5c4c2030800df25d0d227deaac386aee5
ms.lasthandoff: 03/29/2017


---

# <a name="modeling-a-lean-organization"></a>Моделирование бережливой организации

Статья представляет информацию о ключевых понятиях в моделировании бережливый организации. 

Обычно — Сценарий бережливого производства — это обычно нечто большее, чем агломерация несвязанных правил канбана или политик поставки материалов. Движение материалов и продуктов через производственные ячейки и месторасположения для конкретного сценария производства или поставок можно описать как последовательность или небольшую сеть мероприятий по обработке и перемещению. Эта последовательность или сеть называется производственным потоком.

## <a name="production-flows-in-lean-manufacturing"></a>Производственные потоки в бережливом производстве
В производственных сценариях, основанных на производственных заказах, выпуск материала производится по конкретный производственный заказ. В ходе последовательности мероприятий, на основе спецификации и маршрутов, создаются продукты, которые в конечном итоге поступают в указанное месторасположение. Время изготовления производственных заказов варьируется от минут до недель. В производственном заказе аккумулируются все связанные затраты, материалы и трудозатраты. С целью сокращения времени поставки и уровней запасов между рабочими центрами, вызванных производством продукции партиями, в бережливом производстве используется пополнение канбанов, а также супермаркеты в производстве и пополнении складских запасов. Эти функции обычно нарушают производство частично независимых канбан-циклов. Пополнение канбана для полуфабриката больше не инициируется заказом на готовый продукт. Для восстановления производственного и затратного контекстов для различных сценариев использования канбанов, предлагаемых в Microsoft Dynamics AX, в качестве принципиальной основы бережливого производства введены производственные потоки, основанные на мероприятиях. Все правила канбанов ссылаются на эту предопределенную структуру. Основанная на мероприятиях модель позволяет выстраивать сценарии в более широком спектре, чем при использовании предыдущих версиях бережливого производства в Microsoft Dynamics AX. Модель не добавляет сложность для работников цеха, поскольку во всех сценариях используется один и тот же основанный на мероприятиях интерфейс.

## <a name="semifinished-products-nonbom-levels"></a>Полуфабрикаты (не уровни спецификации)
Бережливое производство для Dynamics AX интегрирует канбаны для направляемых в запасы продуктов и полуфабрикатов в единую структуру, обеспечивая унифицированный пользовательский опыт во всех ситуациях. Вследствие этой архитектуры устраняется потребность во введении дополнительных уровней спецификаций для использования канбанов для полуфабрикатов. Эта архитектура также помогает уменьшить проводки по запасам к минимуму.

## <a name="products-and-material-in-work-in-progress"></a>Продукты и материалы в незавершенном производстве
Уменьшение размеров партий вплоть до идеального состояния — поединичного потока — в бережливом производстве может привести к резкому увеличению количества проводок по запасам, если каждый процесс комплектации или регистрации канбана будет формировать проводки по потребленным номенклатурам. Архитектура производственного потока позволяет перемещать материалы в производственный поток, вместе с канбанами изъятия в месте хранения или величинами единиц обработки транспортировки. Стоимость выданного материала добавляется на счет Незавершенное производство (НЗП), связанный с производственным потоком. Это поведение напоминает поведение для материала, выданного в производственный заказ. Тот же принцип может применяться к продуктам и полуфабрикатам. Если эти продукты не создаются, не перемещаются и не потребляются в пределах производственного потока, проводки по запасам не являются обязательными. После того, как продукты разнесены в запасы, сальдо счета НЗП для производственного потока уменьшается путем вычитания соответствующих стандартных затрат.

## <a name="value-streams-and-value-stream-mapping"></a>Потоки создания ценности и картирование потока создания ценности
Архитектура бережливого производства для Dynamics AX продиктована 5 принципами бережливого производства, сформулированными Вумеком и Джонсом: определить ценность продукта для потребителя, определить поток создания ценности для этого продукта, обеспечить непрерывное течение потока создания ценности продукта, позволить потребителю вытягивать продукт, стремиться к совершенству. Один утвержденный метод для внедрения решений Бережливого производства в физическом мире производства — картирование потока создания ценности (VSM). Этот метод был введен Розером и Шуком в их издании «Учась видеть», изданным Lean Manufacturing Institute. В Dynamics AX поток создания стоимости в будущем состоянии может быть смоделирован в виде версии производственного потока. Все процессы потока создания ценности моделируются как мероприятия процесса. Перемещения или переносы могут моделироваться в виде мероприятий перемещения, если статус перемещения должен регистрироваться, или если требуется интеграция с комплектацией запасов или консолидированными отгрузками. Сам поток создания ценности моделируется как операционная единица в Dynamics AX. Поэтому поток создания ценности можно использовать как финансовая аналитика.

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Расчет себестоимости для бережливого производства на основе производственного потока
Периодическая консолидация затрат на производственный поток позволяет скорректировать связанный счет НЗП и делает возможным определение отклонений для продуктов, поставляемых производственным потоком.

## <a name="continuous-improvement"></a>Непрерывное совершенстование
Для поддержки непрерывного совершенствования производственные потоки реализуются в виде привязанных ко времени версий. Поэтому существующую версию производственного потока, совместно со всеми связанными правилами канбана, можно скопировать в следующую версию производственного потока. Кроме того, производственный поток в будущем состоянии можно моделировать до его утверждения и активации для производства. Существующие канбаны из старых версий производственного потока автоматически связываются с новой версией, чтобы обеспечить беспрепятственное движение материалов на дату перехода и после нее.

## <a name="simplicity"></a>Простота
Для реализации бережливого производства в Microsoft Dynamics AX мы выбрали подход, основанный на производственном потоке и мероприятиях, который позволяет моделировать и простые, и сложные производственные сценарии в рамках единой масштабируемой архитектуры. При более тщательном рассмотрении концепции мероприятий очевидной становится простота для тех пользователей, которым она нужна: работников цеха и логистических работников. За счет отчетности по заданиям, основанным на мероприятиях, а не проводкам по запасам, и унифицированного пользовательского интерфейса для всех вариантов бережливого производства сложность переносится из пользовательского интерфейса туда, где ей место: в производственный поток как основу бережливого производства.

