---
title: Расширение Talent с помощью Power Apps и Power Automate
description: В этой статье описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Human Resources, использующих Microsoft Power Apps и Microsoft Power Automate.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4036378ca70089a9978a9bf5fb48c058a2064cdc
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689504"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Расширение с помощью Power Apps и Power Automate


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



В этой статье описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Human Resources, использующих Microsoft Power Apps и Microsoft Power Automate. Можно импортировать пакет решения, связанный с каждым примером, в среду Power Apps. Затем можно использовать эти пакеты как руководство или как основу для реализации сценариев, которые применимы к вашей организации.

> [!IMPORTANT]
> Если вы хотите использовать шаблоны и приложения, описанные в этом разделе, "как есть", обязательно проверьте их, чтобы убедиться в том, что они охватывают все сценарии, относящиеся к вашей реализации.

## <a name="prerequisites"></a>Необходимые условия

- Для импорта пакетов пользователи должны иметь разрешение **Создатель среды**.
- Для экспорта или импорта приложений пользователи должны иметь лицензию плана 2 Power Apps или пробную лицензию плана 2 Power Apps.

## <a name="integration-with-microsoft-365-power-automate"></a>Интеграция с Microsoft 365, Power Automate

Приложение **Интеграция с Microsoft 365** может использоваться для извлечения сведений о рабочей группе для выполнивших вход пользователей из Microsoft 365. Ссылается на работников в Human Resources, чтобы извлечь типы идентификации сотрудников. Менеджеры могут проверять даты окончания сроков действия типов кодов сотрудника. Кроме того, они могут отправлять напоминаниями по электронной почте, если срок действия типа кода сотрудника истекает. Power Automate интегрируется с Power Apps для отправки этого напоминания. При отправке напоминания подтверждение будет отправлено обратно в Power Apps из Power Automate. Типы идентификации включают водительское удостоверение, паспорт и другие приемлемые формы удостоверения личности.

Это приложение можно расширить для использования в других сценариях. Например, оно может использоваться для отображения сведений об отпусках рабочей группы, события календаря и любых других событиях, связанных с рабочей группой.

Чтобы загрузить шаблон приложение **Интеграция с Microsoft 365, Power Automate**, перейдите [Интеграция с Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) в центре загрузки Майкрософт.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate — подключение и выполнение SQL

Шаблон **Power Automate — подключение и выполнение SQL** подключается к Microsoft SQL Server и позволяет выполнять запросы SQL.

Хотя этот шаблон считывает и обновляет таблицы SQL, его можно расширить и использовать в других сценариях. Например, он может использоваться для заполнения промежуточной таблицы в Dataverse с записями из SQL Server, а также для периодической синхронизации промежуточной таблицы с помощью инкрементной принудительной отправки из SQL Server.

Расширенный запрос интегрируется с Flow, чтобы включить преобразование данных и выполнить инкрементную принудительную отправку.

Для загрузки шаблона **Power Automate — подключение и выполнение SQL** перейдите к пункту [Power Automate — подключение и выполнение SQL](https://go.microsoft.com/fwlink/?linkid=2081789) в центре загрузки Майкрософт.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
