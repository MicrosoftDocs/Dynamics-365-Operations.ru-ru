---
title: Обзор политик консолидации отгрузок
description: В этой статье представлен обзор функциональных возможностей, обеспечивающих гибкую настройку политик консолидации отгрузок.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationError, WHSShipConsolidationSetShipment, WHSShipConsolidationPolicySelect, WHSShipPlanningListPage, TMSCarrierGroup, WHSShipConsolidationTemplate, WHSShipConsolidationTemplateApply, WHSShipConsolidationTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 7113fc635a7c01e4b9cc44898daa3d2617058b6b
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427937"
---
# <a name="shipment-consolidation-policies-overview"></a>Обзор политик консолидации отгрузок

[!include [banner](../includes/banner.md)]

Процесс консолидации отгрузок, использующий политики консолидации отгрузок, позволяет использовать автоматическую консолидацию отгрузок во время автоматического и ручного запуска на склад. Автоматизированная консолидация, которая была доступна до того, как была введена эта функция, имела жестко запрограммированные поля и была основана на поле **Консолидировать отгрузку перед запуском на склад**, которое было задано для склада.

Политики консолидации отгрузок используются для следующих функций:

- Пакетное задание автоматического выпуска на склад
- Команда **Запуск на склад** в заказе на продажу или в заказе на перемещение
- Страница Специальный **Запуск на склад**
- Команда **Запуск на склад** на странице **Рабочем месте планирования загрузки**
- Ручная консолидация отгрузок на страницах **Консолидация отгрузок** и **Рабочее место консолидации отгрузок**

Прежде чем были введены политики консолидации отгрузок, функция консолидации существовала как настройка на уровне склада. Все заказы для всех клиентов одного склада рассматривались так же, как и в случае одинаковых требований консолидации. Политики консолидации отгрузок позволяют добавлять поддержку сценариев, в которых различные организации имеют различные требования для консолидации отгрузок.

Запросы используются для определения применяемой политики консолидации отгрузок, а затем редактируемый набор полей определяет порядок группировки строк загрузки на уровне отгрузки. (Этот шаблон напоминает шаблон, которым следуют шаблоны волн.) Кроме того, в каждую политику добавляется параметр **Консолидация с существующими отгрузками**. Если этот параметр включен, процедура *Запуск на склад* позволяет найти отгрузки для консолидации, выполняя поиск среди существующих отгрузок, созданных на основе одной и той же политики консолидации. В этом случае система выберет существующую отгрузку или загрузку вместо того, чтобы создавать новые. Однако система будет выполнять консолидацию только с существующими отгрузками, имеющими статус *открыт*; отгрузки со статусом *запущено* или выше не будут рассматриваться как цели консолидации.

Когда функция *Политики консолидации отгрузок* включена для вашей системы, параметр **Консолидировать отгрузку перед выпуском на склад**, который ранее был доступен на странице настройки **Склады**, скрыт. Для облегчения перехода к новой функции консолидации отгрузок функция страница **Политики консолидации отгрузок** позволяет создать политику по умолчанию, которая автоматически включает старые настройки для существующих складов. После создания политики по умолчанию, параметр **Консолидировать отгрузку перед запуском на склад** на странице **Настройка складов** больше учитываться не будет. Дополнительные сведения см. в разделе [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md).

Можно использовать страницу **запуск на склад**, чтобы вручную переопределить применимую политику консолидации тем же способом, что и для переопределения политик выполнения.

Можно использовать команду **Запуск в производство \> Запуск на склад** на странице **Рабочее место планирования загрузки**, чтобы собрать исходящие загрузки, основанные на заказе на продажу и строках заказа на перемещение перед выполнением выпуска на склад. Эти загрузки используют одну и ту же логику консолидации, которая была введена вместе с консолидацией политик отгрузки.

Можно использовать страницу **Рабочее место консолидации отгрузок** , чтобы консолидировать существующие отгрузки, которые еще не были подтверждены, но уже были запущены на склад. Эта функция поддерживает сценарии, в которых автоматизированный процесс запуска в производство, имеющий собственную консолидацию отгрузки, запускается несколько раз в день, но возможные дополнительные консолидации вручную определяются до завершения отгрузки перевозчикам в ходе процесса подтверждения. Эта функция позволяет консолидировать исходящие отгрузки, созданные из строк заказа на продажу или заказа на перемещение в любое время после выпуска отгрузок на склад, но перед подтверждением.

