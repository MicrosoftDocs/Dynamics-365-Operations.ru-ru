---
title: Настройка общих параметров
description: Необходимо настроить общие параметры для записей, которые используются совместно несколькими компаниями, например записи должностей. В этой статье описывается, как настроить параметры модуля "Управление персоналом" в разных юридических лицах.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 888caa19a9befd32ce27b27e499cdfe88a1bbf01
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054532"
---
# <a name="configure-shared-parameters"></a>Настройка общих параметров

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Необходимо настроить общие параметры для записей, которые используются совместно несколькими компаниями, например записи должностей. В этой статье описывается, как настроить параметры модуля "Управление персоналом" в разных юридических лицах.

Некоторые типы записей, такие как записи "Должность", используются сразу несколькими компаниями. Для этих записей необходимо настроить общие параметры. Например, страница **Совместно используемые параметры управления персоналом** используется для задания параметров модуля "Управление персоналом", общих для нескольких юридических лиц. 

На странице **Совместно используемые параметры управления персоналом** параметры сгруппированы в разделы в зависимости от их функциональности. 

### <a name="previously-released-functionality"></a>Ранее выпущенная функциональность
На вкладке **Идентификация** необходимо выбрать типы идентификации, представляющие идентификационные номера, перечисленные на странице. Перед вводом идентификационных сведений для работников можно настроить типы документов, удостоверяющих личность. Информация о номере социального обеспечения, идентификационном номере (для граждан и иностранцев) и коде удостоверения личности ведется на странице **Тип документа**. Чтобы определить новый тип удостоверяющего личность документа или просмотреть список существующих типов, выберите **Управление персоналом** &gt; **вкладка "Ссылки"** &gt; **Настройка** &gt; **Типы документов, удостоверяющих личность**. Можно ввести простой код и описание. 

### <a name="if-youre-using-dynamics-365-human-resources"></a>При использовании Dynamics 365 Human Resources
На вкладке **Идентификация** необходимо выбрать типы идентификации, представляющие идентификационные номера, перечисленные на странице. Перед вводом идентификационных сведений для работников можно настроить типы документов, удостоверяющих личность. Информация о номере социального обеспечения, идентификационном номере (для граждан и иностранцев) и коде удостоверения личности ведется на странице **Тип документа**. Чтобы определить новый тип удостоверяющего личность документа или просмотреть список существующих типов, выберите **Управление персоналом** &gt; **Настройка** &gt; **Типы документов, удостоверяющих личность**. Можно ввести простой код и описание. 

На вкладке **Номерные серии** можно выбрать номерные серии, используемые для следующих записей: табельный номер, должность, код запроса пользователя, документ по форме I-9, кандидат, обсуждение, код льготы и действие персонала (если этот тип записи включен). Для ведения ссылок и кодов номерных серий используется страница списка **Номерные серии**. Чтобы найти эту страницу, используйте функцию поиска страниц. 

На вкладке **Должности** укажите, доступны ли новые должности для назначения по умолчанию:

-   **Всегда** — можно назначать работников на новые должности при создании должностей. При создании должностей в качестве даты и времени в поле **Доступна для назначения** на вкладке **Общее** страницы **Должность** автоматически устанавливаются дата и время создания.
-   **Никогда** — назначать работников на новые должности при создании должностей нельзя. Если выбран этот параметр, вы должны открывать страницу **Должность** для каждой новой должности, когда она станет доступна, а затем на вкладке **Общее** ввести дату в поле **Доступна для назначения**, чтобы назначение работников на должность стало возможно.


[!INCLUDE[footer-include](../includes/footer-banner.md)]