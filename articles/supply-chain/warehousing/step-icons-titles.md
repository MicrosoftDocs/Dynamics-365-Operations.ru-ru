---
title: Назначение значков и названий шагов для мобильного приложения Warehouse Management
description: В этом разделе описывается, как назначать значки и названия шагов для новых или настроенных потоков задач для мобильного приложения Warehouse Management.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a74847b50512d2f712e5a9a5125e520afc732591
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344503"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>Назначение значков и названий шагов для мобильного приложения Warehouse Management

[!include [banner](../includes/banner.md)]

В этом разделе описывается, как назначать значки шагов и названия шагов для новых или настроенных потоков задач для мобильного приложения Warehouse Management.

На следующем рисунке показано, как будут отображаться значки и названия шагов в мобильном приложении Warehouse Management.

![Пример значка шага и названия шага в мобильном приложении Warehouse Management.](media/step-icon-example.png "Пример значка шага и названия шага в мобильном приложении Warehouse Management")

## <a name="turn-on-this-feature-in-your-system"></a>Включение этой функции в системе

Прежде чем использовать эту функцию, она должна быть включена в системе. Администраторы могут использовать параметры [Управление компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения. В рабочей области **Управление функциями** эта функция перечисляется следующими способами:

- **Модуль:** *Управление складом*
- **Название компонента:** *Параметры пользователя, значки и названия шагов для нового приложения склада*

## <a name="standard-step-ids-classes-and-icons"></a>Идентификаторы, классы и значки стандартных шагов

Каждый шаг в потоке задач определяется с помощью идентификатора шага, и у каждого идентификатора шага имеется соответствующий класс шага. Значок и заголовок шага указаны в каждом из классов шагов.

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>Идентификаторы шагов и классы шагов

В следующей таблице перечислены все доступные идентификаторы шагов, а также соответствующий класс шага. В качестве идентификатора шага используется имя элемента управления первичного поля ввода.

Пример использования этих идентификаторов шагов и классов см. в реализации метода `WHSMobileAppStepInfoBuilder.stepId()` в разделе [Пример: назначение значков и заголовков шагов для настраиваемого потока](#example) далее в этой теме.

| Идентификатор шага | Класс шага |
|-|-|
| BatchDisposition | WHSMobileAppStepBatchDisposition |
| Перевозчик | WHSMobileAppStepCarrier |
| CatchWeight | WHSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WHSMobileAppStepCatchWeight |
| CatchWeightTag | WHSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WHSMobileAppStepCatchWeightTagWeight |
| ChangeWarehouseSuccess | WHSMobileAppStepChangeWarehouseSuccess |
| CheckDigit | WHSMobileAppStepCheckDigit |
| ClusterId | WHSMobileAppStepClusterId |
| ClusterPickQtyVerification | WHSMobileAppStepQtyVerification |
| ClusterPosition | WHSMobileAppStepClusterPosition |
| ConfigId | WHSMobileAppStepConfigId |
| Подтверждение | WHSMobileAppStepConfirmation |
| ConsolidateFromLicensePlateId | WHSMobileAppStepConsolidateFromLicensePlateId |
| ConsolidateLPConfirmation | WHSMobileAppStepConsolidateLPConfirmation |
| ConsolidateToLicensePlateId | WHSMobileAppStepConsolidateToLicensePlateId |
| ContainerType | WHSMobileAppStepContainerType |
| CountingReasonCode | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WHSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WHSMobileAppStepCycleCountQty |
| CycleCountQty2 | WHSMobileAppStepCycleCountQty |
| CycleCountQty3 | WHSMobileAppStepCycleCountQty |
| CycleCountQty4 | WHSMobileAppStepCycleCountQty |
| Disposition | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| DriverCheckOutId | WHSMobileAppStepDriverCheckOutId |
| ExpDate | WHSMobileAppStepExpDate |
| FromBatchDisposition | WHSMobileAppStepFromBatchDisposition |
| FromInventoryStatus | WHSMobileAppStepInventoryStatusFrom |
| FullQty | WHSMobileAppStepFullQty |
| InboundPut | WHSMobileAppStepInboundPut |
| InventBatchId | WHSMobileAppStepBatch |
| InventColorId | WHSMobileAppStepInventColorId |
| InventLocation | WHSMobileAppStepInventLocation |
| InventLocationId | WHSMobileAppStepWarehouse |
| InventSerialId | WHSMobileAppStepInventSerialId |
| InventSizeId | WHSMobileAppStepInventSizeId |
| InventStatusId | WHSMobileAppStepInventStatus |
| InventStyleId | WHSMobileAppStepInventStyleId |
| InventVersionId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMContainerID | ITMMobileAppStepContainerId |
| ITMShipmentID | ITMMobileAppStepShipmentId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanOrCardId | WHSMobileAppStepKanbanCard |
| LicensePlateId | WHSMobileAppStepLicensePlate |
| LoadId | WHSMobileAppStepLoadId |
| LocationLicensePlatePosition | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPCheck | WHSMobileAppStepLocOrLPCheck |
| LocVerification | WHSMobileAppStepLocVerification |
| LPAdjustIn | WHSMobileAppStepLPAdjustIn |
| LPBreakChildLP | WHSMobileAppStepLPBreakChildLP |
| LPBreakParentLP | WHSMobileAppStepLPBreakParentLP |
| LPBuildChildLP | WHSMobileAppStepLPBuildChildLP |
| LPBuildParentLP | WHSMobileAppStepLPBuildParentLP |
| LPVerification | WHSMobileAppStepLPVerification |
| MergeContainerId | WHSMobileAppStepMergeContainerId |
| MixedLPLineNum | WHSMobileAppStepMixedLPLineNum |
| MobileDeviceQueueMessageCollectionIdentifierId | WHSMobileAppStepSelectOrder |
| MovementConfirmCancel | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WHSMobileAppStepCatchWeight |
| NewQty | WHSMobileAppStepNewQty |
| OutboundCatchWeightTag | WHSMobileAppStepCatchWeightTag |
| OutboundPut | WHSMobileAppStepOutboundPut |
| OutboundWeight | WHSMobileAppStepCatchWeight |
| OverridePutNewLocation | WHSMobileAppStepOverridePutNewLocation |
| PieceByPieceConfirmation | WHSMobileAppStepQtyVerification |
| POLineNum | WHSMobileAppStepPOLineNum |
| Номер заказа на покупку | WHSMobileAppStepPONum |
| PositionFull | WHSMobileAppStepPositionFull |
| PositionFullQty | WHSMobileAppStepPositionFullQty |
| Доля | WHSMobileAppStepPotency |
| PrinterName | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdLastPalletConfirmation | WHSMobileAppStepProdLastPalletConfirmation |
| ProductConfirmation | WHSMobileAppStepProductConfirmation |
| ProductionScrapConfirmation | WHSMobileAppStepProductionScrapConfirmation |
| Поместить | WHSMobileAppStepPut |
| PutawayClusterId | WHSMobileAppStepPutawayClusterId |
| Кол-во | WHSMobileAppStepQty |
| QtyAdjust | WHSMobileAppStepQtyAdjust |
| QtyShort | WHSMobileAppStepQtyShort |
| QtyToConsume | WHSMobileAppStepQtyToConsume |
| QtyToPick | WHSMobileAppStepQtyToPick |
| QtyToPut | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| QtyVerification | WHSMobileAppStepQtyVerification |
| QtyWithScanningLimit | WHSMobileAppStepQtyAdjust |
| ReasonString | WHSMobileAppStepReasonString |
| RecvLocationId | WHSMobileAppStepRecvLocationId |
| RemoveContainerId | WHSMobileAppStepRemoveContainerId |
| ReprintLabelConfirmation | WHSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| ShortPickReason | WHSMobileAppStepShortPickReason |
| SortConOrLP | WHSMobileAppStepSortConOrLP |
| SortLicensePlateId | WHSMobileAppStepSortLicensePlateId |
| SortPositionId | WHSMobileAppStepSortPositionId |
| SortVerification | WHSMobileAppStepSortVerification |
| StartLocationId | WHSMobileAppStepStartLocationId |
| StartProdOrderConfirmation | WHSMobileAppStepStartProdOrderConfirmation |
| TargetLicensePlateId | WHSMobileAppStepTargetLicensePlateId |
| TOLineNum | WHSMobileAppStepTOLineNum |
| ToLocation | WHSMobileAppStepToLocation |
| TONum | WHSMobileAppStepTONum |
| ToWarehouse | WHSMobileAppStepWarehouseTo |
| TransportLoadId | WHSMobileAppStepTransportLoadId |
| WaveLabelId | WHSMobileAppStepWaveLabelId |
| WaveLblQty | WHSMobileAppStepWaveLblQty |
| Вес | WHSMobileAppStepWeight |
| WeightToConsume | WHSMobileAppStepWeightToConsume |
| WHSAdjustmentType | WHSMobileAppStepWHSAdjustmentType |
| WHSReceivingException | WHSMobileAppStepWHSReceivingException |
| WHSWorkException | WHSMobileAppStepWHSWorkException |
| WHSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobileAppStepLocation |
| WorkId | WHSMobileAppStepWorkId |
| WorkIdToCancel | WHSMobileAppStepWorkIdToCancel |
| WorkLPIdPutawayCluster | WHSMobileAppStepWorkLPIdPutawayCluster |
| WorkPoolId | WHSMobileAppStepWorkPoolId |
| ZoneId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>Доступные значки шагов

В системе имеется набор стандартных значков шагов, которые также можно использовать для пользовательских шагов. Сейчас вы не можете отправлять значки пользовательских шагов. Поэтому следует всегда выбирать один из стандартных значков шагов.

В следующей таблице представлен каждый стандартный значок шагов, который в настоящее время доступен, и его имя.

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Значок шага описания"><br>О программе</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Значок шага добавления грузоместа или номенклатуры"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Значок этапа обработки партии"><br>BatchDisposition</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Значок шага перевозчика"><br>Перевозчик</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Значок шага тега учета в двух единицах измерения"><br>CatchWeightTag</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Значок шага веса тега учета в двух единицах измерения"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Значок шага контрольного разряда"><br>CheckDigit</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Значок шага кода получения или возврата"><br>CheckInOutId</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Значок шага дочернего грузоместа"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Значок шага идентификатора кластера"><br>ClusterId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Значок шага положения кластера"><br>ClusterPosition</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Значок шага идентификатора конфигурации"><br>ConfigId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Значок шага настраиваемого поля"><br>ConfiguredField</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Значок шага контейнера или грузоместа"><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Значок шага консолидации из кода грузоместа"><br>ConsolidateFromLicensePlateID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Значок шага консолидации в код грузоместа"><br>ConsolidateToLicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Значок шага типа контейнера"><br>ContainerType</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Значок шага инвентаризации"><br>Инвентаризация</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Значок шага кода причины инвентаризации"><br>CountingReasonCode</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Значок шага кода страны происхождения"><br>CountryOfOrigin</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Значок шага обработки"><br>Disposition</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Значок шага завершения"><br>Выполнено</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Значок шага подтверждения прибытия водителя"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Значок шага кода прибытия водителя"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Значок шага кода отбытия водителя"><br>DriverCheckOutId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Значок шага даты окончания срока действия"><br>ExpDate</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Значок шага поля"><br>Поле</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Значок шага обработки из партии"><br>FromBatchDisposition</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Значок шага статуса из запасов"><br>FromInventoryStatus</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Значок шага атрибута идентификатора"><br>IdAttribute</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Значок шага кода складской партии"><br>InventBatchID</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Значок шага кода цвета запасов"><br>InventColorID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Значок шага местоположения запасов"><br>InventLocation</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Значок шага кода серийного номера запасов"><br>InventSerialID</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Значок шага кода размера запасов"><br>InventSizeID</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Значок шага кода статуса запасов"><br>InventStatusID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Значок шага кода стиля запасов"><br>InventStyleID</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Значок шага кода версии запасов"><br>InventVersionID</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Значок шага идентификатора номенклатуры"><br>ItemID</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Значок шага кода контейнера ITM"><br>ITMContainerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Значок шага кода отгрузки ITM"><br>ITMShipmentID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Значок шага кода карты канбана"><br>KanbanCardID</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Значок шага кода канбана или карточки"><br>KanbanOrCardID</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Значок шага кода грузоместа"><br>LicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Значок шага идентификатора загрузки"><br>LoadId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Значок шага позиции грузоместа в местонахождении"><br>LocationLicensePlatePosition</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Значок шага местоположения или грузоместа"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Значок шага проверки местоположения или грузоместа"><br>LocOrLPCheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Значок шага исходного местоположения или грузоместа"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Значок шага целевого местоположения или грузоместа"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Значок шага завершения продолжительной обработки"><br>LongProcessCompleted</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Значок шага разбиения грузоместа родительского грузоместа"><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Значок шага кода объединения контейнера"><br>MergeContainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Значок шага нумерации строк смешанного грузоместа"><br>MixedLPLineNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Значок шага исходящего веса"><br>OutboundWeight</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Значок шага владельца"><br>Ответственный</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Значок шага родительского грузоместа"><br>ParentLP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Значок шага подтверждения"><br>PleaseConfirm</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Значок шага номера строки заказа на продажу"><br>POLineNum</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Значок шага номера заказа на продажу"><br>Номер заказа на покупку</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Значок шага заполненной позиции"><br>PositionFull</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Значок шага доли"><br>Доля</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Значок шага имени принтера"><br>PrinterName</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Значок шага идентификатора продукта"><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Значок шага подтверждения продукта"><br>ProductConfirmation</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Значок шага размещения"><br>Поместить</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Значок шага идентификатора кластера размещения"><br>PutawayClusterId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Значок шага количества"><br>Кол-во</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Значок шага корректировки количества"><br>QtyAdjustIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Значок шага недостающего количества"><br>QtyShort</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Значок шага количества для потребления"><br>QtyToConsume</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Значок шага количества для размещения"><br>QtyToPut</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Значок шага количества для списания в отходы"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Значок шага подтверждения количества"><br>QuantityConfirmation</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Значок шага приемки завершенного задания"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Значок шага идентификатора местоположения получения"><br>RecvLocationID</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Значок шага удаления кода контейнера"><br>RemoveContainerID</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="Значок шага номера RMA"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Значок шага выбора заказа"><br>SelectOrder</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Значок шага причины недоукомплектования"><br>ShortPickReason</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Значок шага кода позиции сортировки"><br>SortPositionId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Значок шага кода целевого грузоместа"><br>TargetLicensePlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Значок шага номера целевой строки"><br>ToLineNum</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Значок шага целевого местоположения"><br>ToLocation</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Значок шага целевого номера"><br>ToNum</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Значок шага целевого склада"><br>ToWarehouse</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Значок шага идентификатора транспортной загрузки"><br>TransportLoadId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Значок шага кода партии поставщика"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Значок шага кода метки волны"><br>WaveLabelId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Значок шага количества метки волны"><br>WaveLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Значок шага веса"><br>Вес</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Значок шага веса для потребления"><br>WeightToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="Значок шага типа корректировки WHS"><br>WHSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="Значок шага исключения приемки WHS"><br>WHSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Значок шага кода местоположения WHS"><br>WMSLocationID</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Значок шага идентификатора работы"><br>WorkId</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Значок шага кода работы для отмены"><br>WorkIdToCancel</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Значок шага кода грузоместа работы"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Значок шага кластера размещения кода грузоместа работы"><br>WorkLPIDPutawayCluster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Значок шага идентификатора пула работ"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Значок шага идентификатора зоны"><br>ZoneID</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>Пример: назначение значков и заголовков шагов для настраиваемого потока

В этом примере объясняется, как настроить значки и названия шагов для настраиваемого потока задач. Сценарий создан на примере пользовательского потока задач, который более подробно представлен и изучен в следующей записи блога: [Настройка складских приложений для мобильных устройств](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app). Поток задач выполняется следующим образом:

1. Приложение отображает страницу, которая предлагает сотруднику указать идентификатор контейнера (например, путем сканирования штрих-кода).
1. Если код контейнера допустим, приложение открывает новую страницу, которая предлагает сотруднику ввести вес. (Если код контейнера недействителен, сотрудник возвращается на первую страницу.)
1. Когда работник вводит допустимый вес, система сохраняет вес и возвращает сотрудника на первую страницу.

Следующая иллюстрация показывает этот поток задач.

![Схема потока задач.](media/step-icons-example-task-flow.png "Схема потока задач")

### <a name="create-a-step-class-for-the-container-input-page"></a>Создание класса шага для страницы ввода контейнера

Страница ввода контейнера позволяет работнику сканировать или вводить идентификатор контейнера.

![Страница ввода контейнера.](media/step-icons-example-container-input.png "Страница ввода контейнера")

На странице ввода контейнера имя элемента управления для поля ввода будет `ContainerId`. Поскольку это имя элемента управления не отображается в [списке кодов шагов](#step-ids-classes), вы не найдете существующего шага, основанного на нем. Поэтому необходимо создать класс шага, представляющий этот шаг. Рассмотрим пример:

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

Идентификатор значка шага хранится в участнике класса `defaultStepIcon`, а заголовок шага сохраняется в участнике класса `defaultStepTitle`.

Чтобы назначить значок шага, установите `defaultStepIcon` на один из кодов значков, которые указаны в разделе [Доступные значки шагов](#step-icons) ранее в этой теме.

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>Использование стандартного или пользовательского значка и заголовка шага для ввода веса

Страница ввода веса позволяет сотруднику ввести вес.

![Страница ввода веса.](media/step-icons-example-weight-input.png "Страница ввода веса")

На странице ввода веса имя элемента управления поля ввода равно `Weight`, которое находится в [списке кодов шагов](#step-ids-classes). Таким образом, если значок и заголовок шага, заданные в классе `WHSMobileAppStepWeight`, являются приемлемыми для вас, вам не придется ничего изменять для этого шага.

Однако, если вы предпочитаете использовать для этого шага другие значок или заголовок, можно переопределить метод `stepId()` или метод `stepInfo()` в классе конструктора. У каждого потока задач имеется свой собственный конструктор информации о шаге.

#### <a name="override-the-stepid-method"></a>Переопределение метода stepId()

В следующем примере показан один из способов изменения класса конструктора путем переопределения метода `stepId()`.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

Затем создается класс шага для шага `NewWeight`. Код должен походить на код для примера `ContainerId`, приведенного ранее в этой теме.

#### <a name="override-the-stepinfo-method"></a>Переопределение метода stepInfo()

В следующем примере показан один из способов изменения класса конструктора путем переопределения метода `stepInfo()`.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

После этого создается объект `WHSMobileAppStepInfo` и устанавливается значок и/или заголовок непосредственно.

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Установка и подключение мобильного приложения "Управление складом"](install-configure-warehouse-management-app.md)
- [Параметры пользователя мобильного устройства](mobile-device-user-settings.md)
