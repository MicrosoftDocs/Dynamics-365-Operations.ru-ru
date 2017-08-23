--- 
title: "Создавать заказы на продажу"
description: "Следующая процедура используется для создания заказа на продажу."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 62276765e1cc76b2328a7b5b57bd18593d93e4ab
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-orders"></a>Создавать заказы на продажу

[!include[task guide banner](../../includes/task-guide-banner.md)]

Следующая процедура используется для создания заказа на продажу. Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF. Заказы на продажу обычно создаются обработчиком заказов на продажу. 




## <a name="enter-sales-order-header-details"></a>Ввод сведений заголовка заказа на продажу
1. Перейдите в раздел "Продажи и маркетинг" > "Заказы на продажу" > "Все заказы на продажу".
2. Щелкните "Создать".
3. В поле "Счет клиента" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
4. В списке найдите и выберите запись клиента.
    * В данном примере выберите номер клиента US-004.  
5. В списке перейдите по ссылке в выбранной строке.
6. Нажмите кнопку "OК".

## <a name="enter-sales-order-line-details"></a>Ввод сведений строки заказа на продажу
    * Продукты, проданные организацией, могут иметь варианты, отличающиеся по аналитикам, таким как конфигурация, размер, цвет и стиль. Кроме того, продукты могут быть настроены для использования аналитик хранения, таких как сайт, склад и паллета, и аналитик отслеживания, таких как партия и серийные номера. Если эти аналитики назначены, необходимо выбрать значения для этих аналитик в строке заказа. Для повышения эффективности ввода заказа может потребоваться добавить соответствующие поля аналитик в сетку заказа.  
1. Щелкните "Строка заказа на продажу".
2. Щелкните "Аналитики".
    * В этом примере выберите аналитики "Цвет", "Сайт" и "Склад". Выбранные аналитики отобразятся в сетке заказа на продажу. Если требуется сохранить выбранные значения, задайте для параметра "Сохранить настройки" значение "Да".   
3. Нажмите кнопку "OК".
4. В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
5. В этом примере выберите код номенклатуры T0004.
6. В списке перейдите по ссылке в выбранной строке.
    * Если номенклатура является частью категории продаж, имя номенклатуры автоматически отображается в поле "Категория продаж".  
    * Если в полях аналитик продукта уже содержатся значения, это значит, что значения были скопированы из записи продукта, где они были определены как аналитики продукта по умолчанию. Значение по умолчанию можно изменить в любой момент.   
7. В поле "Цвет" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
8. Поиск и выбор требуемой записи в списке.
9. В списке перейдите по ссылке в выбранной строке.
10. В поле "Количество" введите число.
    * Если номенклатура продается в единицах измерения, отличных от единиц измерения, используемых при ее покупке, производстве и хранении, и единица измерения продажи указана в записи продукта, это значение будет отображаться в поле "Единица измерения". Значение можно изменить в любое время.   
    * Если в поле "Сайт" уже содержится значение, это значение было скопировано из заголовка заказа или из настроек заказа, связанных с продуктом. Значение можно изменить в любое время. Если это поле пусто, выберите значение.   
    * Если в поле "Цена за единицу" уже содержится значение, это значение было скопировано из допустимого коммерческого соглашения или из записи продукта. (Также может использоваться цена за единицу из договора продажи, но процесс создания заказов на продажу из договоров продажи отличается от указанного здесь процесса.) Если это поле пусто, введите значение.   
    * В поле "Скидка" содержится сумма скидки на единицу продукта. Для расчета общей суммы скидки по строке значение скидки умножается на количество строки.    Если в поле "Скидка" уже содержится значение, это значение было скопировано из допустимого коммерческого соглашения. Если это поле пусто и требуется предоставить скидку по строке клиенту, введите значение.  
    * В поле "Процент скидки" содержится процентное значение, на которое снижается общая валовая сумма по строке.  Если в поле "Процент скидки" уже содержится значение, это значение было скопировано из допустимого коммерческого соглашения. Если это поле пусто и требуется предоставить скидку по строке клиенту, введите значение.  
    * В поле "Чистая сумма" содержится значение, рассчитанное на основании количества и цены за единицу строки, скорректированной с учетом скидки.  Можно переопределить рассчитанное значение другим.  

## <a name="review-the-order-totals"></a>Просмотр итогов по заказу
1. В области действий щелкните "Заказ на продажу".
2. Щелкните "Итоги".
    * На странице "Итоги" отображаются сведения обо всем заказе. Сюда входит промежуточная сумма, которая является суммой всех чистых сумм по строкам, скорректированных с учетом окончательных скидок по строке, итоговая сумма накладной, которая является промежуточной суммой, скорректированной с учетом окончательной скидки на уровне заказа, накладных расходов и налога, кредитный лимит клиента и т. д.  Сумма накладной — это сумма, которая отображается в документе накладной клиента.  
3. Нажмите кнопку "OК".

