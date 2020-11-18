---
title: Вопросы и ответы по вводу в эксплуатацию
description: В этой теме перечислены часто задаваемые вопросы о том, как ввести в эксплуатацию проект реализации Dynamics 365 Human Resources.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64a85840be328702a06779390fe383fd1896fd04
ms.sourcegitcommit: d66fd72342931fad25a696b251c05781280d36c4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "4011436"
---
# <a name="go-live-faq"></a>Вопросы и ответы по вводу в эксплуатацию 

В этой теме перечислены часто задаваемые вопросы о том, как ввести в эксплуатацию проект реализации Dynamics 365 Human Resources. 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>Когда можно настроить и запросить производственную среду? 

Обычно производственная среда разворачивается после того, как удовлетворяются следующие критерии:

- Код всех настроек завершен.
- Приемочное тестирование пользователем (UAT) завершено.
- Клиент утвердил решение.
- Нет блокирующих проблем для ввода в эксплуатацию. 

Если на данном этапе имеются квалифицированные клиенты, группа Microsoft FastTrack будет работать с группой проекта, чтобы выполнить оценку ввода в эксплуатацию. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>Какие необходимые условия для развертывания производственной среды? 

Список необходимых требований см. в разделе  [Подготовка к вводу в эксплуатацию](hr-admin-go-live-prepare.md). 

## <a name="what-is-a-go-live-assessment"></a>Что такое оценка ввода в эксплуатацию?  

Оценка ввода в эксплуатацию является частью  [программы Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview). Во время этого рассмотрения архитектор решений оценивает, готов ли проект реализации к успешному переключению и вводу в эксплуатацию. Эта проверка является обязательной для каждого проекта реализации до того, как вы сможете запросить ввод в эксплуатацию в производственной среде. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>Наши среды в песочнице развернуты в центре обработки данных в центральной части США. Мы хотим, чтобы наши производственные среды были развернуты в центре обработки данных в западной части США. Можно ли выбрать западную часть США в качестве центра обработки данных в моей производственной конфигурации? 

LCS не ограничивает выбор других центров обработки данных при развертывании среды Human Resources, но настоятельно не рекомендуется выбирать другой центр обработки данных.  

Если требуется, чтобы производственная среда была в центре обработки данных в западной части США, необходимо сначала заново развернуть среды в песочнице в центре обработки данных в западной части США, проверить их и утвердить. 

Сведения о выборе правильного центра обработки данных см. в разделе [Требования к сети](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements). 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>Какой уровень доступа требуется для ресурсов Azure в моих средах Human Resources?  

Доступ к средам Human Resources ограничивается. У вас нет доступа к виртуальной машине (VM) или Microsoft Internet Information Services (IIS). Доступ к базе данных также невозможен через Microsoft SQL Server Management Studio. 

Хотя непосредственное обращение к вашим ресурсам Azure или среде Dynamics 365 Human Resources, можно использовать дополнительные функции для доступа к данным:

- Можно развернуть базу данных SQL Azure в своем собственном клиенте Azure и использовать функцию "назначить собственную базу данных" (BYOD) для синхронизации данных. Дополнительные сведения см. в разделе [Использование собственной базы данных (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).

- Можно использовать интеграцию Common Data Service для синхронизации выбранных сущностей в базе данных Common Data Service. Дополнительные сведения см. в разделе [Сущности Common Data Service](hr-developer-entities.md). 

## <a name="how-often-is-my-production-database-backed-up"></a>Как часто архивируется моя производственная база данных? 

Базы данных защищаются автоматическим созданием резервных копий при следующих частотах:

| Тип резервного копирования | Частота |
| --- | --- |
| Полная резервная копия баз данных | Еженедельно |
| Разностная резервная копия баз данных | Каждые 12–24 часа |
| Резервное копирование журнала транзакций | Каждые 5–10 минут |

Корпорация Майкрософт сохраняет необходимые резервные копии, чтобы иметь возможность восстановления до точки во времени (PITR) в течение последних семи дней. 

Дополнительные сведения см. в разделе  [Подробнее об автоматически создаваемых резервных копиях в базе данных SQL](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database). 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>Можно ли запросить копию резервной копии производственной базы данных? 

№ п/п Однако можно отправить запрос на обслуживание обновления базы данных, чтобы скопировать свою производственную среду в среду "песочницы". Можно развернуть базу данных SQL Azure в своем собственном клиенте Azure и использовать функцию BYOD для синхронизации данных из производственной среды. Дополнительные сведения см. в разделе [Использование собственной базы данных (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>Как переместить среду "песочницы" в производство для ввода в эксплуатацию? 

Поскольку функция копирования недоступна для переноса среды из среды песочницы в производственную среду, необходимо использовать пакеты данных для переноса данных в производственную среду.  

Рекомендуется поддерживать четкий список сущностей, настроенных в вашей среде песочницы в течение всего проекта. Затем проверьте процесс переключения и миграцию каких-либо пакетов данных, необходимых для ввода в эксплуатацию. Необходимо вручную переместить любые пакеты данных в производственную среду, когда будете готовы к вводу в эксплуатацию. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>Что делать, если производственная среда не работает? 

Чтобы сообщить об отключении производственной среды, следуйте процедуре, описанной в разделе  [Отчет об отключении производства](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage). 

 ## <a name="see-also"></a>См. также

 [Подготовка к вводу в эксплуатацию](hr-admin-go-live-prepare.md)