Страница **Рабочее место консолидации отгрузок** функционирует подобно рабочее место формирования загрузок, где можно одновременно оценивать несколько отгрузок и назначить неконсолидированный заказ для определенной отгрузки. Шаблоны консолидации отгрузок можно применять для оценки предлагаемых консолидаций несколько раз и для их подтверждения. Некоторые правила реализованы для предотвращения неавторизованной консолидации и предупреждения о возможных ошибках.

## <a name="overview-of-new-functionality"></a>Обзор новых функциональных возможностей

В этом разделе описываются страницы, команды и функции, которые были изменены или добавлены при включении и использовании функции *политики консолидации отгрузок*.

### <a name="shipment-consolidation-policies-page"></a>Страница политик консолидации отгрузок

Политики различаются по типу заказов на работу. Тип **заказов на продажу** представляет отгрузки по _заказу на продажу_, а тип **заказов на перемещение** представляет отгрузки _Выдача на перемещение_.

Каждая политика консолидации отгрузок содержит запрос, определяющий, когда он применяется, и порядковый номер, определяющий порядок выполнения. Консолидация применяется для каждой уникальной комбинации выбранных полей. Дополнительный параметр используется для консолидации с существующими (открытыми) отгрузками. Эти политики оцениваются и применяются каждый раз, когда создается новая отгрузка (до обработки волн).

Если в политике отсутствуют обязательные поля или в нее включены какие-либо запрещенные поля, эта политика помечается как недопустимая в разделе **Выбрано**. Списки обязательных и запрещенных полей являются жестко запрограммированными и могут быть расширены.

В следующем списке показаны обязательные поля. Поскольку отгрузки всегда разбиваются на основе этих полей, невозможно сгруппировать несколько отгрузок, имеющих различные значения для этих полей.

- Заказы на продажу

    - **Номер счета:** _WHSShipmentTable.AccountNum_
    - **Получатель доставки:** _WHSShipmentTable.DeliveryName_
    - **Почтовый адрес (RecId):** _WHSShipmentTable.DeliveryPostalAddress_
    - **Склад:** _WHSShipmentTable.InventLocationId_

- Для заказы на перемещение:

    - **Со склада:** _InventTransferTable.InventLocationIdFrom_
    - **На склад:** _InventTransferTable.InventLocationIdTo_

Следующие поля недоступны для всех типов документов. Эти поля не отображаются в интерфейсе пользователя и не могут использоваться для консолидации.

- **Код отгрузки:** _WHSShipmentTable.ShipmentId_
- **Статус:** _WHSShipmentTable.ShipmentStatus_
- **Политика консолидации отгрузок:** _WHSShipmentTable.ShipConsolidationPolicyName_
- **Тип проводки работы:** _WHSShipmentTable.WorkTransType_
- **Код волны:** _WHSShipmentTable.WaveId_
- **Код загрузки:** _WHSShipmentTable.LoadId_
- **Код отгрузки:** _WHSLoadLine.ShipmentId_
- **Код загрузки:** _WHSLoadLine.LoadId_

По умолчанию при создании политики набор обязательных полей используется в качестве полей консолидации. Однако список можно изменить с помощью кнопок со стрелками влево и вправо. (Процесс напоминает процесс выбора способов в шаблонах волн.)

Значения, выбранные пользователями для этих полей, будут использоваться для всех вновь создаваемых отгрузок, или они будут добавлены в существующие отгрузки в ходе консолидации с этими отгрузками. Когда две отгрузки имеют одинаковое значение для поля, выбранного для консолидации этих отгрузок, отгрузки консолидируются. Этот же принцип применяется для всех последующих полей консолидации, которые выбраны. Если значения различаются, вторая отгрузка сбрасывается и выбирается для новой отгрузки. Процесс автоматической консолидации состоит из создания всех уникальных комбинаций значений полей консолидации отгрузок и последующего назначения отгрузки соответствующей комбинации.

Невыбранные поля игнорируются в процессе консолидации. Если для невыбранных полей две отгрузки имеют различающиеся значения, это поле очищается (то есть оно задается пустым). Если обе отгрузки имеют одинаковое значение для невыбранных полей, поле заполняется.

Список полей консолидации (то есть полей, которые будут очищены, если они имеют другие значения) является жестко запрограммированным. Список содержит все поля, которые инициализируются в строке заказа на продажу или заказа на перемещение при создании новой отгрузки. Другими словами, если поле не инициализировано из строки заказа на продажу или заказа на перемещение, оно игнорируется при добавлении новых данных в существующую отгрузку.

