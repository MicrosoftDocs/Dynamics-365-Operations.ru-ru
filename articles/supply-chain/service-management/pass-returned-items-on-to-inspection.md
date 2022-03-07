---
title: Передача возврата на проверку
description: При регистрации возвращенной номенклатуры имеется возможность определить, что номенклатуру следует отправить для инвентаризации перед возвращением на склад или списать ее другим способом.
author: ShylaThompson
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdee1ed2c7e98843e5dcfe9669e6a7c1eb11173c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810686"
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