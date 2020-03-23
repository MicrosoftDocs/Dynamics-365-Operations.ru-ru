---
title: Создание юридических лиц
description: В этом разделе описывается создание юридических лиц в Microsoft Dynamics 365 Commerce, которые должны быть созданы и настроены перед созданием каналов.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 28cbcc42505f1dc90c420adc812735841541c8e0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002412"
---
# <a name="create-legal-entities"></a>Создание юридических лиц


[!include [banner](includes/banner.md)]

В этом разделе описывается создание юридических лиц в Microsoft Dynamics 365 Commerce, которые должны быть созданы и настроены перед созданием каналов.

## <a name="overview"></a>Обзор

Юридическое лицо — это организация, имеющая зарегистрированную или узаконенную правовую структуру. Юридические лица могут заключать юридические соглашения и обязаны подготавливать отчетность по результатам своей деятельности.

Компания — это тип юридического лица. В настоящее время компании являются единственным доступным для создания типом юридического лица. Каждое юридическое лицо имеет свой ИД компании. Эта связь существует, поскольку некоторые функциональные области программы используется код компании или код *DataAreaId* в своих моделях данных. В этих функциональных областях компании используются в качестве границы для обеспечения безопасности данных. Пользователи могут осуществлять доступ только к данным компании, вход в систему которой они выполнили. 

При создании канала необходимо указать юридическое лицо, к которому относится данный канал.

## <a name="create-a-new-legal-entity"></a>Создание юридического лица

Чтобы создать юридическое лицо в Dynamics 365 Commerce, выполните следующие действия.

1. В области переходов перейдите **Модули \> Настройка центрального офиса \> Юридические лица**.
1. В области действий выберите **Создать**. В правой части появится **Новое юридическое лицо**.
1. В поле **Имя** введите значение.
1. В поле **Компания** введите значение.
1. В поле **Страна/регион** введите или выберите значение.
1. Нажмите **ОК**. 

   ![Создание юридического лица](media/legal-entities.png)

1. В разделе **Общее** укажите следующие общие сведения о юридическом лице: 
   1. Введите Краткое наименование, если Краткое наименование необходимо. Краткое наименование — это альтернативное имя, которое можно использовать для поиска этого юридического лица. 
   1. Выберите используется ли это юридическое лицо как консолидированная компания.
   1. Выберите используется ли это юридическое лицо как Компания элиминирования. 
   1. Выберите **язык по умолчанию** для юридического лица. 
   1. Выберите **часовой пояс** для юридического лица.
1. В разделе **Адреса** выберите **Изменить**, чтобы ввести информацию об адресе, например название улицы, номер дома, почтовый индекс и название города.
1. В разделе **Контактная информация** введите сведения о методах связи, например адреса электронной почты, URL-адреса и номера телефонов.
1. В разделе **Предусмотренная отчетность** введите регистрационные номера, которые используются для предусмотренной отчетности.
1. В разделе **Регистрационные номера** введите любую информацию, требуемую юридическим лицом.
1. В разделе **Сведения о банковском счете** введите банковские счета и внутренние номера для юридического лица.
1. В разделе **Внешняя торговля и логистика** введите сведения об отгрузке для юридического лица.
1. В разделе **Номерные серии** можно просмотреть номерные серии, которые связаны с юридическим лицом. Это значение будет пустым.
1. В разделе **Изображение на панели мониторинга** просмотрите или измените изображение эмблемы или панели мониторинга, связанной с юридическим лицом.
1. В разделе **Налоговая регистрация** введите регистрационные номера, которые используются для отчета в налоговые органы.
1. В разделе **Налог по форме 1099** введите сведения 1099 для юридического лица.
1. В разделе **Информация о налогах** введите информацию о налогах для юридического лица.
1. Нажмите **Сохранить**.

На следующем рисунке показаны сведения с примером юридического лица.

![Общий раздел юридического лица](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор организаций и организационных иерархий](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Планирование организационной иерархии](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Организационные иерархии](channels-org-hierarchies.md)

[Обзор каналов](channels-overview.md)

[Необходимые условия для настройки каналов](channels-prerequisites.md)