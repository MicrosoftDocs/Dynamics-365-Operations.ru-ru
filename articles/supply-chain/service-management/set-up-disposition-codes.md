---
title: Настройка кодов метода обработки
description: Можно настроить коды расстановки для определения способа обработки номенклатуры, которая возвращена клиентом.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnDispositionCode
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16f0ddb9ad956367adc66a952bd8d12551da56a5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4435717"
---
# <a name="set-up-disposition-codes"></a>Настройка кодов метода обработки 

[!include [banner](../includes/banner.md)]


Можно настроить коды расстановки для определения способа обработки номенклатуры, которая возвращена клиентом. Например, создайте код расстановки под названием **Ремонт и возврат**, чтобы указать, что возвращенная номенклатура будет отремонтирована, а затем будет возвращена клиенту. Дополнительные примеры кодов расстановки, которые обычно используются для возвращаемых клиентами номенклатур см. в разделе [Определение порядка списания возврата](specify-how-to-dispose-of-returned-items.md).

Можно также настроить код причины, чтобы объяснить причину почему номенклатура была возвращена. Для получения дополнительных сведений о кодах причин см. раздел [Настройка кодов причин возврата](set-up-return-reason-code.md).

1.  Щелкните **Продажи и маркетинг** \> **Настройка** \> **Заказы на продажу** \> **Возвраты** \> **Коды метода обработки**.

2.  Нажмите кнопку **Создать** или нажмите сочетание клавиш CTRL+N, чтобы создать новый код расстановки.

3.  Введите уникальное описательное имя, выберите действие и введите описание для кода расстановки.

4.  Если необходимо связать какую-либо оплату клиентом с данным кодом расстановки, нажмите кнопку **Накладные расходы**, чтобы открыть форму **Настройка накладных расходов**.

5.  Если необходимо определить соответствие каких-либо внешних кодов собственным кодам методов обработки компании, нажмите кнопку **Внешние коды**, чтобы открыть форму **Внешние коды**.

## <a name="see-also"></a>См. также

[Обзор возвратов клиентами](disposition-and-return-reason-codes.md)

[Коды методов обработки (форма)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

[Автоматические затраты (форма)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))

[Форма "Внешние коды" (форма)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]