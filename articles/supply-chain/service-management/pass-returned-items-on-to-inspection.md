---
title: Передача возврата на проверку
description: При регистрации возвращенной номенклатуры имеется возможность определить, что номенклатуру следует отправить для инвентаризации перед возвращением на склад или списать ее другим способом.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 959df8e1ecbc493dc11e4793120f352b94b8b635
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676757"
---
# <a name="pass-returned-items-on-to-inspection"></a>Передача возврата на проверку 

[!include [banner](../includes/banner.md)]


При регистрации возврата имеется возможность определить, что номенклатуру следует отправить для инвентаризации перед возвращением на склад или списать ее другим способом.

1.  Щелкните **Управление запасами** \> **Журналы** \> **Прибытие номенклатуры** \> **Прибытие номенклатуры**.
    
    \-или-
    
    Щелкните **Управление запасами** \> **Журналы** \> **Прибытие номенклатуры** \> **Получение из производства**.

2.  Регистрация прихода номенклатуры выполняется обычным способом в форме **Журнал местоположений**.
    

    > [!NOTE]
    > <P>Для получения дополнительных сведений о регистрации прихода возврата см. раздел <A href="register-the-receipt-of-returned-items.md">Регистрация прихода возврата</A>.</P>



3.  На вкладке **Значения по умолчанию**, в области **Режим обработки** выберите поле **Управление карантином**.

Это приведет к созданию в системе карантинного заказа, и человек или подразделение, выполняющие инвентаризации, ответит на этот заказ с помощью формы **Карантинный заказ**.

## <a name="see-also"></a>См. также

[Прохождение возвратом процедуры проверки](take-returned-items-through-inspection.md)

[Определение порядка списания возврата](specify-how-to-dispose-of-returned-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]