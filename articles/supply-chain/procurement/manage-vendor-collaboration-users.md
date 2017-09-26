---
title: "Управление пользователями совместной работы с поставщиками"
description: "В этом разделе описывается, как можно запросить подготовку новых пользователей модуля совместной работы с поставщиками, а также как добавлять новые контакты в модуль совместной работы с поставщиками."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: ec7ed3a81d296e9bef4d26f1756b73883d560cb5
ms.contentlocale: ru-ru
ms.lasthandoff: 06/13/2017

---

# <a name="manage-vendor-collaboration-users"></a>Управление пользователями совместной работы с поставщиками

[!include[banner](../includes/banner.md)]


В этом разделе описывается, как можно запросить подготовку новых пользователей модуля совместной работы с поставщиками, а также как добавлять новые контакты в модуль совместной работы с поставщиками. 

Интерфейс для совместной работы с поставщиками в Microsoft Dynamics 365 for Finance and Operations предоставляет внешним поставщикам информацию о заказах на покупку, накладных и складе коносамента. Можно создать новые контакты совместной работы с поставщиками и запросить настройку новых пользователей, если вы работаете как внешний поставщик с ролью безопасности **Администратор поставщика (внешний)** или аналогичными разрешениями. Также можно выполнить следующие задачи при работе в качестве специалиста по закупкам. В этом разделе эта роль ссылается на специалиста по закупкам, который работает в компании с собственным экземпляром Dynamics 365 for Finance and Operations. Дополнительные сведения о том, как использовать совместную работу с поставщиками, если вы являетесь внешним поставщиком, см. в разделе [Поставщик с клиентами](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Дополнительные сведения о том, как использовать совместную работу с поставщиками, если вы являетесь специалистом по закупкам, см. в разделе [Совместная работа с внешними поставщиками](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Добавление новых контактов в интерфейс совместной работы с поставщиками
Если вы хотите, чтобы кто-то имел доступ к совместной работе с поставщиками, его необходимо сначала добавить как контактное лицо совместной работы с поставщиками. Можно также добавить контакты для сотрудников вашей компании, которые не будут использовать совместную работу с поставщиками. Например, они могут быть контактными лицами для других типов данных по закупкам. Новые контакты добавляются на странице **Все контакты**, которую можно открыть из меню **Совместная работа с поставщиками** &gt; **Контакты**. Для добавления нового контактного лица:

1.  Нажмите **Создать**.
2.  Введите сведения о контактном лице.
3.  Выберите, какое юридическое лицо они представляет в вашей организации, и с каким юридическим лицом они будет работать в компании, с которой они будут сотрудничать. Это делается путем выбора пары **Юридическое лицо в моей компании**/**Юридическое лицо в компании клиента**.
4.  Щелкните **Создать**.

Если необходимо удалить контактное лицо, можно удалить только созданных вами.

## <a name="vendor-collaboration-user-requests"></a>Запросы пользователей совместной работы с поставщиками
Запросы пользователей для совместной работы с поставщиками могут создаваться специалистом по закупкам или администратором внешнего поставщика.

-   Если вы внешний поставщик, вы отправляете запросы со страницы **Все контакты** в модуле **Совместная работа с поставщиками**.
-   Если вы специалист по закупкам, вы отправляете запросы со страницы **Просмотреть контакты**. Для этого в записи поставщика в разделе **Настройка** на панели операций выберите **Контакты** &gt; **Просмотреть контакты**.

Можно сделать запрос на настройку пользователя, на отключение пользователя или на изменение роли безопасности. Если вы являетесь администратором внешнего поставщика, вы должны быть зарегистрированы как контактное лицо для счетов поставщика, для которого вы хотите делать запросы пользователей, и вам необходимо иметь доступ к интерфейсу совместной работы с поставщиками по этим счетам поставщика.  

Когда запрос отправлен, он добавляется в список **Запросы пользователей совместной работы с поставщиками** в модуле **Совместная работа с поставщиками** и в список **Запрос пользователя совместной работы с поставщиками** в модуле **Закупки и источники** (модуль "Закупки и источники" недоступен для внешних пользователей).

### <a name="provision-a-user"></a>Подготовка пользователя

Прежде чем можно будет запросить настройку нового пользователя, этот сотрудник должен быть настроен как контактное лицо для одного или нескольких счетов поставщика. Чтобы создать запрос на нового пользователя совместной работы с поставщиками:

1.  На странице **Все контакты** щелкните **Подготовить пользователя поставщика**.
2.  Ввод адреса электронной почты для этого пользователя. Этот адрес будет использоваться пользователем для входа в Finance and Operations. Если адрес электронной почты принадлежит домену, зарегистрированному как владелец Microsoft Azure, этот адрес электронной почты должен быть существующей учетной записью в Azure Active Directory (ADD), чтобы процесс подготовки был выполнен успешно. Если адрес электронной почты не принадлежит домену, зарегистрированному в Microsoft Azure, учетная запись ADD будет создана как часть процесса подготовки и новый пользователь получит письмо с приглашением. Адреса электронной почты клиента с такими доменами, как @hotmail.com, @gmail.com или @comcast.net, не могут использоваться для регистрации пользователя Finance and Operations.
3.  Установите для параметра **Доступ к совместной работе с поставщиками разрешен** значение **Да** для всех компаний, к которым пользователю требуется доступ.
4.  В разделе **Назначить роли пользователей** установите флажок **Назначить** для ролей безопасности, которые новый пользователь должен иметь.
5.  Щелкните **Отправить**.

Когда запрос пользователя поставщика отправлен, в поле **Доступ к совместной работе с поставщиками разрешен** устанавливается значение **Да** для выбранного счета поставщика и запускается workflow-процесс запроса пользователя. В рамках workflow-процесса новый пользователь создается в Finance and Operations и роли безопасности назначаются. Кроме того, служба Azure B2B активируется, которая начинает взаимодействие с порталом Azure и связывает новую или существующую учетную запись AAD с учетной записью пользователя Finance and Operations.

### <a name="inactivate-a-user"></a>Деактивирование пользователя

Существует два способа прекратить доступ к совместной работе с поставщиками для пользователя:

-   На странице **Контакты** для поставщика установите для параметра **Доступ к совместной работе с поставщиками разрешен** значение **Нет** для этого контактного лица. Это можно сделать по отдельности для каждого юридического лица, для которого данный пользователем служит контактом. Этот параметр может использоваться только специалистами по закупкам.
-   Отключите всю учетную запись пользователя, отправив запрос **Деактивировать пользователя поставщика**.

Чтобы запросить деактивацию пользователя:

1.  На странице **Все контакты** щелкните **Деактивировать** **пользователя поставщика**.
2.  Введите комментарий в поле **Деловое обоснование**.
3.  Щелкните **Отправить**.

### <a name="modify-security-roles"></a>Изменение ролей безопасности

Страница **Ведение ролей пользователей поставщиков** совпадает со страницей **Подготовить пользователя поставщика**, кроме списка ролей безопасности, который можно изменять.  

Чтобы запросить изменение ролей безопасности для пользователя:

1.  На странице **Все контакты** щелкните **Ведение** **ролей пользователей поставщиков**.
2.  Введите комментарий в поле **Деловое обоснование**.
3.  В разделе **Ведение ролей пользователей** выберите роли безопасности, которые требуется назначить, или снимите отметку у ролей, которые требуется удалить.
4.  Щелкните **Отправить**.