### <a name="release-to-warehouse-page"></a>Страница «Запуск на склад»

- Новое поле в нижней сетке отображает примененную политику консолидации.
- Новая кнопка позволяет вручную выбрать и/или переопределить политику консолидации.

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>Команда Запуск на склад на странице Рабочее место планирования загрузки

- Логика была настроена так, что использует примененные политики консолидации.
- Отгрузки в данный состав консолидируются только в рамках одной загрузки.

### <a name="consolidate-shipments-page"></a>Страница Консолидация отгрузок

- Поиск аналогичных отгрузок (то есть кандидатов для консолидации) был изменен так, чтобы он использовал поля, выбранные в политике консолидации отгрузок.
- Поля, имеющие различающиеся значения в других отгрузках, в данный форме устанавливаются как пустые. (Ранее использовались значения из выбранной отгрузки "базовая".)

### <a name="shipment-consolidation-workbench-page"></a>Страница Рабочее место консолидации отгрузок

- Новая функциональность копирует процесс консолидации вручную с большим масштабом.
- Теперь эту страницу можно открыть из меню **Запуск на склад** в модуле **Управление складом**.
- Алгоритм анализирует существующие отгрузки, которые еще не были отгружены. Затем она предлагает консолидацию на основе полей, выбранных в политиках консолидации.

## <a name="comparison-of-functionality"></a>Сравнение функций

В следующей таблице показано, как выполняется консолидация отгрузки, когда не используются политики консолидации отгрузок и когда они используются.

