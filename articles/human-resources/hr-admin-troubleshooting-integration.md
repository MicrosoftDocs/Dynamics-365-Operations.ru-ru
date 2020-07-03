---
title: Вопросы и ответы интеграции с Finance
description: В этой статье объясняется, какие данные синхронизируются в интеграции Human Resources и Finance.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0a3389d6ce5f1985f7515e777a2bafae4eae5f0c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431115"
---
# <a name="integration-with-finance-faq"></a>Вопросы и ответы интеграции с Finance

В этом разделе содержатся ответы на часто задаваемые вопросы, связанные с тем, какие данные синхронизируются в случае интеграции Dynamics 365 Human Resources с Dynamics 365 Finance.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Синхронизируются все данные или только некоторые информационные объекты?

Синхронизируется подмножество данных. Список всех сущностей см. в разделе [Интеграция Dynamics 365 Finance](hr-admin-integration-finance.md).

## <a name="why-dont-i-see-any-data-synced-to-common-data-service"></a>Почему не отображаются данные, синхронизированные с Common Data Service?

По умолчанию интеграция Common Data Service отключена в новых средах, не содержащих предоставленных демонстрационных данных. По умолчанию он включается в новых средах, содержащих демонстрационные данные, а синхронизация данных начинается при подготовке среды. После того как среда готова к синхронизации данных, можно включить интеграцию. Дополнительные сведения см. в разделе [Настройка интеграции Common Data Service](hr-admin-integration-common-data-service.md).

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Можно ли создать новое сопоставление без использования шаблонов?

