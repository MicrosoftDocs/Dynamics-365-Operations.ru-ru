---
title: Создание состояния жизненного цикла продукта для исключения продуктов из сводного планирования
description: В этой процедуре показано, как создать новое состояние жизненного цикла продукта, которое исключает продукты из сводного планирования и расчета уровня спецификации.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 156972cdbf4ffb02b01b00972cc83d003d941378
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567753"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Создание состояния жизненного цикла продукта для исключения продуктов из сводного планирования

[!include [task guide banner](../../includes/task-guide-banner.md)]

В этой процедуре показано, как создать новое состояние жизненного цикла продукта, которое исключает продукты из сводного планирования и расчета уровня спецификации.


## <a name="create-an-obsolete-state"></a>Создание устаревшего состояния
1. Перейдите в раздел "Управление сведениями о продукте" > "Настройка" > "Состояние жизненного цикла продукта".
2. Щелкните "Создать".
3. В поле "Состояние" введите значение.
4. Выберите "Нет" в поле "Активен для планирования".
5. В поле "Описание" введите значение.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>Связь устаревшего состояния с выпущенным продуктом
1. Закройте страницу.
2. Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".
3. Используйте экспресс-фильтр для поиска записей. Например, отфильтруйте поле "Имя поиска" по значению "M00".
4. Щелкните "Изменить".
5. В списке пометьте выбранную строку.
6. В поле "Состояние жизненного цикла продукта" введите или выберите значение.

