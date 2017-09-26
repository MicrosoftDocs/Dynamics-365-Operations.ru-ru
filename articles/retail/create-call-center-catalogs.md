---
title: "Создание каталога центра обработки вызовов"
description: "В этой статье содержится обзор процесса создания каталога для центра обработки вызовов."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 28aaa84c11a897b895b2a106ca5f0cd6168997b2
ms.contentlocale: ru-ru
ms.lasthandoff: 06/20/2017

---

# <a name="create-a-call-center-catalog"></a>Создание каталога центра обработки вызовов

[!include[banner](includes/banner.md)]


В этой статье содержится обзор процесса создания каталога для центра обработки вызовов. 

В центре обработки вызовов каталоги продуктов используются для определения продуктов, которые требуется предложить клиентам. В центрах обработки вызовов обычно используются печатные каталоги. Разработка и производство печатного каталога выполняются вне Microsoft Dynamics 365 for Retail. Однако вы можете создать и сохранить цифровую форму каталога, используя те же формы, что и при настройке интернет-каталогов розничной торговли. Перед созданием каталога необходимо настроить ассортименты продуктов и назначить ассортименты центру обработки вызовов. После этого следует добавить продукты в каталог, выбрав продукты из этих ассортиментов. После добавления продуктов в каталог и завершения составления каталога необходимо утвердить каталог для проверки данных. Затем следует отправить каталог на просмотр и утверждение. После утверждения каталога, он может быть опубликован. После создания каталога центра обработки вызовов можно сделать снимок данных каталога при публикации каталога. Благодаря этой функции снимка можно получить доступ к определенной версии каталога, даже если каталог изменяется и обновляется впоследствии. Кроме того, каталоги центра обработки вызовов можно настроить для включения следующих дополнительных возможностей.

-   **Коды источников** — коды, которые используются для отслеживания реакции клиентов на определенные рассылки каталогов.
-   **Бесплатные продукты** — продукты, включенные в заказ клиента без дополнительной платы. Эти продукты автоматически добавляются в заказ, когда код источника каталога вводится в заказ.
-   **Сценарии** — тексты, которые работник центра обработки вызовов предоставляет клиенту при создании заказа на продажу. Сценарии могут включать приветствия или предложения покупки.
-   **Номенклатура к расширению продаж или к перекрестным продажам** — номенклатуры, которые отображаются как предложение, когда к заказу добавляется определенный продукт.

Эти параметры должны быть настроены до утверждения и публикации каталога.

## <a name="prerequisites"></a>Необходимые условия
Сначала необходимо выполнить следующие задачи.

-   Настройка продуктов и ассортиментов продуктов.
-   Настройка розничных продуктов.
-   Настройка ассортимента.
-   Создание центра обработки вызовов.
-   Настройка центра обработки вызовов.
-   Добавление центра обработки вызовов в организационную иерархию.
-   Создание и изменение организационной иерархии.

## <a name="create-a-catalog"></a>Создание каталога
Сначала следует создать каталог, добавить продукты в каталог, а затем просмотреть и обновить атрибуты продуктов.

## <a name="validate-the-catalog"></a>Проверка каталога
После завершения настройки каталога необходимо проверить его. В ходе процесса проверки проверяется, что данные, необходимые для атрибутов канала и атрибутов продукта, полные и допустимые, и что каталог можно опубликовать.

## <a name="submit-the-catalog-for-review-and-approval"></a>Отправка каталога на проверку и утверждение
После проверки каталога можно отправить каталог для просмотра и утверждения. Каталог должны быть утвержден, прежде чем его можно опубликовать. Можно настроить workflow-процесс, чтобы каталоги утверждались автоматически или вручную.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>(Необязательно) Добавление кодов источников, бесплатных продуктов и сценариев
Вы можете также добавить следующие пункты в каталог центра обработки вызовов. Эти пункты являются необязательными.

-   **Коды источника** могут использоваться компаниями, которые производят печатные каталоги, для отслеживания реакции клиентов на определенные каталоги. Коды источника часто печатаются на обратной стороне каталога и вводятся в заказ на продажу, когда клиент совершает покупку. Чтобы добавить исходный код в каталог, необходимо сначала создать целевой рынок. Целевой рынок обычно сопоставляется собственному или арендованному списку рассылки.
-   **Бесплатные продукты** — это рекламные номенклатуры, которые бесплатно включаются в заказ клиента, если указана ссылка на каталог.
-   **Сценарии** можно использовать для руководства взаимодействием работника с клиентами в контексте каталога или продукта в каталоге.

## <a name="publish-the-catalog"></a>Публикация каталога
При публикации каталога для центра обработки вызовов следует указать сведения о продукте в каталоге. Публикация также показывает, что каталог готов для любых дополнительных действий, которые необходимо выполнить. Например, вы можете создать печатный каталог. Можно опубликовать каталоги вручную или использовать процесс пакетной обработки для публикации согласно графику. Прежде чем вы сможете опубликовать каталог, каталог необходимо проверить и утвердить. Для внесения изменений в каталог после его публикации можно отозвать каталог, а затем снова опубликовать его.



