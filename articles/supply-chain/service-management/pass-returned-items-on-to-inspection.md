---
title: "Передача возврата на проверку"
description: "При регистрации возвращенной номенклатуры имеется возможность определить, что номенклатуру следует отправить для инвентаризации перед возвращением на склад или списать ее другим способом."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4a60e6635e3bb1723ced7aba1a71135116b53272
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

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


