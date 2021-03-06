---
title: Создание потребностей в номенклатуре для заказов на обслуживание
description: Если необходимо зарезервировать определенные номенклатуры для Заказа на сервисное обслуживание, можно создать потребность в складской номенклатуре для него.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 650d02d2160757d9629e4deb1e9217c85e9d01df
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831634"
---
# <a name="create-item-requirements-for-service-orders"></a>Создание потребностей в номенклатуре для заказов на обслуживание 

[!include [banner](../includes/banner.md)]


Можно создать заказ на сервисное обслуживание, чтобы отслеживать и управлять услугами, которые предоставляются вашим клиентам. Если необходимо зарезервировать определенные номенклатуры для Заказа на сервисное обслуживание, можно создать потребность в складской номенклатуре для него. Потребность в номенклатуре можно сразу потребить из запасов или она может запустить производственный заказ для номенклатуры.

Используя потребность в номенклатуре вместо проводки с номенклатурой, можно запланировать поставку перед самым моментом использования данной номенклатуры, создать заказ на покупку, включить номенклатуру в схему коммерческих соглашений, и использовать потребность в номенклатуре при планировании производства.

Потребности в номенклатуре для заказов на обслуживание обрабатываются с помощью проекта. Для создания потребности в номенклатуре в заказе на сервисное обслуживание заказ на обслуживание необходимо назначить проекту. После создания потребности в номенклатуре для заказа на сервисное обслуживание можно просмотреть потребность в номенклатуре в форме **Проекты** для выбранного проекта.

## <a name="create-an-item-requirement-for-a-service-order"></a>Создание потребности в номенклатуре для заказа на сервисное обслуживание

1.  Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.

2.  Выберите заказ на сервисное обслуживание, для которого необходимо создать потребность в номенклатуре.

3.  В разделе **Панель операций** на вкладке **Отправка** выберите **Потребность в номенклатуре**.

4.  В форме **Потребности в номенклатуре** введите сведения для требуемой номенклатуры. Дополнительные сведения об отдельных полях см. в разделе [Потребности в номенклатуре (форма)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Создание потребности в номенклатуре для соглашения о сервисном обслуживании

1.  Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.

2.  Откройте соглашение о сервисном обслуживании, для которого необходимо создать потребность в номенклатуре.

3.  На экспресс-вкладке **Строки** щелкните **Добавить**, чтобы создать новую строку.

4.  В поле **Тип проводки** выберите **Номенклатура**.

5.  В поле **Настройка номенклатуры** выберите **Потребность в номенклатуре**.

6.  В поле **Код номенклатуры** выберите номенклатуру, которая требуется для соглашения о сервисном обслуживании обслуживание.

7.  На экспресс-вкладке **Сведения о строке** на вкладке **Аналитики продуктов** в поле **Сайт** выберите сайт запасов для номенклатуры.

8.  Чтобы создать заказ на сервисное обслуживание из данной строки соглашения, на экспресс-вкладке **Строки** щелкните **Создать заказы на сервисное обслуживание** и введите необходимую информацию в форму **Создать заказы на сервисное обслуживание**. 


## <a name="see-also"></a>См. также

[Автоматическое создание заказов на обслуживание](create-service-orders-automatically.md).

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]