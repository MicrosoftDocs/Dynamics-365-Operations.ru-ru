---
title: Устранение неполадок с соединитель платежей Dynamics 365 для Adyen
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь в обеспечении технической поддержки при возникновении проблем с соединитель платежей Microsoft Dynamics 365 для Adyen.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f40e29a17fe860440bd8192a89b0f5150f0db9ab213b2190f9deaf33a4f2aaba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743943"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a>Устранение неполадок с соединитель платежей Dynamics 365 для Adyen

[!include [banner](../../includes/banner.md)]

В этом разделе содержатся указания по устранению неполадок, которые могут помочь в обеспечении технической поддержки при возникновении проблем с соединитель платежей Microsoft Dynamics 365 для Adyen.

## <a name="description"></a>описание

У вас есть вопросы с соединителем платежей Dynamics 365 для Adyen в следующих областях, и вам необходима поддержка рабочей группы Adyen:

- Конфигурация POS, Modern POS (MPOS), центра обработки звонков или Dynamics 365 Commerce
- Номер ссылки поставщика службы платежа Adyen (PSP) (например, если имеются вопросы о отклонениях, в том числе при ручном вводе ключа \[MKE\])
- Все, что не работает в испытательной или реальной среде продавца

## <a name="resolution"></a>Приказ

Используйте следующий шаблон сообщения электронной почты для запуска процесса поддержки с помощью рабочей группы Adyen. Для ускорения устранения неполадок убедитесь, что в сообщении электронной почты содержатся все необходимые сведения.

| Поле        | значение |
|--------------|-------|
| по           | `support@adyen.com` |
| Копия           | |
| Строка темы | Запрос на поддержку Microsoft Dynamics |
| Текст         | <p>Добрый день,</p><p>Предоставьте поддержку по следующей проблеме:</p><ul><li>Счет торговца</li><li>Среда (тест/произв.)</li><li>Канал (POS/центр обработки вызовов/электронная коммерция Commerce)</li><li>Номер ссылки PSP, если проблема связана с конкретной проводкой (вы можете найти номер ссылки PSP в чеке, в области клиента Adyen или в меню проводки на POS).</li><li>Снимок экрана или фотография сообщения об ошибке, если это применимо</li><li>Журналы средства просмотра событий (в формате .txt)</li><li>Описание проблемы и шаги по устранению неполадок, которые вы пытались выполнить</li></ul> |

## <a name="additional-resources"></a>Дополнительные ресурсы

[Прием платежей с соединителем Adyen для Dynamics 365 Commerce](https://www.adyen.com/partners/dynamics-365-commerce)

[Соединитель платежей Dynamics 365 для Adyen](../dev-itpro/adyen-connector.md)

[Настройка соединителя платежей Adyen для Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