Шаблоны являются отправной точкой. Можно создать собственный шаблон, но всегда требуется шаблон при создании проекта интеграции. Дополнительные сведения об интеграторе данных (DI), шаблонах и проектах см. в разделе [Интеграция данных в Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>Можно ли сопоставить финансовые аналитики для перемещения между Human Resources и Finance?

Финансовые аналитики в настоящее время не находятся в Common Data Service для приложений и, в результате, не являются частью шаблона по умолчанию. Эта сущность запланирована, но в настоящее время не известно, когда она будет выпущена.

Для данных, которые расположены в Finance, но не существуют в Human Resources, свяжите две системы вместе с помощью **Настроить ссылки** в Human Resources.

![Сопоставление финансовых аналитик](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>Иногда при импорте сотрудников они перемещаются в неактивных работников в Finance. Почему?

Данная ошибка может возникать, если у сотрудников нет активной записи сведений о приеме на работу в Human Resources. Чтобы решить эту проблему, откройте **Управление персоналом \> Сотрудники \> История занятости \> Диспетчер дат**и убедитесь, что имеется активная запись данных о приеме на работу.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Если я выбрал сопоставить только подмножество полей, изменений, будут ли изменения, внесенные в несопоставленные поля, вызывать синхронизацию?

Синхронизация данных производится в соответствии с графиком выполнения. Интеграция выберет запись, если любое поле в записи было изменено, независимо от того, является ли это поле частью сопоставления интеграции.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Как отправить только изменения активных рабочих, но не завершенные записи?

С помощью функции "Расширенный запрос" можно фильтровать и формировать исходные данные перед передачей их в место назначения.

![Расширенный запрос активных работников](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>Можно ли указать поля, которые передаются в Finance, для конкретной сущности?

Поля можно добавлять или удалять из задачи интеграции. Не все поля данных, которые существуют в сущности Common Data Service будет заполняться из Human Resources.
Дополнительные данные могут заполняться через Power Apps.

![Добавление полей в задачу интеграции и удаление полей из задачи интеграции](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Я настроил интеграцию как пакетное задание, но Human Resources потерял подключение к системе назначения. Как можно отправить этот же набор изменений в систему назначения?

Специальная настройка для обработки исключений не требуется. Интегратор данных автоматически перехватывает ошибки, которые произошли в источнике или пункте назначения, сообщает о них и позволяет выполнить повторные попытки вручную. Однако это не обеспечивает ручной коррекции данных. Если требуются обновления данных, это должно быть выполнено как в источнике, так и в месте назначения.

## <a name="can-i-set-up-bi-directional-integration"></a>Как можно настроить двунаправленную интеграцию?

Нет, сейчас интеграция односторонняя (из Human Resources в Finance and Operations). Тем не менее, существует шаблон по умолчанию для отправки данных из Human Resources в Finance.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Можно ли разрешить удаление записи как часть моей интеграции?

Нет, интегратор данных не будут регистрировать удаленные записи для переноса данных. Только создание данных и обновления (UPSERT) входят в настоящее время.

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Можно ли повторно выполнить поврежденное выполнение? Если да, будет ли отправлен полный файл или только изменения?

Первый запуск интегратора данных всегда является полным запуском. Последующие запуски основаны на отслеживании изменений. В случае выполнения с ошибками извлекаются записи в области выполнения и отправляются самые последние изменения из Common Data Service.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>При сохранении проекта появилось сообщение об ошибке: "Проект имеет ошибки сопоставления". Что делать?

Проверьте настройку интеграционных ключей, внесите все требуемые изменения в настройку, затем обновите сущности в проекте.

При использовании шаблона по умолчанию интеграционные ключи будут импортированы автоматически. Эта проблема может возникнуть при добавлении новой задачи к существующему шаблону.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Если имеется N юридических лиц, в которых сотрудники имеют занятость, нужно ли создать сопоставление для каждого из них?

Да, для каждого юридического лица в Finance необходим отдельный проект интеграции в интеграции данных.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Требуется перенести данные, которые не являются частью шаблона по умолчанию, предоставленного корпорацией Майкрософт. Можно сделать это?

Да, поля можно добавить в существующий шаблон или удалить их из него. Можно изменить шаблон для включения дополнительных данных из других сущностей Common Data Service для приложений. Сущность должна находиться в Common Data Service для приложений, чтобы ее можно было включить в шаблон. 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Я только что создал новые среды Finance и Human Resources и получил ошибку "Значение данных нарушает ограничения целостности". Почему?

Причины этой ошибки могут быть следующими:

- Передача данных привела к извлечению дублирующихся записей в источнике (Common Data Service).

- Перемещение данных содержит значения NULL для полей, которые необходимы в Finance and Operations. Проверьте данные в Common Data Service и соответствуют требованиям Finance and Operations.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Если имеются ошибки выполнения и код сотрудника не синхронизируется, как найти старое задание, которое содержит сбойную запись сотрудника?

Интегратор данных создаст несколько проектов в Finance. Связь между задачей интегратора данных и проектом Finance будет один к одному.

Отследите время из журнала выполнения интегратора данных и найдите проект индекс -1 в Finance. Если номер задачи равен 9 в интеграторе данных, индекс в Finance — 8.

1. Запишите индекс задачи из интегратора данных (в этом примере это "9").

    ![Запись индекса задачи из интегратора данных](media/CaptureTaskIndex.png)

2. Отследите время выполнения проекта.

    ![Отслеживание времени выполнения проекта](media/CaptureTimeOfExecution.png)

3. В Finance укажите индекс — 1. В этом примере проект с суффиксом "8" и временем выполнения проекта с индексом "0" совпадает со времени выполнения на этапе 2.

    ![Определение индекса](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>После интеграции Human Resources и Finance я не вижу свои данные Human Resources в Finance. Что делать?

Интеграция с Finance осуществляется в два этапа. Во-первых убедитесь, что данные Human Resources обновлены и доступны в Common Data Service. Это синхронизация почти в реальном времени, и ее можно проверить в Power Apps, просмотрев данные в информационных объектах.

![Данные в Common Data Service](media/DataInCDS.png)

Если данные не отображаются должным образом в Common Data Service, убедитесь, что сущность поддерживается в интеграции. Чтобы включить дополнительные данные в Common Data Service, изменение будет требоваться со стороны корпорации Майкрософт.

Если сущность поддерживается и данные доступны в Common Data Service, проверьте правильность сопоставления в интеграторе данных. Если сопоставление интегратора выглядит правильным, затем проверьте успешность выполнения заданий управления данными. Ошибки могут возникать при выполнении пакетных заданий. Дополнительные сведения об управлении данными см. в разделе [Управление данными](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>Адреса моих сотрудников неправильные после импорта в Finance. Что делать?

Номерная серия для параметра **Код местоположения** использует одинаковый шаблон в Human Resources и Finance. Номерная серия должна быть уникальной на обеих сторонах, поэтому нет конфликтов адресов при интеграции данных из Common Data Service в Finance and Operations.

Во время реализации Human Resources убедитесь, что номерные серии не одинаковы в Human Resources и Finance. Проверьте, что все номерные серии не идентичны там, где данные могут поддерживаться в обеих системах.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>При создании моего набора подключения я не вижу подключение в раскрывающемся списке подключения. Что делать?

Убедитесь, что при создании подключений выбраны Dynamics 365 Finance и Common Data Service.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>При синхронизации занятости возникают ошибки «CompanyInfo_FK не существует» или «Значение "31.12.2154 23:59:59" в поле "Дата окончания занятости" не найдено в связанной таблице "Занятость"». Что делать?

Убедитесь, что сопоставляются правильные юридические лица. Синхронизация юридических лиц не является частью шаблона по умолчанию, поэтому ожидается, что каждое юридическое лицо, которое присутствует в Human Resources и Common Data Service, также присутствует в Finance.
Кроме того, убедитесь, что выбраны правильные юридические лица для связанного набора соединений.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>После настройки проекта сопоставление полей для Finance выглядит пустым. Что делать?

Обновите информационные объекты в Finance, перейдя в **Управление данными \> Параметры структуры \> Параметры объекта \> Обновить список объектов**. Данная процедура займет несколько минут, затем вы должны увидеть эти сопоставления. Эта проблема возникает при создании новых проектов.

![Отсутствует сопоставление полей](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

- Интегратор данных (DI): 

  - [Интеграция данных в Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [Управление ошибками и устранение неполадок интегратора данных](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [Ответ на запросы DSR для созданных системой журналов в Power Apps, Microsoft Power Automate и Common Data Service](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Управление данными:

  - [Управление данными](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
