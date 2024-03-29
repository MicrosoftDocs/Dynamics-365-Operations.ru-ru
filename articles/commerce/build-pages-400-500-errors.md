---
title: Создание страниц ответов для ошибок с кодом состояния 4xx/5xx
description: В этой статье описывается, как создавать настраиваемые страницы ответов для ошибок кода состояния 4xx и 5xx с помощью средств разработки в Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4a3b1762cebc74c1b77f9ca60925608bc966e306
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276409"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Создание страниц ответов для ошибок с кодом состояния 4xx/5xx

[!include [banner](includes/banner.md)]

В этой статье описывается, как создавать настраиваемые страницы ответов для ошибок кода состояния 4xx и 5xx с помощью средств разработки в Microsoft Dynamics 365 Commerce.

Если запрос не выполнен, сервер выдает сообщения об ошибке кода состояния HTTP. Код состояния 404 записывается и возвращается, если страница не найдена, а код состояния 500 фиксируется и возвращается в случае возникновения ошибки сервера. В Dynamics 365 Commerce пользователи приложения могут создавать пользовательские страницы ответа с кодами состояний ошибки, которые отображаются пользователям для этих сообщений об ошибке кода состояния.

## <a name="build-a-status-code-error-response-page"></a>Создание страницы сообщения об ошибке кода состояния

Чтобы начать создание страницы сообщения об ошибке код состояния, выполните следующие действия.

1. В предпочтительном веб-браузере выполните вход в Dynamics 365 Commerce. 
1. Выберите сайт, для которого требуется создать страницу сообщения об ошибке кода состояния 4xx/5xx

### <a name="build-the-template"></a>Создание шаблона

Чтобы создать шаблон для страницы сообщения об ошибке код состояния, выполните следующие действия.

1. Перейдите в пункт **Шаблоны**.
1. Выберите **Создать** для создания шаблона страницы.
1. В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите имя нового шаблона, затем выберите **ОК**.
1. Создайте шаблон на основе структуры, которую должна иметь страница сообщения об ошибке кода состояния.
1. Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его. 

### <a name="build-the-status-code-error-response-page"></a>Создание страницы сообщения об ошибке кода состояния

Чтобы создать страницу сообщения об ошибке код состояния, выполните следующие действия.

1. Перейти к пункту **Страницы**.
1. Выберите **Создать** для создания страницы.
1. В диалоговом окне **Выбор шаблона** выберите шаблон, затем в разделе **Имя страницы** введите имя страницы ответа при ошибке с кодом состояния. Не заполняйте поле **URL-адрес страницы**.
1. Создайте страницу.
1. Выберите **Сохранить**, выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.

> [!NOTE]
> Можно создать отдельные страницы сообщений об ошибках кода состояния для ошибок кода состояния 4xx и 5xx. В качестве альтернативы можно использовать одну и ту же страницу сообщения об ошибке кода состояния для обеих категорий ошибок.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Настройка перенаправления для страницы сообщения об ошибке кода состояния

Чтобы настроить перенаправление для страницы сообщения об ошибке код состояния, выполните следующие действия.

1. Перейдите в раздел **URL-адреса \> Создать \> Создать псевдоним** и выберите страницу сообщения об ошибке кода состояния, созданную ранее.
1. В поле **Псевдоним** введите **default-4xx** или **default-5xx**, в зависимости от страницы сообщения об ошибке кода состояния, для которой выполняется настройка перенаправления. Эти псевдонимы должны быть опубликованы. В противном случае перенаправление работать не будет.
1. Выберите **ОК**, чтобы подтвердить связывание.

> [!NOTE]
> Если для обеих категорий ошибок используется одна страница сообщения об ошибке кода состояния, повторите эту процедуру, чтобы связать псевдоним для другой категории ошибок с этой же страницей.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Работа с шаблонами](work-with-templates.md)

[Добавление новой страницы сайта](add-new-page.md)

[Создание URL-адреса страницы](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
