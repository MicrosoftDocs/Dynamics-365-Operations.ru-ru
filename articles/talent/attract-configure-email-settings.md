---
title: Настройка параметров электронной почты в Microsoft Dynamics 365 for Talent - Attract
description: В этой теме объясняется, как задать настройки для сообщений электронной почты, которые отправляется Microsoft Dynamcis 365 for Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 360937b807ea149edb2f16ad6799d74791d599b5
ms.sourcegitcommit: a6b32be10b6eb6340f8f68261bf62d0202c03dd1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/05/2019
ms.locfileid: "1729799"
---
# <a name="configure-email-settings-in-microsoft-dynamics-365-for-talent---attract"></a>Настройка параметров электронной почты в Microsoft Dynamics 365 for Talent - Attract
[!include[banner](../includes/banner.md)]

Ваша торговая марка устанавливает доверие и помогает создать отношения с кандидатами еще до того, как они подадут заявление на ваши вакансии. Положительное впечатление от торговой марки привлекает лучшие кадры и увеличивает лояльность существующих сотрудников. Microsoft Dynamics 365 for Talent: Attract позволяет настроить сообщения электронной почты, чтобы они соответствовали торговой марке компании. Таким образом, можно обеспечить согласованное взаимодействие с кандидатами на должности в процессе обработки заявлений.

С помощью Attract можно выполнять следующие действия:

- Настройте параметры сообщений электронной почты таким образом, чтобы использовалась учетная запись службы электронной почты Microsoft Exchange компании. Таким образом кандидаты знают, что сообщения электронной почты поступают от компании. Например, можно задать настройки таким образом, чтобы кандидаты получали сообщения электронной почты с адреса `recruiting@contoso.com`, а не с адреса `contoso@microsoft.com`.
- Создайте согласованный фирменный стиль для всех сообщений электронной почты, задав глобальный верхний и нижний колонтитулы для шаблонов электронной почты. 

> [!NOTE]
> Чтобы настроить Attract, чтобы использовать учетную запись службы электронной почты компании для отправки сообщений электронной почты, необходима надстройка Comprehensive hiring.

## <a name="connect-an-email-service-account"></a>Подключение учетной записи службы электронной почты

Путем подключения учетной записи службы электронной почты компании можно создать фирменное взаимодействие по электронной почте для ваших кандидатов на работу. Если вы не подключаете учетную запись компании, в Attract используется учетная запись службы электронной почты Майкрософт по умолчанию.

1. Выберите **Параметры** (символ шестеренки в верхнем правом углу), затем выберите **Центр администрирования**.
2. На вкладке **Параметры электронной почты** в разделе **Учетные записи службы электронной почты** выберите **Подключить учетную запись компании**.

    ![Подключение учетной записи службы электронной почты компании в Attract](./media/attract-admin-email-service-accounts.png)

    Дополнительные сведения о создании общей учетной записи электронной почты см. в разделе [Общие почтовые ящики в Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).

3. В окне входа в Microsoft выполните вход, используя учетные данные вашей организации.
4. Если вы еще не настроили учетную запись службы электронной почты или хотите добавить новую, выберите **Добавить новую учетную запись службы**, затем введите данные электронной почты. Если вы уже настроили учетную запись службы электронной почты, которую вы хотите использовать, выберите ее.

Когда учетная запись службы электронной почты успешно настроена, она отображается в списке **Учетные записи службы электронной почты**.

## <a name="disconnect-an-email-service-account"></a>Отключение учетной записи службы электронной почты

Если требуется прекратить использование домена компании в сообщениях электронной почты в Attract, можно отключить учетную запись службы электронной почты.

1. Выберите **Параметры** (символ шестеренки в верхнем правом углу), затем выберите **Центр администрирования**.
2. На вкладке **Параметры электронной почты** в разделе **Учетные записи службы электронной почты** нажмите кнопку **Дополнительно** (три вертикальные точки) рядом с учетной записью службы электронной почты, которую необходимо отключить.
3. Выберите **Отключить учетную запись электронной почты**.

    ![Отключение учетной записи службы электронной почты компании](./media/attract-admin-disconnect-email-account.png)

4. При появлении запроса на подтверждение операции выберите **Отключить.**

    ![Подтверждение отключения учетной записи службы электронной почты компании](./media/attract-admin-email-confirm-disconnect.png)

Если вы не подключили другую учетную запись службы электронной почты, письма, отправленные из Attract, будут использовать учетную запись службы электронной почты Майкрософт по умолчанию.

## <a name="configure-email-template-settings"></a>Настройка параметров шаблонов электронной почты

Вы можете отправить изображение эмблемы компании и другую информацию в виде фирменного заголовка для своих сообщений электронной почты. Можно также предоставить ссылки на политику конфиденциальности и условия использования в нижних колонтитулах сообщений электронной почты.

> [!NOTE]
> Вы должны соблюдать все действующее законодательство своей страны или региона, а также законодательство страны или региона получателя сообщений электронной почты. Эти законы включают в себя правила защиты от нежелательной почты.

1. Выберите **Параметры** (символ шестеренки в верхнем правом углу), затем выберите **Центр администрирования**.
2. На вкладке **Параметры электронной почты** в разделе **Параметры шаблонов электронной почты** перетащите изображение, которое требуется использовать в качестве заголовка электронной почты, в поле изображения, или щелкните в поле изображения, чтобы найти файл. Чтобы заменить существующее изображение, необходимо сначала выбрать **Удалить** рядом с ним. Изображение должно быть файлом JPEG, JPG, PNG или SVG. Рекомендуемый размер для изображений составляет от 25 до 800 пикселей в ширину, и от 25 до 150 пикселей в высоту. Максимальный размер файла для заголовка — 1 мегабайт (МБ).

    ![Добавление изображения для заголовка сообщений электронной почты компании](./media/attract-admin-email-header.png)

3. В поле **Ваша политика конфиденциальности в отношении переписки** укажите ссылку на политику конфиденциальности компании. В поле **Ваши условия в отношении переписки** предоставьте ссылку на условия использования, принятые в вашей компании.

    ![Добавление ссылок на политику конфиденциальности компании и условия использования для нижнего колонтитула сообщений электронной почты](./media/attract-admin-email-footer.png)

4. Выберите **Сохранить** для сохранения своих настроек шаблонов сообщений электронной почты.