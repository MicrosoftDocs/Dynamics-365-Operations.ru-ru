---
title: "Мониторинг консигнационных запасов в рамках совместной работы с поставщиком"
description: "Эта процедура показывает порядок использования совместной работы с поставщиками для просмотра сведений об уровне запасов продукта, который был помещен в коносамент у клиента."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ad4868991226aef21a0410860e3f98d11901ffbb
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a>Мониторинг консигнационных запасов в рамках совместной работы с поставщиком

[!include[task guide banner](../../includes/task-guide-banner.md)]

Эта процедура показывает порядок использования совместной работы с поставщиками для просмотра сведений об уровне запасов продукта, который был помещен в коносамент у клиента. Вы также можете контролировать потребление запасов, когда клиент принимает на себя владение запасами. Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF. Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.


## <a name="view-consumed-inventory"></a>Просмотр израсходованных запасов
1. Перейдите в раздел "Совместная работа с поставщиками" > "Консигнационные запасы" > "Продукты, полученные из консигнационных запасов".
    * В списке отображаются строки поступления продуктов, которые были созданы при изменении владельца консигнационных запасов с поставщика на клиента. Может потребоваться прокрутить вправо, чтобы просмотреть количества и другие сведения. Можно использовать сведения в этом списке для создании накладных для клиента. Можно также экспортировать данные в Microsoft Excel.   
2. Щелкните "Просмотр заказа на покупку".
3. Разверните раздел "Сведения о строке".
    * Строка помечается как коносамент, и в разделе заголовка указывается, что заказ на покупку имеет статус "Получено".  
4. Закройте страницу.

## <a name="view-on-hand-inventory"></a>Просмотр запасов в наличии
1. Перейдите в раздел "Совместная работа с поставщиками" > "Консигнационные запасы" > "Консигнационные запасы в наличии".
    * Страница "Консигнационные запасы в наличии" показывает запасы, принадлежащие вам на складе клиента. Можно показать дополнительные аналитики, такие как сайт и склад, выбрав вкладку "Отобразить аналитики".   
