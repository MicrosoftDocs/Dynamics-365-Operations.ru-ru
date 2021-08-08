---
title: Организационная иерархия в Dataverse
description: Эта тема описывает интеграцию организационных данных между приложениями Finance and Operations и Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: d1ad3bc4eef1650b927d9f6dd699f788994c7e87
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542595"
---
# <a name="organization-hierarchy-in-dataverse"></a>Организационная иерархия в Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Поскольку Dynamics 365 Finance — это финансовая система, *организация* является основной концепцией, а настройка системы начинается с конфигурации организационной иерархии. Финансы бизнеса затем могут отслеживаться на уровне организации, а также на любом уровне в иерархии организации.

Хотя Dataverse не имеет понятия иерархии организации, она имеет несколько отдельных концепций, таких как общий доход от продаж. В рамках интеграции Dataverse структура данных иерархии организации добавляется в Dataverse.

## <a name="data-flow"></a>Поток данных

Бизнес-экосистема, состоящая из приложений Finance and Operations и Dataverse, будет по-прежнему иметь организационную иерархию. Эта организационная иерархия построена на приложениях Finance and Operations, но она доступна в Dataverse для целей информации и расширения. На следующей иллюстрации показана информация об иерархии организации, которая доступна в Dataverse в качестве одностороннего потока данных из приложений Finance and Operations в Dataverse.

![Изображение архитектуры.](media/dual-write-data-flow.png)

Сопоставления таблицы организационной иерархии доступны для односторонней синхронизации данных из приложений Finance and Operations в Dataverse.

## <a name="templates"></a>Шаблоны

Информация о продукте содержит все сведения, имеющие отношение к продукту и его определению, такие как аналитики продукта или аналитики отслеживания и хранения. Как показано в следующей таблице, для синхронизации продуктов и связанных сведений создается коллекция сопоставлений таблиц.

Приложения Finance and Operations | Приложения для взаимодействия с клиентами     | описание
-----------------------|--------------------------------|---
[Юридические лица](mapping-reference.md#102) | cdm_companies | Обеспечивает двунаправленную синхронизацию информации о юридическом лице (компании).
[Юридические лица](mapping-reference.md#142) | msdyn_internalorganizations |
[Операционная единица](mapping-reference.md#143) | msdyn_internalorganizations |
[Организационная иерархия — опубликованная версия](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Этот шаблон обеспечивает одностороннюю синхронизацию таблицы опубликованной организационной иерархии.
[Цели организационной иерархии](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Этот шаблон обеспечивает одностороннюю синхронизацию таблицы цели организационной иерархии.
[Тип организационной иерархии](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Этот шаблон обеспечивает одностороннюю синхронизацию таблицы типа организационной иерархии.

## <a name="internal-organization"></a>Внутренняя организация

Сведения о внутренней организации в Dataverse поступают из двух таблиц, **Операционная единица** и **Юридические лица**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
