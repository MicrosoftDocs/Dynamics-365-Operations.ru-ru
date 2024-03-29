---
title: Единая номерная серия для кодов заданий
description: Эта функция предоставляет одну унифицированную номерную серию, которая создает коды заданий для модулей контроля производства, управления производством, а также времени и посещаемости.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 301a4bb58f896a2dc0f0cddcd2e29344865ca898
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897555"
---
# <a name="unified-number-sequence-for-job-ids"></a>Единая номерная серия для кодов заданий

[!include [banner](../includes/banner.md)]

Эта функция предоставляет одну унифицированную номерную серию, которая создает коды заданий для модулей контроля производства, управления производством, а также времени и посещаемости. Ранее была возможность выбрать другую номерную серию для каждого из этих модулей, что может привести к конфликтующим кодам заданий, если две или более из этих последовательностей используют одинаковый формат. Такой конфликт может привести к повреждению данных.

## <a name="turn-on-this-feature-for-your-system"></a>Включите эту функцию для своей системы

Если ваша система еще не содержит функцию, описанную в этой статье, перейдите в [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) и включите функцию *Унифицированная номерная серия для кодов заданий*.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>Настройка унифицированной номерной серии для кодов заданий

После включения этой функции существующие параметры номерной серии **Код задания**, расположенные на страницах параметров для модулей контроля производства, управления производством и времени и посещаемости, будут устаревшими и будет добавлено новое поле **Унифицированный код задания**. Значение **Унифицированный код задания** совместно используется всеми тремя модулями, что гарантирует, что все модули ссылаются на одну и ту же номерную серию. Таким образом, коды заданий будут уникальными во всех трех модулях, и конфликт никогда не будет происходить.

Чтобы настроить унифицированную номерную серию для кодов заданий:

1. Включите функцию, как описано в предыдущем разделе.
1. Либо определите номерную серию, которую хотите использовать для унифицированных кодов задания, либо создайте новую. Дополнительные сведения см. в разделе [Обзор номерных серий](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).
1. Перейдите на страницу **Параметры управления производством**, **Параметры модуля "Управление производством"** или **Параметры учета посещаемости и времени присутствия**. Не важно, которую из них вы выберете, потому что при задании этого параметра на любой из этих страниц все остальные страницы обновятся автоматически.
1. Откройте вкладку **Номерные серии** на выбранной странице параметров.
1. Назначьте **Код номерной серии**, который вы идентифицировали ранее, строке **Унифицированные коды заданий** сетки.
