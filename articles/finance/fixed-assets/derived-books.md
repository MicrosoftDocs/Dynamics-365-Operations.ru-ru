---
title: Производные книги
description: Эта статья содержит обзор функции производной книги.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c31116ba234bd1fce445ac382fe8f8aea263a66
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769485"
---
# <a name="derived-books"></a>Производные книги

[!include [banner](../includes/banner.md)]

Эта статья содержит обзор функции производной книги.

Целью производных книг является упрощение разноски проводок книги основных средств, которые планируются для регулярных интервалов.  Одну книгу следует выбрать как основную книгу. Обычно это книга, которая используется для бухгалтерской амортизации. Затем она присоединяется к другим книгам, настроенным для разноски проводок для интервалов, аналогичных интервалам в первичной книге. Книги налоговой амортизации часто настраиваются как производные книги. 

Проводками, для которых наиболее часто выполняется настройка разноски в производных книгах, являются приобретения, корректировки приобретений и выбытия. 

## <a name="example"></a>Пример

Книги B и C настраиваются как производные книги для книги A для типа проводки "Приобретения". В книге A введите проводку приобретения для актива 123 на 1500,00. 

Когда выполняется разноска проводки, создается проводка приобретения в активе 123 для книги B и в активе 123 для книги C на 1500,00. При подготовке проводок этой основной книги к разноске в журнал основных средств также можно просмотреть и изменить проводки производных книг. При подготовке проводок первичной книги в другом журнале проводки производной стоимости не отображаются. Однако они разносятся на соответствующие счета и уровни разноски, когда выполняется разноска проводок первичной книги.

> [!NOTE]                                                                                                                               
> Книги, которые настраиваются в проводках разноски на интервалах, отличных от интервалов первичной книги, должны присоединяться к основным средствам в качестве отдельных книг, а не в виде производных книг.  

Дополнительные сведения см. в разделе [Разноска с производными книгами](post-derived-value-models.md).


