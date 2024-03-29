---
title: Разноска с производными книгами
description: В этой статье описывается использование производных книг.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0270ad1e66193832fb1139fca4439b36b5ffb84
ms.sourcegitcommit: dca54dd3afc7c94795d89c63050b105df2c48e3f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2022
ms.locfileid: "9682916"
---
# <a name="post-with-derived-books"></a>Разноска с производными книгами

[!include [banner](../includes/banner.md)]

В этой статье описывается использование производных книг.

При разноске проводки для книги, содержащей производные книги, проводки журнала производной амортизации автоматически разносятся из журналов, заказов на покупку или накладных с произвольным текстом. Однако если вы готовите проводки основной книги в журнале "Основные средства", можно просматривать и изменять суммы производных проводок перед их разноской.
-   Некоторые счета, например счета налогов и клиентов или поставщиков, обновляются только один раз при помощи разносок основной книги. Проводки производной книги разносятся по счетам, определенным для производной книги на странице "Профили разноски основных средств".
-   Приобретение часто используется в качестве типа проводки для производных книг. Это необходимо, когда книга и производная книга должны применяться к ОС с момента ввода ОС в эксплуатацию.
-   Для данного типа проводки могут применяться и другие значения. Например, если у основной книги и производных книг одинаковые интервалы продажи или выбытия, все типы проводок ОС доступны для настройки производной модели стоимости.

> [!WARNING]
> Сумма амортизации, разнесенная в производной книге, равна сумме, разнесенной для основной книги. Если методы амортизации для различных книг отличаются, не следует создавать проводки амортизации с использованием производного процесса. 

## <a name="example"></a>пример 
Ниже представлены сведения о способах настройки проводок приобретения с функциональностью производной книги.

1.  Создайте книги на странице "Книги".
    -   Книга для учета: VM 1, текущий слой разноски
    -   Книга для налогов: VM 2, слой разноски налога

2.  В МС 1 щелкните вкладку "Производные книги". Выберите "МС 2" в поле "Книга" и "Приобретение" в поле "Тип проводки".

Книги могут быть прикреплены к определенным ОС. 

Когда ввод в эксплуатацию разнесен для ОС с книгой МС 1, ввод в эксплуатацию разносится не только в МС 1, но также в производной книге МС 2. Статус обеих книг основных средств обновляется на "Открыта".

> [!NOTE]                                                                                                         
> Если вы не используете производные книги, необходимо разнести ввод в эксплуатацию ОС для книги МС 1 и книги МС 2.

Дополнительные сведения см. в разделе [Производные книги](derived-books.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
