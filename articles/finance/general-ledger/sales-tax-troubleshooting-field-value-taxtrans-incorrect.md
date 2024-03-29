---
title: Неправильное значение поля в TaxTrans
description: В этой статье содержатся сведения об устранении неполадок из-за неверных значений полей в TaxTrans.
author: EricWangChen
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6e7329ffdc04207116c92cb42e02750b176713fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899824"
---
# <a name="incorrect-field-value-in-taxtrans"></a>Неправильное значение поля в TaxTrans

[!include [banner](../includes/banner.md)]

Если значение поля в **TaxTrans** неверное, воспользуйтесь сведениями из этой статьи, чтобы попытаться разрешить проблему.

## <a name="overview-of-values"></a>Обзор значений
В следующем списке показано, как **TaxTrans**, **TaxUncommitted** и **TmpTaxWorkTrans** являются похожими наборами данных, но работают по-разному.

  - **TaxTrans** является окончательным результатом разнесенных проводок налога, которые сохранены в базе данных.
  - **TaxUncommitted** — это промежуточный рассчитанный налоговый результат, сохраненный в базе данных (если применимо), который будет использоваться в дальнейшем при разноске.
  - **TmpTaxWorkTrans** — это временный вычисленный результат в таблице в памяти (тип таблицы = InMemory).

Если вы обнаружили основную причину неправильного столбца **TaxTrans**, вы также обнаружили основную причину неправильного столбца **TaxUncommitted** или **TmpTaxWorkTrans**. Это объясняется тем, что три столбца копируются друг с другом.

Обычно в процессе расчета налога создается **TmpTaxWorkTrans**, а затем создается, если применимо, **TaxUncommitted**. При разноске налога создается **TaxTrans**.


## <a name="add-breakpoints"></a>Добавление точек останова
Выполните следующие шаги, чтобы добавить точки останова: 

1. Добавьте расширения и точки останова в *insert()* и *update()* в расширениях, как показано ниже:

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. Иди же можно добавлять точки останова непосредственно, когда **TaxUncommitted** не включен.

     - *TaxTrans.insert()*, *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>Воспроизведение и отладка

После задания точек останова во время отладки видны все изменения сохранения данных. Чтобы найти основную причину неправильного столбца в **TaxTrans**, **TaxUncommitted** или **TmpTaxWorkTrans**, проверьте и обратите внимание на следующие элементы:

- Последняя точка останова, в которой столбец является правильным.
- Первая точка останова, в которой столбец является неправильным.
- Что происходит между этими двумя точками.

## <a name="determine-whether-customization-exists"></a>Определение существования настройки
Если вы выполнили шаги в предыдущих разделах, но не смогли решить проблему, определите, существует ли настройка. Если настройка не существует, обратитесь в службу поддержки Майкрософт.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

