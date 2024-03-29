---
title: Работа с функцией электронных сообщений
description: В этой статье содержится информация о том, как работать с функцией электронных сообщений (EM).
author: AdamTrukawka
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 929d3d3aad249007264204a3fd51377c8bb42377
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279283"
---
# <a name="work-with-the-electronic-messages-functionality"></a>Работа с функцией электронных сообщений

[!include [banner](../includes/banner.md)]

При работе на уровне сообщений страница **Электронные сообщения** (**Налог** \> **Запросы и отчеты** \> **Электронные сообщения** \> **Электронные сообщения**) является более полезной. При работе на уровне сбора данных или элементов сообщения страница **Элементы электронного сообщения** (**Налог** \> **Запросы и отчеты** \> **Электронные сообщения** \> **Элементы электронного сообщения**) является более полезной.

## <a name="electronic-messages"></a>Электронные сообщения

Страница **Электронные сообщения** представляет действия, которые доступны для вас на основе вашей роли. Роли безопасности связаны с обработкой в настройке этой обработки. Для каждой обработки, которая вам доступна, эта страница отображает электронные сообщения и сведения, относящиеся к ним.

На экспресс-вкладке **Сообщения** отображаются электронные сообщения для выбранной обработки. В зависимости от статуса выбранного сообщения и заранее определенной обработки, можно выполнять некоторые действия, используя кнопки над сеткой:

- **Создать** — эта кнопка связана с действиями типа **Создать сообщение**.
- **Удалить** — эта кнопка доступна, если флажок **Разрешено удаление** выбран для текущего статуса выбранного сообщения.
- **Собрать данные** — эта кнопка связана с действиями типа **Заполнить записи**.
- **Создать отчет** — эта кнопка связана с действиями типа **Сообщение экспорта электронной отчетности**.
- **Отправить отчет** — эта кнопка связана с действиями типа **Веб-служба**.
- **Импорт ответа** — эта кнопка связана с действиями типа **Импорт электронной отчетности**.
- **Обновить статус** — эта кнопка связана с действиями типа **Пользовательская обработка на уровне сообщения**.
- **Элементы сообщения** — открытие страницы **Элементы электронного сообщения**.

На экспресс-вкладке **Журнала действий** отображаются сведения обо всех действиях, которые были выполнены для выбранного сообщения. Если действие вызвало ошибку, сведения об ошибке присоединяются к связанной строке в сетке. Для просмотра сведений об ошибке выберите строку в сетке, затем выберите кнопку **Вложение** (символ скрепки) в верхнем правом углу страницы.

На экспресс-вкладке **Дополнительные поля сообщения** отображаются все дополнительные поля, которые определены для сообщений в настройке обработки. Экспресс-вкладка также содержит значения этих дополнительных полей.

На экспресс-вкладке **Элементы сообщения** отображаются все элементы сообщения, связанные с выбранным сообщением. В зависимости от статуса выбранного элемента сообщения можно выполнять некоторые действия, используя кнопки над сеткой:

- **Удалить** — эта кнопка доступна, если флажок **Разрешено удаление** выбран для текущего статуса выбранного элемента сообщения.
- **Обновить статус** — эта кнопка связана с действиями типа **Обработка пользователя**.
- **Исходный документ** — открытие страницы, на которой отображается исходный документ для выбранного элемента сообщения.

Отчеты, которые уже созданы и получены для сообщения, присоединяются к этому сообщению. Для просмотра вложений, которые связаны с сообщением, выберите сообщение, затем выберите кнопку **Вложение** (символ скрепки) в верхнем правом углу страницы.

![Кнопка вложений](media/attachment-icon.png)

На странице **Вложения** отображаются вложения, которые относятся к выбранному сообщению. Чтобы просмотреть файл, выберите его в списке слева, затем выберите **Открыть** в области действий.

![Кнопка "Открыть"](media/open-button.png)

Можно просмотреть вложения, связанные с определенным действием, которое было ранее выполнено для сообщения. На странице **Электронные сообщения** на экспресс-вкладке **Сообщения** выберите сообщение. На экспресс-вкладке **Журнал действий** выберите действие и затем нажмите кнопку **Вложение** (символ скрепки) в верхнем правом углу страницы.

Можно выполнить полную обработку или только определенное действие, выбрав **Выполнить обработку** в области действий.

## <a name="electronic-message-items"></a>Элементы электронного сообщения

На странице **Элементы электронного сообщения** представлены все элементы сообщения и журнал действий, которые были выполнены для каждого элемента сообщения. На странице также показаны дополнительные поля, которые определены для элементов сообщения, и значения этих дополнительных полей.

В следующей таблице описаны поля на вкладке **Элементы сообщения**.

