---
title: Расширение Talent с помощью Power Apps и Power Automate
description: В этой статье описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Human Resources, использующих Microsoft Power Apps и Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2e89347829ccd6569d568db42c79b5fea2316ba3
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527034"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Расширение с помощью Power Apps и Power Automate

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

В этой статье описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Human Resources, использующих Microsoft Power Apps и Microsoft Power Automate. Можно импортировать пакет решения, связанный с каждым примером, в среду Power Apps. Затем можно использовать эти пакеты как руководство или как основу для реализации сценариев, которые применимы к вашей организации.

> [!IMPORTANT]
> Если вы хотите использовать шаблоны и приложения, описанные в этом разделе, "как есть", обязательно проверьте их, чтобы убедиться в том, что они охватывают все сценарии, относящиеся к вашей реализации.

## <a name="prerequisites"></a>Необходимые условия

- Для импорта пакетов пользователи должны иметь разрешение **Создатель среды**.
- Для экспорта или импорта приложений пользователи должны иметь лицензию плана 2 Power Apps или пробную лицензию плана 2 Power Apps.

## <a name="integration-with-microsoft-365-power-automate"></a>Интеграция с Microsoft 365, Power Automate

Приложение **Интеграция с Microsoft 365** может использоваться для извлечения сведений о рабочей группе для выполнивших вход пользователей из Microsoft 365. Ссылается на работников в Human Resources, чтобы извлечь типы идентификации сотрудников. Менеджеры могут проверять даты окончания сроков действия типов кодов сотрудника. Кроме того, они могут отправлять напоминаниями по электронной почте, если срок действия типа кода сотрудника истекает. Power Automate интегрируется с Power Apps для отправки этого напоминания. При отправке напоминания подтверждение будет отправлено обратно в Power Apps из Power Automate. Типы идентификации включают водительское удостоверение, паспорт и другие приемлемые формы удостоверения личности.

Это приложение можно расширить для использования в других сценариях. Например, оно может использоваться для отображения сведений об отпусках рабочей группы, события календаря и любых других событиях, связанных с рабочей группой.

Чтобы загрузить приложение **Интеграция с Microsoft 365, Power Automate** перейдите к пункту [Интеграция с Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) в центре загрузки Майкрософт.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate — подключение и выполнение SQL

Шаблон **Power Automate — подключение и выполнение SQL** подключается к Microsoft SQL Server и позволяет выполнять запросы SQL.

Хотя этот шаблон считывает и обновляет таблицы SQL, его можно расширить и использовать в других сценариях. Например, он может использоваться для заполнения промежуточной таблицы в Common Data Service с записями из SQL Server, а также для периодической синхронизации промежуточной таблицы с помощью инкрементной принудительной отправки из SQL Server.

Расширенный запрос интегрируется с Flow, чтобы включить преобразование данных и выполнить инкрементную принудительную отправку.

Для загрузки шаблона **Power Automate — подключение и выполнение SQL** перейдите к пункту [Power Automate — подключение и выполнение SQL](https://go.microsoft.com/fwlink/?linkid=2081789) в центре загрузки Майкрософт.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]