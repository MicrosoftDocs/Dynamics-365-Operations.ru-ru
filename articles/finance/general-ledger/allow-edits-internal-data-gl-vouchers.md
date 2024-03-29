---
title: Разрешить изменение внутренних данных по ваучерам главной книги
description: В этой статье приводятся сведения о том, как изменять внутренние данные по ваучерам главной книги.
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 6e346c6ff881d3a33743196b45247493fd19ed1d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573260"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Разрешить изменение внутренних данных по ваучерам главной книги

[!include[banner](../includes/banner.md)]


При разноске записей учета в главную книгу поле **Описание** часто используется для хранения внутренних примечаний или документации. Если информация оказывается неверной, это может привести к путанице и усложнить закрытие периода. Эта функция позволяет главному бухгалтеру или супервизору по учету исправлять ошибки, редактируя поле **Описание** в разнесенных ваучерах в главной книге.

Изменения в разнесенных ваучерах в главной книге ограничены данными, которые являются внутренними по своей природе. Эта функция никогда не позволит изменять такие данные, как суммы, даты разноски, счета ГК и валюту проводки. Изменения этих данных повлияют на внешние отчеты о финансовых показателях и должны выполняться только через новые ваучеры главной книги.

> [!NOTE]
> В Dynamics 365 Finance версии 10.0.29 эта функция позволяет изменять только поле **Описание**.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Изменение внутренних данных по ваучерам главной книги

Чтобы получить возможность изменять внутренние данные по ваучерам главной книги, необходимо включить функцию **Разрешить изменение внутренних данных по ваучерам главной книги** в рабочей области **Управление функциями**.
После включения этой функции пользователь, который будет редактировать разнесенные ваучеры, должен быть назначен роли главного бухгалтера или супервизора по учету. Можно также добавить разрешения для других ролей, настроив роли безопасности.

Изменение допускается только со страницы проводок по ваучеру.

1. Перейдите в раздел **Главная книга** > **Запросы и отчеты** > **Проводки по ваучеру**.
2. В диалоговом окне **SysQuery** введите критерии поиска для выбора ваучеров.
3. Выберите строки с ваучерами, которые необходимо изменить, а затем выберите команду **Изменить ваучер** > **Изменить внутренние данные ваучера**.

    [![Страница проводок по ваучеру](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
На странице **Изменить внутренние данные ваучера** отображаются следующие данные для каждой выбранной строки:
  
  - Счет учета
  - Наименование счета
  - Ваучер
  - Текущее описание
  - Новое описание

    [![Операция журнала.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Редактировать можно только поле **Новое описание**. По умолчанию значение соответствует значению поля **Текущее описание**, что позволяет быстро исправлять незначительные ошибки в описании.

4. Измените поле **Новое описание** в каждой строке или удалите описание из каждой строки.

   Если необходимо внести одно и то же значение в несколько строк, можно также выполнить для этого указанные ниже действия.

      1. Выберите строки для редактирования, а затем выберите команду **Массовое обновление выбранных записей**.
      2. В поле **Изменяемое поле** выберите поле, которое необходимо изменить. В настоящее время в поиске используется только поле **Новое описание**.
      3. В поле **Новое значение** введите новое описание.
      4. Выберите **Обновить**. Все выбранные записи будут обновлены с использованием нового значения.

      [![Диалоговое окно "Массовое обновление выбранных записей".](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. В поле **Причина для изменения** добавьте примечание, объясняющее, почему было сделано изменение. Это примечание отображается на странице **Аудиторский след изменения ваучеров**.

   Для одного ваучера может быть выполнено несколько изменений, и каждое изменение будет отслеживаться.

## <a name="audit-trail-of-voucher-edits"></a>Аудиторский след изменения ваучеров

Аудиторский след ведется специально для отслеживания изменений, внесенных с помощью этой функции. Доступ к аудиторскому следу изменения ваучеров можно получить двумя способами:

  - Перейдите в раздел **Главная книга** > **Запросы и отчеты** > **Проводки по ваучеру**. На странице **Запросы ваучера** выберите пункт **Изменить ваучер** > **Аудиторский след изменения ваучеров**. Аудиторский след отображается только для выбранной записи ваучера. 
   
    При открытии запроса таким образом можно сосредоточиться на всех изменениях, внесенных в отдельную запись ваучера.
  
  - Перейдите к пункту **Главная книга** > **Периодические задачи** > **Аудиторский след изменения ваучеров**. В диалоговом окне введите критерии, чтобы указать ваучеры, для которых необходимо просмотреть аудиторский след для изменений. Для просмотра аудиторского следа для всех операций оставьте критерии пустыми и нажмите кнопку **ОК**. 
    
    Открыв запрос таким образом, можно отфильтровать изменения, сделанные в конкретный день или конкретным пользователем.

На странице **Аудиторский след изменений** отображаются следующие сведения:

- **Дата и время создания** — дата и время изменения.
- **Причина для изменения** — причина, которую пользователь указал для изменения.
- **Кем создано** — пользователь, внесший изменение.

Чтобы просмотреть подробные сведения о каждом аудиторском следе, получите детализацию по значению **Дата и время создания**. На странице **Просмотр свойств измененного ваучера** отображается та же информация, что и на исходной странице редактирования, включая предыдущее описание и обновленное описание.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