<table>
<thead>
<tr>
<th>Поле</th>
<th>описание</th>
</tr>
</thead>
<tbody>
<tr>
<td>Обработка</td>
<td>Имя обработки, которая использовалась при создании элемента сообщения.</td>
</tr>
<tr>
<td>Элемент сообщения</td>
<td>Идентификатор элемента сообщения. Этот код присваивается автоматически на основе номерной серии <b>Элемент сообщения</b>, которая определена на странице <b>Параметры главной книги</b>.</td>
</tr>
<tr>
<td>Дата элемента сообщения</td>
<td>Дата создания элемента сообщения.</td>
</tr>
<tr>
<td>Тип элемента сообщения</td>
<td>Тип элемента сообщения. Можно настроить несколько типов элементов сообщений для этой и той же обработки (например, <b>Входящие накладные</b> и <b>Исходящее накладные</b>). Это поле может заполняться автоматически только в том случае, когда накладная добавляется в таблицу элементов сообщения.</td>
</tr>
<tr>
<td>Статус элемента сообщения</td>
<td><p>Фактический статус элемента сообщения. Доступные статусы зависят от типа элемента сообщения. Далее приводятся некоторые примеры.</p>
<ul>
<li><b>Заполнен</b> — запись была добавлена в таблицу элементов сообщения.</li>
<li><b>Вычислен</b> — дополнительные атрибуты были рассчитаны для элемента сообщения.</li>
<li><b>Сообщен</b> — элемент сообщения был успешно добавлен в отчет.</li>
<li><b>Исключен</b> — этот статус полезен, если необходимо исключить некоторые элементы сообщения из отчета до его экспорта.</li>
</ul>
</td>
</tr>
<tr>
<td>Дата передачи</td>
<td>Для обработки, которая автоматически передает сформированный отчета за пределы системы, это дата передачи элемента сообщения.</td>
</tr>
<tr>
<td>Номер документа</td>
<td>Это поле заполняется автоматически на основе настройки действия заполнения записей. Это поле может заполняться автоматически только в том случае, когда накладная добавляется в таблицу элементов сообщения.</td>
</tr>
<tr>
<td>Расчетный счет</td>
<td>Номер счета клиента или поставщика, или другое значение поля, в зависимости от поля, которое определено в действии заполнения записей. Это поле может заполняться автоматически только в том случае, когда накладная добавляется в таблицу элементов сообщения.</td>
</tr>
<tr>
<td>Сообщение</td>
<td>Номер сообщения. Этот номер присваивается автоматически на основе номерной серии <b>Сообщение</b>, которая определена на странице <b>Параметры главной книги</b>.</td>
</tr>
<tr>
<td>Статус сообщения</td>
<td>Фактический статус электронного сообщения.</td>
</tr>
<tr>
<td>Следующее действие</td>
<td>Следующие действия, которые могут быть запущены для текущего статуса элемента сообщения.</td>
</tr>
</tbody>
</table>

На вкладке **Дополнительные поля** отображаются дополнительные поля для выбранного элемента сообщения и их значения.

### <a name="run-processing"></a>Выполнить обработку

Выберите **Выполнить обработку** в области действий для выполнения обработки для элементов сообщения. Чтобы выполнить определенное действие, в диалоговом окне **Выполнить обработку** задайте для параметра **Выберите действие** значение **Да**, затем выберите действие. Для выполнения всей обработки оставьте для параметра **Выберите действие** значение **Нет**.

### <a name="generate-report"></a>Создать отчет

На панели операций выберите **Создать отчет**. Эта кнопка связана с действиями типа **Экспорт электронной отчетности**.

### <a name="update-status"></a>Изменить статус

Выберите **Изменить статус** в области действий для обновления статуса одного или нескольких элементов сообщения. В диалоговом окне **Изменить статус** используйте экспресс-вкладку **Включаемые записи**, чтобы выбрать элементы сообщения для обновления. Убедитесь, что вы правильно определили критерии выбора, так как статусы элементов сообщения будут обновлены в соответствии с этими критериями, начальным статусом выбранного действия и указанным значением в поле **Новый статус**. После завершения обновления статуса будет сложно определить, какие элементы были обновлены. Таким образом будет сложно выполнить откат обновления статуса.

### <a name="electronic-messages"></a>Электронные сообщения

Выберите **Электронные сообщения** в области действий, чтобы просмотреть электронное сообщение, которое связано с выбранным элементом сообщения.

Можно также просмотреть файлы, которые связаны с определенным элементом сообщения. Выберите поле **Сообщение** для элемента сообщения или выберите **Электронные сообщения** в области действий. На странице **Электронное сообщение** выберите сообщение, для которого требуется просмотреть файлы, затем выберите кнопку **Вложение** (символ скрепки) в верхнем правом углу страницы.

На странице **Вложения** отображаются вложения, которые относятся к сообщению. Чтобы просмотреть файл, выберите его в списке слева, затем выберите **Открыть** в области действий.

### <a name="original-document"></a>Исходный документ

Выберите **Исходный документ** в области действий, чтобы открыть исходный документ для выбранного элемента сообщения.
