---
title: Что нового и что изменилось в Dynamics 365 Talent (7 января 2020 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974438"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Что нового и что изменилось в Dynamics 365 Talent (7 января 2020 г.)

В этой статье описываются новые и измененные компоненты в Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Изменения в Attract

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Изменения в Onboard

Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Изменения в Core HR

Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2697. Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>Не удается удалить работников, не имеющих записей о занятости (386157)

Это изменение добавляет параметр удаления в форме **Сотрудники без занятости**. Работники отображаются в этой форме, если для данного сотрудника не существует будущего, активного или исторического трудоустройства. В этом выпуске удаление разрешено только для системных администраторов. Однако в выпуске следующей недели система безопасности будет обновлена, чтобы позволить всем пользователям с ролью помощника в отделе кадров удалить сотрудников без занятости. Эти изменения также можно выполнить вручную, выполнив следующие действия:

1. Перейдите **Конфигурация безопасности**.
2. На вкладке **Привилегии** отфильтруйте список **Привилегии** до **Ведение работников**.
3. В столбце **Ссылки** выберите **Пункты меню отображения**.
4. В **Пункты меню отображения** выберите **HcmWOrkersWithoutEmployment**.
5. Установите разрешение **Удалить** как "Разрешить".
6. Перейдите на вкладку **Неопубликованные объекты**.
7. Выберите **Опубликовать все**.
