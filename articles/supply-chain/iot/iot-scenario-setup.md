---
title: Настройка сценария для бизнес-аналитики Интернета вещей
description: В этом разделе описывается, как настроить сценарий в Supply Chain Management для бизнес-аналитики Интернета вещей.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386554"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="dc9d3-103">Настройка сценария для бизнес-аналитики Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="dc9d3-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dc9d3-104">В этом разделе описывается, как настроить сценарий в Supply Chain Management для бизнес-аналитики Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="dc9d3-105">Прежде чем настраивать сценарии, необходимо [настроить LCS](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="dc9d3-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="dc9d3-106">В этом разделе можно настроить сценарий **простой оборудования**, чтобы создать уведомление в Supply Chain Management при отключении компьютера.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="dc9d3-107">Настройка сценария **простой оборудования** в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dc9d3-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="dc9d3-108">В сценарии **простой оборудования** отображается сигнал частичного выхода для порога оповещения компьютера.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="dc9d3-109">Наблюдение за станком осуществляется только в том случае, если компьютер выбрана для сценария и настроен на выполнение в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="dc9d3-110">Если время, прошедшее с момента получения сигнала о частичном выходе компьютера, превышает порог оповещения, то уведомление об **отключении компьютера** запускается.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="dc9d3-111">Если компьютер все еще работает, при получении следующего сигнала **PartOut** запускается уведомление о **включении компьютера**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="dc9d3-112">Если компьютер остановлен в течение 30 минут, будет запущено новое уведомление об **отключении компьютера**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="dc9d3-113">В сценарии **простой оборудования** имеются следующие зависимости:</span><span class="sxs-lookup"><span data-stu-id="dc9d3-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="dc9d3-114">Для запуска оповещения производственный заказ должен быть запущен на сопоставленном станке.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="dc9d3-115">Сигнал, представляющий сигнал частичного выхода сопоставленного компьютера, должен быть отправлен в узел Интернета вещей с уникальным именем свойства.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="dc9d3-116">В сообщении узла Интернета вещей должно присутствовать свойство метки времени для миллисекунд UNIX.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="dc9d3-117">Выполните следующие действия, чтобы настроить сценарий:</span><span class="sxs-lookup"><span data-stu-id="dc9d3-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="dc9d3-118">Войдите в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="dc9d3-119">Включите флаг функции аналитики Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="dc9d3-120">Дополнительные сведения см. в разделе [Обзор управления функциями](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dc9d3-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="dc9d3-121">Настройка метрик.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-121">Configure the metrics.</span></span> <span data-ttu-id="dc9d3-122">Дополнительные сведения см. в [Как настроить метрики](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="dc9d3-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="dc9d3-123">Перейдите в **Управление производством**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="dc9d3-124">Перейдите в раздел **Настройка \> аналитика Интернета вещей \> управление сценариями**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="dc9d3-125">Щелкните **настроить** на плитке **простой оборудования**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="dc9d3-126">Мастер настройки запускается со страницы **определение схемы датчика оборудования**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="dc9d3-127">Целью этого является настройка схемы в Supply Chain Management так, чтобы она соответствовала формату JSON сообщений Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="dc9d3-128">Можно определить несколько схем сообщений.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="dc9d3-129">Дополнительные сведения см. в разделе [форматы схем сообщений для узла Интернета вещей](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="dc9d3-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="dc9d3-130">В данном примере полезная нагрузка сообщения содержит пакет сообщений с данным форматом:</span><span class="sxs-lookup"><span data-stu-id="dc9d3-130">In this example, the message payload contains a batch of messages with this format:</span></span>

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. <span data-ttu-id="dc9d3-131">Добавление строки в таблицу.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="dc9d3-132">Установите **Имя схемы** на **Код**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="dc9d3-133">Установите **Имя схемы** на **/полезная нагрузка[\*]/код**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="dc9d3-134">Установите **описание** на **Код сообщения**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="dc9d3-135">Добавление строки в таблицу.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="dc9d3-136">Установите **Имя схемы** на **Метка времени**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="dc9d3-137">Установите **Имя схемы** на **/полезная нагрузка[\*]/метка времени**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="dc9d3-138">Установите **описание** на **Метка времени сообщения**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="dc9d3-139">Добавление строки в таблицу.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="dc9d3-140">Установите **Имя схемы** на **Значение**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="dc9d3-141">Установите **Имя схемы** на **/полезная нагрузка[\*]/значение**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="dc9d3-142">Установите **описание** на **Значение сообщения**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="dc9d3-143">Нет необходимости определять все свойства в сообщении, а не только те, которые необходимы.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="dc9d3-144">В этом примере не была создана строка для **корневой метки времени**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="dc9d3-145">Путь для **корневой метки времени** должен быть **/метка времени**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="dc9d3-146">Нажмите кнопку **Далее**, чтобы перейти на страницу **Сопоставление схемы датчика оборудования**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="dc9d3-147">В строке **кода ресурса оборудования** задайте **имя схемы** значение **Код**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="dc9d3-148">В раскрывающейся таблице отображаются допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="dc9d3-149">В строке для **времени UTC** задайте для **имени схемы** значение **Метка времени**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="dc9d3-150">В раскрывающейся таблице отображаются допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="dc9d3-151">В строке для **сигнал произведенной части** задайте **имя схемы** значение **Значение**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="dc9d3-152">В раскрывающейся таблице отображаются допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="dc9d3-153">Щелкните **Далее**, чтобы получить страницу **Конфигурация кода ресурса оборудования**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="dc9d3-154">На этом шаге значения сообщения узла Интернета вещей сопоставляются с ресурсами Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="dc9d3-155">В таблице **значения данных сигнала** добавьте новую строку и введите **IoTInt.Machine1225.PartOut** в столбце **значение**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="dc9d3-156">Значение **IoTInt.Machine1225.PartOut** поступает из свойства **код** JSON в сообщении узла Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="dc9d3-157">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-157">Click **Save**.</span></span>
    3. <span data-ttu-id="dc9d3-158">В таблице **сопоставление бизнес-записей** щелкните **создать**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="dc9d3-159">Значение по умолчанию для **типа бизнес-записи** заполняется автоматически, и его не нужно менять.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="dc9d3-160">В столбце **Бизнес-запись** выберите ресурс компьютера Supple Chain Management, с которого отсылается значение этого сигнала.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="dc9d3-161">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-161">Click **Save**.</span></span>
    6. <span data-ttu-id="dc9d3-162">Повторите эти шаги, добавляя сопоставление новых бизнес-записей для **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="dc9d3-163">Можно сопоставить несколько значений данных сигналов одной записи в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="dc9d3-164">Используйте столбец **Выбрано** для выбора компьютеров, которые необходимо обработать.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="dc9d3-165">Нет необходимости определять все значения сигнала, и вам не придется выбирать все компьютеры.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="dc9d3-166">Нажмите кнопку **Далее**, чтобы перейти на страницу **Конфигурация сигнала произведенных частей**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="dc9d3-167">В таблице **значения данных сигнала** добавьте строку и установите **значение** в **Истина**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="dc9d3-168">Значение **Истина** поступает из свойства **значение** JSON в сообщении узла Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="dc9d3-169">Можно добавить столько значений, сколько необходимо для сценария.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="dc9d3-170">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-170">Click **Save**.</span></span>
20. <span data-ttu-id="dc9d3-171">Нажмите кнопку **Далее**, чтобы перейти на страницу **Порог простоя оборудования**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="dc9d3-172">В списке приведены компьютеры, ранее сопоставленные со значениями сигналов.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="dc9d3-173">На этом шаге определяется пороговое значение, чтобы определить, отключен ли компьютер.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="dc9d3-174">Например, если установить пороговое значение 10, Supply Chain Management создает уведомление, если в течение 10 минут не поступило сообщение о выходе части с компьютера.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="dc9d3-175">Щелкните **Далее**, чтобы перейти к странице **Включить сценарий**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="dc9d3-176">Чтобы включить сценарий, переключите слайдер.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="dc9d3-177">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-177">Click **Finish**.</span></span>

<span data-ttu-id="dc9d3-178">Настройка сценария завершена.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-178">The scenario setup is complete.</span></span> <span data-ttu-id="dc9d3-179">Аналитика Интернета вещей автоматически начнет обрабатывать сообщения узла Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="dc9d3-180">Настройка сценария **качество продукта** в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dc9d3-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="dc9d3-181">Сценарий **качество продукта** создает уведомление, если атрибут номенклатуры выходит за пределы указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="dc9d3-182">Например, с помощью датчика можно отсылать вес каждой номенклатуры в узел Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="dc9d3-183">В Supply Chain Management будет создано уведомление, если номенклатура слишком большая или слишком маленькая.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="dc9d3-184">Сценарий имеет следующие зависимости:</span><span class="sxs-lookup"><span data-stu-id="dc9d3-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="dc9d3-185">Производственный заказ должен выполняться на сопоставленном компьютере и создавать продукт с сопоставленным атрибутом партии для срабатывания оповещения.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="dc9d3-186">Сигнал, представляющий атрибут партии, должен быть отправлен в узел Интернета вещей с уникальным именем свойства.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="dc9d3-187">В сообщении узла Интернета вещей должно присутствовать свойство метки времени для миллисекунд UNIX.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="dc9d3-188">Настройка сценария **задержки производства** в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dc9d3-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="dc9d3-189">Сценарий **задержки производства** создает уведомление, если пропускная способность производства падает ниже порогового значения.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="dc9d3-190">В этом случае сигнал **PartOut** для каждой произведенной номенклатуры направляется в узел Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="dc9d3-191">В Supply Chain Management задержка заказа рассчитывается на основе времени, в течение которого запланировано выполнение производственного заказа, сколько номенклатур должно быть произведено, как долго выполняется задание и сколько сигналов **PartOut** поступает.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="dc9d3-192">Уведомление о задержке будет создано, если число сигналов **PartOut** для задания оказывается ниже порогового значения ожидаемого значения.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="dc9d3-193">Сценарий имеет следующие зависимости:</span><span class="sxs-lookup"><span data-stu-id="dc9d3-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="dc9d3-194">Для запуска оповещения производственный заказ должен быть запущен на сопоставленном станке.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="dc9d3-195">Сигнал, представляющий сигнал частичного выхода сопоставленного компьютера, должен быть отправлен в узел Интернета вещей с уникальным именем свойства.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="dc9d3-196">В сообщении узла Интернета вещей должно присутствовать свойство метки времени для миллисекунд UNIX.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="dc9d3-197">Как отключить сценарий</span><span class="sxs-lookup"><span data-stu-id="dc9d3-197">How to disable a scenario</span></span>

<span data-ttu-id="dc9d3-198">Для отключения сценария выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="dc9d3-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="dc9d3-199">В Supply Chain Management перейдите к **Управление производством \> Настройка \> аналитика Интернета вещей \> Управление сценарием**.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="dc9d3-200">Щелкните **Настройка** в сценарии.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="dc9d3-201">Щелкните **Далее**, чтобы перейти к последней вкладке мастера.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="dc9d3-202">Чтобы отключить сценарий, переключите слайдер.</span><span class="sxs-lookup"><span data-stu-id="dc9d3-202">Toggle the slider to disable the scenario.</span></span>
