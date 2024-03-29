---
title: Копирование содержимого в другой языковой стандарт
description: В этой статье описывается копирование существующего содержимого в другой языковой стандарт в рамках сайта в конструкторе сайтов Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 6afa871048bde22133ae083b8d56b6e99e49c401
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269270"
---
# <a name="copy-content-to-another-locale"></a>Копирование содержимого в другой языковой стандарт

[!include[banner](../includes/banner.md)]

В этой статье описывается копирование существующего содержимого в другой языковой стандарт в рамках сайта в конструкторе сайтов Microsoft Dynamics 365 Commerce.

При создании содержимого в конструкторе сайтов Commerce оно всегда связано с кодом языка, например "en-us". Можно копировать отдельные страницы и ресурсы в другой языковой стандарт в рамках одного сайта электронной коммерции, переключив языковой стандарт при редактировании элемента содержимого, а затем создав новый вариант элемента. В некоторых случаях, например при запуске в витрине совершенно нового языкового стандарта, имеет смысл дублировать все элементы содержимого в существующем языковом стандарте в новый языковой стандарт. Если новый языковой стандарт имеет тот же базовый язык, что и один из существующих языковых стандартов, можно использовать существующий языковой стандарт в качестве исходного языкового стандарта для операции копирования в языковой стандарт. (Например, в языковых стандартах "en-US" и "en-AU" используется английский язык.) Таким образом можно сократить усилия, необходимые для локализации содержимого в новом языковом стандарте.

Следующие процедуры описывают, как добавить новый языковой стандарт к существующему каналу, скопировать все элементы содержимого из существующего языкового стандарта в новый языковой стандарт и контролировать статус операции копирования в языковой стандарт.

## <a name="add-a-new-locale"></a>Добавление нового языкового стандарта

Чтобы добавить новый языковой стандарт в конфигураторе сайта Commerce, выполните следующие шаги.

1. В конфигураторе сайта перейдите на свой сайт.
1. В левой области переходов выберите **Параметры сайта**, затем выберите **Каналы**.
1. В поле **Канал** выберите канал, в который добавляется новый языковой стандарт.
1. В диалоговом окне канала, которое отображается справа, выберите **Добавить языковой стандарт**.
1. В диалоговом окне **Добавить языковой стандарт** в поле **Языковой стандарт для поддержки** выберите языковой стандарт.
1. Убедитесь, что значение **Домен** введено правильно.
1. В области **Путь** введите уникальный путь URL-адреса (например, **en-us** или **english-us**).
1. Нажмите **ОК**.
1. Закройте диалоговое окно канала.
1. В области **Канал** убедитесь, что новый языковой стандарт указан рядом с нужным каналом.
1. Выберите **Сохранить и опубликовать**.

> [!NOTE]
> Прежде чем новый языковой стандарт можно будет настроить в конструкторе сайтов, он должен быть добавлен к соответствующему каналу интернет-магазина в Commerce Headquarters.

## <a name="copy-all-content-items-to-a-new-locale"></a>Копирование всех элементов содержимого в новый языковой стандарт

Чтобы скопировать все элементы содержимого в новый языковой стандарт в конфигураторе сайта Commerce, выполните следующие шаги.

1. В конфигураторе сайта перейдите на свой сайт.
1. В левой области переходов выберите **Параметры сайта**, затем выберите **Каналы**.
1. На панели команд выберите **Создать копию языкового стандарта из**.
1. В диалоговом окне **Создание копии языкового стандарта**, которое появляется справа, в области **Исходный сайт** убедитесь, что выбран правильный сайт.
1. В поле **Исходный канал** выберите исходный канал.
1. В поле **Канал назначения** выберите тот же исходный канал.
1. В поле **Исходный языковой стандарт** выберите исходный языковой стандарт.
1. В поле **Языковой стандарт назначения** выберите новый языковой стандарт.
1. Выберите **Копировать языковой стандарт**. Уведомление подтверждает, что операция копирования языкового стандарта запущена.

> [!NOTE]
> Имеется также возможность копировать содержимое между различными каналами.

## <a name="monitor-the-status-of-the-locale-copy"></a>Отслеживание статуса копии языкового стандарта

Чтобы отслеживать состояние операции копирования языкового стандарта, выполните следующие действия.

1. В конфигураторе сайта перейдите на свой сайт.
1. В левой области переходов выберите **Параметры сайта**, затем выберите **Задания**.
1. В области **Текущие задания** выберите задание, которое необходимо отслеживать. Сведения о задании отображаются в диалоговом окне, которое появляется справа.