| Без политик консолидации отгрузок | С политиками консолидации отгрузок |
|---|----|
| Неприменимо | Отгрузки по продажам или перемещению, выбранные для консолидации, должны иметь ту же политику консолидации, что и создаваемая отгрузка, или они должны быть назначены открытой отгрузке (когда включен параметр **Консолидация с существующими отгрузками** ). |
| Процедура *Запуск на склад* не выполняет поиск по существующим отгрузкам, чтобы найти отгрузку для консолидации. Для поиска отгрузки для консолидации используются только отгрузки, созданные текущим экземпляром процедуры *Запуск на склад*. | Если для используемой в данный момент политики консолидации включен параметр **консолидация с существующими отгрузками**, то процедура *запуск на склад* выполняет поиск среди существующих отгрузок, созданных на основе той же политики консолидации для поиска отгрузки для консолидации. Таким образом, если имеется две политики, отгрузка, создаваемая на основе политики 2, никогда не будет консолидироваться с отгрузкой, созданной на основе политики 1. |
| Неприменимо | Если список полей политики консолидации пуст, или если политика не найдена, создается новая отгрузка для каждой строки заказа на продажу или заказа на перемещение. |
| Следующее поле консолидации определяет уникальное сочетание значений, используемых для консолидации отгрузок для *строки перемещения*. (Все остальные поля игнорируются.)<ul><li>Номер заказа (OrderNum)</li></ul> | Следующее поле консолидации определяет уникальное сочетание значений, используемых для консолидации отгрузок для *строки перемещения*. (Все остальные поля игнорируются.)<ul><li>Номер заказа (OrderNum)</li><li>Получатель поставки (DeliveryName)</li><li>Почтовый адрес (DeliveryPostalAddress)</li><li>Код страны ISO (CountryRegionISOCode)</li><li>Адрес (Address)</li><li>Узел (InventSiteId)</li><li>Склад (InventLocationId)</li><li>Перевозчик, осуществляющий доставку (CarrierCode)</li><li>Услуга перевозчика (CarrierServiceCode)</li><li>Режим доставки (ModeCode) \*</li><li>Группа перевозчика (CarrierGroupCode)</li><li>Условия поставки (DlvTermId)</li></ul><p>Эти поля являются единственными полями, доступными и инициализированными при создании новой отгрузки.</p><p>\*Примечание: *ModeCode* является **режимом**, назначенным **перевозчику**, выбранному для доставки строки перемещения (но не к **способу доставки** , выбранному для строки перемещения). Если вы решили включить *режим поставки (ModeCode)* среди критериев консолидации, система выполнит консолидацию только строк перемещения с тем же значением **режима**, при условии, что **перевозчик**, **услуга перевозчика**, и **режим доставки** определяются для данной строки (независимо от их значений). Кроме того, система также консолидирует все строки перемещения, в которых этот **режим** пуст.</p> |
| Следующее поле консолидации определяет уникальное сочетание значений, используемых для консолидации отгрузок для *строки продажи*. (Все остальные поля игнорируются.)<ul><li>Номер заказа (OrderNum)</li><li>Ссылка клиента (CustomerRef)</li><li>Заявка клиента (CustomerReq)</li><li>Условия поставки (DlvTermId)</li></ul> | Следующее поле консолидации определяет уникальное сочетание значений, используемых для консолидации отгрузок для *строки продажи*. (Все остальные поля игнорируются.)<ul><li>Номер заказа (OrderNum)</li><li>Номер счета (AccountNum)</li><li>Получатель поставки (DeliveryName)</li><li>Почтовый адрес (DeliveryPostalAddress)</li><li>Код страны ISO (CountryRegionISOCode)</li><li>Адрес (Address)</li><li>Узел (InventSiteId)</li><li>Склад (InventLocationId)</li><li>Перевозчик, осуществляющий доставку (CarrierCode)</li><li>Услуга перевозчика (CarrierServiceCode)</li><li>Режим доставки (ModeCode) \*</li><li>Группа перевозчика (CarrierGroupCode)</li><li>Код брокера (BrokerCode)</li><li>Направление (LoadDirection)</li><li>Условия поставки (DlvTermId)</li><li>Ссылка клиента (CustomerRef)</li><li>Заявка клиента (CustomerReq)</li></ul><p>Эти поля являются единственными полями, доступными и инициализированными при создании новой отгрузки.</p><p>\*Примечание: *ModeCode* является **режимом**, назначенным **перевозчику**, выбранному для строки продажи (но не к **способу доставки** , выбранному для строки продажи). Если вы решили включить *режим поставки (ModeCode)* среди критериев консолидации, система выполнит консолидацию только строк продаж с тем же значением **режима**, при условии, что **перевозчик**, **услуга перевозчика**, и **режим доставки** определяются для данной строки (независимо от их значений). Кроме того, система также консолидирует все строки продаж, в которых этот **режим** пуст.</p> |
| Неприменимо | Следующие поля консолидации являются обязательными для *строки продажи* и не могут быть удалены:<ul><li>Номер счета (AccountNum)</li><li>Получатель поставки (DeliveryName)</li><li>Почтовый адрес (DeliveryPostalAddress)</li><li>Склад (InventLocationId)</li></ul>По умолчанию эти поля будут назначены при создании новой политики. Их невозможно удалить. |
| В процедуре *Запуск загрузок на склад* на странице **Рабочее место планирования загрузки** используется собственный отдельный код для создания отгрузок и волн. | Политики консолидации отгрузок используются для определения полей, которые должны быть оценены для консолидации. Отгрузки консолидируются только в рамках одной загрузки. |
| Вручную выберите **консолидация отгрузок** на странице **все отгрузки** , а затем выберите целевой "основной" отгрузки. Фильтр предложит все существующие отгрузки, имеющие одинаковые значения для нескольких ключевых полей. | Вручную выберите **консолидация отгрузок** на странице **все отгрузки** , а затем выберите целевой "основной" отгрузки. Система предложит другие существующие отгрузки, соответствующие значениям нескольких ключевых полей, настроенных для соответствующих политик консолидации отгрузок. |
| Можно использовать команду **консолидировать отгрузки** на странице **все отгрузки** только для одной отгрузки. | Страница **Рабочее место консолидации отгрузок** позволяет найти набор отгрузок, которые еще не находятся в состоянии "отгружено". Эти отгрузки анализируются на основе нескольких ключевых полей, настроенных в политиках консолидации отгрузок. Все отгрузки, для которых значения этих полей совпадают, предлагаются для консолидации.<p>Консолидацию можно выполнить вручную, удалив отгрузки из предложенных консолидаций и/или добавив отгрузки в них. Могут возникать различные типы ошибок, но некоторые из них можно переопределить.</p> |
| **Примечание:** процедуры *Автоматический запуск заказов на продажу на склад* разделяет строки продаж по группам. Каждая группа имеет собственное уникальное значение **ReleaseToWarehouseId** и обрабатывается отдельно в соответствии с процедурой *Запуск на склад*. Эта процедура создает новую работу независимо от настройки перерыва в работе. | **Примечание:** процедура *Автоматический запуск заказов на продажу на склад* назначает одно и то же значение **ReleaseToWarehouseId** всем обрабатываемым строкам продаж. Все строки продаж обрабатываются в одно и то же время с помощью процедуры *Запуск на склад*. Для обеспечения более раннего поведения необходимо настроить для кода отгрузки его перерыв в работе. |

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Настройка политик консолидации отгрузок](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]