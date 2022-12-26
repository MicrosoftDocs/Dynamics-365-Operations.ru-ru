---
title: Обмен данными данных между компаниями для подарочных сертификатов
description: В этой статье описывается, как настроить Microsoft Dynamics 365 Commerce для использования функций общего доступа к данным Dynamics 365 Finance в областях данных для синхронизации данных подарочных сертификатов.
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: bc0df6c4aac72907e8523069e3f1ae100780dc3c
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473940"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>Обмен данными данных между компаниями для подарочных сертификатов

[!include [banner](../includes/banner.md)]

В этой статье описывается, как настроить Microsoft Dynamics 365 Commerce таким образом, чтобы оно использовало функции общего доступа к данным Dynamics 365 Finance в областях данных для синхронизации данных подарочных сертификатов. Затем можно использовать функцию совместного использования записей данных для совместного использования межфирменных данных между двумя областями данных. Таким образом, внутренняя подарочная таблица Commerce может обмениваться данными между двумя сущностями компании. Дополнительные сведения о совместном использовании данных между компаниями в Dynamics 365 Finance см. в разделе [Совместное использование данных между компаниями](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

## <a name="key-terms"></a>Ключевые термины

| Срок | Описание |
|---|---|
| Компания | Юридическое лицо в среде Dynamics 365 Finance. |
| Подарочный сертификат | Внутренний продукт подарочной карты Dynamics 365 Commerce. |

## <a name="prerequisites"></a>Необходимые условия

Пользователи должны настроить свою среду для совместного использования данных в нескольких компаниях, как описано в разделе [Совместное использование данных между компаниями](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

В **RetailGiftCardTable** для поля **DataSharingType** должно быть задано значение **Дублировать**, чтобы включить совместное использование с дублированием записей (DRS) для таблицы подарочных сертификатов. Дополнительные сведения см. в разделе [Совместное использование данных между компаниями для разработчиков](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev).

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>Настройка совместного использования данных между компаниями для подарочных сертификатов

Чтобы настроить совместное использование данных между компаниями для подарочных сертификатов, выполните следующие действия.

1. в Commerce headquarters перейдите в раздел **Администрирование системы \> Настройка \> Настройка совместного использования данных компаниями**.
1. В области действий выберите **Создать** для добавления записи общего доступа к данным.
1. В поле **Имя** введите имя записи общего доступа к данным (например, **Подарочные сертификаты**).
1. В разделе **Таблицы и поля для совместного использования** выберите **Добавить**.
1. В диалоговом окне **Поделиться новой таблицей** в поле **Имя таблицы** введите **RETAILGIFTCARDTABLE** (таблица для розничных подарочных карт). Поле **Метка таблицы** должно быть автоматически установлено на **Таблица подарочных сертификатов**.
1. Убедитесь, что установлены все флажки **Сохранить данные по компании**, **Имеет уникальный индекс** и **Общий доступ еще не предоставлен**. Выбор этих флажков инициирует проверки, которые относятся к функциям совместного использования данных.
1. Выберите **Добавить таблицу**. Запись **Таблица подарочных сертификатов (RetailGiftCardTable)** теперь должна присутствовать в разделе **Таблицы и поля для совместного использования**. Выберите символ крышки (^) для просмотра всех полей таблицы, которые автоматически связываются с таблицей для совместного использования.
1. В разделе **Компании, использующие записи в этих таблицах** выберите **Добавить**, чтобы добавить компанию, которой требуется предоставить общий доступ к данным.
1. В строке под **Компания** выберите компанию в раскрывающемся списке.
1. В поле **Имя** введите имя компании.
1. Повторите шаги 8–10, чтобы добавить другие строки компании.
1. После завершения добавления строк компаний в области действий выберите **Включить**.
1. Вы получите следующее предупреждающее сообщение "Это действие рекомендуется выполнять только в нерабочее время. Любые операции с проводками, выполняющиеся одновременно, могут завершиться сбоем для таблиц, которые нужно изменить. Продолжить?" Выберите **Да**, чтобы согласиться.
1. Вы получаете следующее предупреждающее сообщение "Скопировать все существующие данные между всеми общими компаниями?" Выберите **Да**, чтобы согласиться.

После того как вы соглашаетесь с обоими сообщениями, будут запущены таблицы для копирования данных между настроенными компаниями. Сальдо по одному подарочному сертификату компании будет затем отображаться в другой компании.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Вопросы и ответы по платежам](payments-retail.md)

[Модуль оформления заказа](../add-checkout-module.md)

[Модуль платежа](../payment-module.md)