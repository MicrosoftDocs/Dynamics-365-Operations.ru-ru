---
title: Разбивка стандартного отклонения стоимости
description: В этой статье содержится информация о настройке профилей разноски для стандартного расчета себестоимости.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: e7b2d04f32b75dbd1354b3ef74a41ea1b6469c8a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894887"
---
# <a name="standard-cost-variance-posting"></a>Разбивка стандартного отклонения стоимости

При использовании стандартной себестоимости для одного или нескольких продуктов в организации необходимо настроить [необходимые условия для стандартного расчета себестоимости](/supply-chain/cost-management/prerequisites-standard-costs.md). В этой статье описываются счета разноски, необходимые для шага 3 предварительных условий «Назначение счетов главной книги для разносок номенклатур, связанных с отклонениями в стандартной стоимости».

Для покупок и заказов на производство могут использоваться различные типы отклонений Примеры отклонения цены производства от себестоимости см. в разделе [Общие источники отклонения цены](/supply-chain/cost-management/common-sources-of-production-variances.md). Расхождения по цене по заказу на покупку происходит при использовании стандартной себестоимости для приобретенной номенклатуры, и существует разница между стандартной себестоимостью продукта и суммой накладной в заказе на покупку.

## <a name="sample-posting-profile-configuration"></a>Образец конфигурации профиля разноски

В следующей таблице показаны примеры типов разноски по умолчанию. Показаны образцы счетов ГК и описаний.

- Столбец "Дебет/кредит?" столбец указывает, является ли транзакция обычно дебетовой или кредитовой. В некоторых случаях проводка может разносить как дебет или как кредит.
- Столбец «Клиринговый счет» показывает, что типом разноски является клиринговый счет. Другими словами, сумма, разнесенная на этот счет, автоматически реверсируется при разноске более поздней проводки.
- В столбце «P/F» указывается тип разноски. «P» представляет физическую разноску, а «F» представляет финансовую разноску.
- В столбце «Следовать» указывается, совпадает ли обычно счет ГК для конкретного типа разноски со счетом ГК другого типа разноски. В частности, он указывает тип разноски, который обычно используется.

> [!NOTE]
> Счета ГК и имена счетов ГК в таблице являются рекомендуемыми. Рекомендуется работать с вашим бухгалтером, чтобы определить оптимальную конфигурацию для потребностей вашего бизнеса.

| Тип разноски | Пример счета главной книги | Пример названия счета главной книги | Тип счета | Дебет/кредит? | Клиринговый счет | P/F | Наследовать | Описание |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Отклонение по цене покупки | 510310 | Отклонение по цене покупки | Расход | Любой из | Нет | П | Неприменимо | Этот счет используется, если имеется расхождение между ценой покупки и стандартными затратами в заказе на покупку. |
| Переоценка складских затрат | 510330 | Переоценка складских затрат | Расход | Любой из | Нет | П | Неприменимо | Этот счет используется при активации новой версии учета затрат для номенклатуры со стандартной себестоимостью для переоценки запасов в наличии |
| Расхождение из-за изменения стоимости | 510320 | Расхождение из-за изменения стоимости | Расход | Любой из | Нет | П | Неприменимо | Этот счет используется, если имеется разница в стандартной себестоимости между сайтами или если номенклатура возвращена и имеется изменение между исходной стандартной себестоимостью и текущей стандартной себестоимостью продукта. |
| Расхождение по размеру производственного лота | 510370 | Расхождение по размеру производственного лота | Расход | Любой из | Нет | П | Неприменимо | Этот счет используется, если имеются различия между основой расчета спецификации и фактическим количеством для расчета себестоимости производственного заказа. |
| Расхождение по производственной цене | 510340 | Расхождение по производственной цене | Расход | Любой из | Нет | П | Неприменимо | Этот счет используется, если имеются различия цены между оценочными затратами и фактическими затратами для производственного заказа. |
| Расхождение по производственному количеству | 510350 | Расхождение по производственному количеству | Расход | Любой из | Нет | П | Неприменимо | Этот счет используется, если имеются различия количества между оценочными затратами и фактическими затратами для производственного заказа. |
| Расхождение по производственному замещению | 510360 | Расхождение по производственному замещению | Расход | Любой из | Нет | П | Неприменимо | Этот счет используется, если в производственном заказе имеется непредвиденное потребление. |
| Расхождение из-за округления | 618160 | Расхождение из-за округления | Расход | Любой из | Нет | П | Неприменимо | Этот счет используется, если имеется разница округления, когда производственные затраты рассчитываются по стандартным затратам. |