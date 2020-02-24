---
title: Расширение Talent с помощью Power Apps и Power Automate
description: В этой статье описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Talent Attract, использующих Microsoft Power Apps и Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1051fa4db16bb94cc9d60a91fc3637d7e5305cc2
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029919"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Расширение Talent с помощью Power Apps и Power Automate

В этой статье описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Talent: Attract, использующих Microsoft Power Apps и Microsoft Power Automate. Можно импортировать пакет решения, связанный с каждым примером, в среду Power Apps. Затем можно использовать эти пакеты как руководство или как основу для реализации сценариев, которые применимы к вашей организации.

> [!IMPORTANT]
> Если вы хотите использовать шаблоны и приложения, описанные в этой статье, "как есть", обязательно проверьте их, чтобы убедиться в том, что они охватывают все сценарии, относящиеся к вашей реализации.


## <a name="prerequisites"></a>Необходимые условия

- Для импорта пакетов пользователи должны иметь разрешение **Создатель среды**.
- Для экспорта или импорта приложений пользователи должны иметь лицензию плана 2 Power Apps или пробную лицензию плана 2 Power Apps.

## <a name="power-automate--form-connect"></a>Power Automate — подключение формы

Шаблон **Power Automate — подключение формы** можно использовать для чтения данных из Microsoft Forms и сохранения их в объекте Common Data Service.

Этот шаблон можно расширить таким образом, чтобы его можно было использовать для других сценариев. Далее приводятся некоторые примеры.

- Запись оценок кандидатов.
- Запись результатов из анкет для курса.
- Компиляция библиотеки вопросов собеседования для администраторов отдела кадров (HR).
- Запись оценки кандидатом процесса собеседования

В Microsoft Dynamics 365: Attract можно использовать формы на портале кандидата, где кандидаты могут заполнять сведения. Формы можно также внедрить как действия в шаблон должности.

Когда кандидат отправляет форму, Microsoft Power Automate записывает отправку формы, считывает данные и сохраняет их в объекте Common Data Service.

Для загрузки шаблона **Power Automate — подключение формы** и структуры пользовательского объекта, перейдите к [Power Automate — подключение формы](https://go.microsoft.com/fwlink/?linkid=2081988) в центре загрузки Майкрософт.

## <a name="power-automate--sharepoint-integration"></a>Power Automate — интеграция SharePoint

Шаблон **Power Automate — интеграция с SharePoint** может использоваться для чтения данных из списка Microsoft SharePoint, сравнения списка со значениями полей для любого объекта Common Data Service и отправить результаты сравнения в виде уведомления по электронной почте. 

Организация может иметь набор навыков, которые требуются срочно. Эти навыки могут храниться в SharePoint в виде списка SharePoint. Когда кандидат подает заявление для любой должности, для которой перечислен набор необходимых навыков, если существует значительное соответствие между навыками кандидата и навыками, которые хранятся в SharePoint, отправляется уведомление по электронной почте. Таким образом должности, которые требуются срочно, заполняются быстрее, поскольку уведомления помогают агентам по найму связываться с кандидатами и выполнять кросс-наем кандидатов в организации.

Этот шаблон можно расширить таким образом, чтобы он мог использоваться для любого сценария, который включает в себя интеграцию SharePoint.

Чтобы загрузить шаблон **Power Automate — интеграция SharePoint**, выберите [Power Automate — интеграция SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) в центре загрузки Майкрософт.

## <a name="referral-app"></a>Приложение ссылки

Для добавления кандидатов в общий кадровый пул можно использовать приложение ссылки. Источник ссылки может ввести значения **Имя**, **Фамилия**, **Адрес электронной почты** и **URL-адрес LinkedIn** при отправке кандидата. Метаданные источника кандидата заполняются информацией об источнике ссылки.

Это приложение можно встроить в дистанционное обслуживание сотрудников для отправки ссылок, либо можно использовать его в качестве гиперссылки на корпоративном портале и запускать его как отдельное приложение.

Чтобы загрузить **Приложение ссылки**, перейдите по адресу [Решение расширения Dynamics 365 Talent: приложение ссылки](https://www.microsoft.com/download/details.aspx?id=58497) в центре загрузки Майкрософт. Можно импортировать это приложение и настроить его для добавления дополнительных функциональных возможностей.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Перенос приложений между клиентами и средами](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
