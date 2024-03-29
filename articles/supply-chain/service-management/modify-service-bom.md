---
title: Изменение спецификации обслуживания
description: Изменение спецификации обслуживания.
author: sorenva
ms.date: 05/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0aac9bf0f312052160b29be606ba587f2de0184
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014676"
---
# <a name="modify-a-service-bom"></a>Изменение спецификации обслуживания 

[!include [banner](../includes/banner.md)]


Можно записать историю элемента в спецификации обслуживания. Каждый раз при обновлении строки спецификации в области **История** создается строка истории. В строке истории указывается текущее состояние строки спецификации.

## <a name="update-a-service-bom-element"></a>Обновление элемента спецификации обслуживания

1.  Щелкните **Управление сервисным обслуживанием** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.

2.  Щелкните **Изменить**, чтобы открыть форму сведений **Соглашения о сервисном обслуживании**.

3.  В разделе **Панель операций** щелкните **Объекты сервисного обслуживания**, чтобы открыть форму **Объекты сервисного обслуживания**.

4.  Выберите объект, для которого требуется обновить строку спецификации, а затем щелкните **Конструктор**.

5.  В форме **Конструктор** выберите обновляемую строку спецификации, а затем нажмите кнопку **Редактировать строку спецификации**.
    
    > [!NOTE]
    > <P>На вкладке <STRONG>Настройка</STRONG> установите флажок <STRONG>Редактир. при добавл.</STRONG>, если требуется открыть форму <STRONG>Редактирование строки спецификации</STRONG> при перетаскивании строки в спецификацию обслуживания.</P>

6.  В поле **Количество** введите количество.

7.  Установите флажок **Создать строку заказа на обслуживание**, если необходимо создать строку заказа на обслуживание для элемента замены, по которой затем можно выставить накладную.

8.  Щелкните **OK**, чтобы закрыть форму.

## <a name="delete-a-service-bom-line"></a>Удаление строки спецификации обслуживания

1.  Щелкните **Управление сервисным обслуживанием** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.

2.  Щелкните **Изменить**, чтобы открыть форму сведений **Соглашения о сервисном обслуживании**.

3.  В разделе **Панель операций** щелкните **Объекты сервисного обслуживания**, чтобы открыть форму **Объекты сервисного обслуживания**.

4.  Выберите объект, из которого требуется удалить строку спецификации обслуживания, а затем щелкните **Конструктор**.

5.  В форме **Конструктор** выберите удаляемую строку спецификации, а затем нажмите кнопку **Удалить строку спецификации**.

## <a name="see-also"></a>См. также

[Шаблоны спецификаций](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]