---
title: Утверждение поставщиков для определенных продуктов
description: В этой процедуре показано, как утвердить поставщиков для определенных продуктов.
author: GalynaFedorova
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5092012f27dd03343410d30d15cae11ad20ce052
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670169"
---
# <a name="approve-vendors-for-specific-products"></a>Утверждение поставщиков для определенных продуктов

[!include [banner](../../includes/banner.md)]

В этой процедуре показано, как утвердить поставщиков для определенных продуктов. Это позволяет контролировать, каких поставщиков можно использовать при добавлении продукта в заказ на покупку. Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные. Обычно эту задачу выполняет менеджер по закупкам.

1. В области перехода выберите **Модули > Управление сведениями о продукте > Продукты > Выпущенные продукты**.
2. В списке найдите и выберите требуемую запись.
3. В списке перейдите по ссылке в выбранной строке.
4. Разверните экспресс-вкладку **Покупка**. Если в поле **Поставщик** отображается основной поставщик, необходимо добавить этого поставщика в качестве утвержденного поставщика на следующих шагах. Запишите номер поставщика, если он отображается.  
5. В области действий щелкните **Покупка**.
6. Щелкните **Настройка**.
7. Нажмите кнопку **Добавить**.
8. В поле "Поставщик" введите или выберите значение. Выберите утвержденного поставщика. Хотя бы одна из строк должна быть основным поставщиком, если она присутствовала в записи продукта. Если вы заполнили номер поставщика ранее, выберите его здесь.  
9. В поле **Истечение срока** введите дату. Выберите дату через несколько месяцев в будущем.  
10. Нажмите кнопку **Добавить**.
11. В поле **Поставщик** введите или выберите значение.
12. В поле **Истечение срока** введите дату. Выберите дату, отличную от предыдущей даты окончания срока действия.  
13. Закройте страницу.
14. На панели операций щелкните **Утвержденные поставщики**.
15. В поле **Истечение срока** введите дату. Эта дата выступает в роли фильтра, чтобы можно было просмотреть, какие поставщики были утверждены до определенной даты.  
16. Закройте страницу.
17. На панели операций щелкните **Период действия**.
18. В поле **Показать поставщиков, срок действия утверждения которых заканчивается до** введите дату. Эту страницу можно использовать для определения поставщиков, срок действия статуса утверждения которых заканчивается после определенной даты.  
19. Закройте страницу.
20. Выберите **Изменить**.
21. В поле **Способ проверки утвержденных поставщиков** выберите параметр. Это поле позволяет выбрать политику в случае, если продукт добавляется к строке заказа на покупку, в которой поставщик не является утвержденным поставщиком.  
22. Нажмите кнопку **Сохранить**.
23. Закройте страницу.
24. Закройте страницу.
25. В области перехода выберите **Модули > Закупки и источники > Поставщики > Отношения поставщика и номенклатуры > Список утвержденных поставщиков по номенклатуре**. На этой странице представлен обзор всех продуктов и утвержденных поставщиков.  
26. Закройте страницу.
27. В область переходов выберите **Модули > Закупки и источники > Поставщики > Все поставщики**. Также можно начать с поставщика, а затем перейти в список утвержденных продуктов для этого счета поставщика.  
28. В списке найдите и выберите требуемую запись.
29. На панели операций щелкните **Закупки**.
30. Щелкните **Список утвержденных поставщиков по поставщикам**.
31. Закройте страницу.
32. Закройте страницу.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]