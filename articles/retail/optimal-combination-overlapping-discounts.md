<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="optimal-combination-overlapping-discounts.md" target-language="ru-RU">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>optimal-combination-overlapping-discounts.e4f3cd.e327f652855f898e50f1dd853ae20f3a0ff41d9e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e327f652855f898e50f1dd853ae20f3a0ff41d9e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\optimal-combination-overlapping-discounts.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Определения оптимального сочетания пересекающихся скидок</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Если скидки пересекаются, необходимо определить сочетание пересекающихся скидок, которое будет давать самую низкую общую суммы проводки или самую большую общую скидку.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common 'Buy 1, get 1 X percent off' (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Когда сумма скидки варьируется в зависимости от цены приобретенных продуктов, как в обычной розничной скидке "купите 1, получите 1 со скидкой X процентов" (BOGO), этот процесс становится предметом комбинаторной задачи оптимизации.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Определения оптимального сочетания пересекающихся скидок</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Если скидки пересекаются, необходимо определить сочетание пересекающихся скидок, которое будет давать самую низкую общую суммы проводки или самую большую общую скидку.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common "Buy 1, get 1 X percent off" (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Когда сумма скидки варьируется в зависимости от цены приобретенных продуктов, как в обычной розничной скидке "купите 1, получите 1 со скидкой X процентов" (BOGO), этот процесс становится предметом комбинаторной задачи оптимизации.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This article applies to Microsoft Dynamics AX 2012 R3 with KB 3105973 (released November 2, 2015) or later, and to Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Эта статья относится к Microsoft Dynamics AX 2012 R3 с исправлением KB 3105973 (выпущено 2 ноября 2015 г.) или более поздней версии, а также к выпуску Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To determine the combination overlapping discounts to apply in a timely manner, we have introduced a method for applying overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Чтобы определить комбинацию пересекающихся скидок для своевременного применения был введен метод применения пересекающихся скидок.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>We call this new method <bpt id="p1">**</bpt>marginal value ranking<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Мы называем этот новый метод <bpt id="p1">**</bpt>ранжирование по маржинальным значениям<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Marginal value ranking is used when the time that is required in order to evaluate the possible combinations of overlapping discounts exceeds a threshold that is configurable on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ранжирование по маржинальным значениям используется, когда время, необходимое для оценки возможных сочетаний пересекающихся скидок превышает пороговое значение, которое можно настроить на странице <bpt id="p1">**</bpt>Параметры розничной торговли<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the marginal value ranking method, a value is calculated for each overlapping discount by using the discount's value on the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В методе ранжирования по маржинальным значениям значение рассчитывается для каждой пересекающейся скидки с помощью значения скидки на общих продуктов.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The overlapped discounts are then applied from the highest relative value to the lowest relative value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Пересекающиеся скидки затем применяются в порядке от самого высокого относительного значения до самого маленького относительного значения.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For details about the new method, see the "Marginal value" section, later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Дополнительные сведения об этом новом методе см. в разделе "Маржинальное значение" далее в этой статье.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Marginal value ranking isn't used when the discount amounts for a product aren't affected by another product in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ранжирование по маржинальным значениям не используется, когда на суммы скидок для продукта не влияет другой продукт в проводке.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For example, this method isn't used for two simple discounts, or for a simple discount and a single product quantity discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Например, этот метод не используется для двух простых скидок или для простой скидки и скидки за количество одного продукта.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Discount examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Примеры скидок</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can create an unlimited number of retail discounts on a common set of products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Можно создать неограниченное число розничных скидок для общего набора продуктов.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>However, because there is no limit, performance issues can occur when you try to calculate the discounts that should be used on the various products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Однако в связи с отсутствием ограничения могут возникать проблемы с производительностью при попытке расчета скидок, которые должны использоваться в различных продуктах.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The following examples illustrate this issue in more detail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Следующие примеры иллюстрируют эту проблему с большей степенью детализации.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In example 1, we start with two products and two overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В примере 1 мы запустим два продукта и две пересекающиеся скидки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Then, in example 2, we show how the issue evolves as more products are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Затем, в примере 2, мы покажем, как появляется проблема по мере добавления дополнительных продуктов.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Example 1: Two products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Пример 1. Два продукта и две скидки</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In this example, two products are required in order to qualify for each discount, and the discounts can't be combined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В этом примере два продукта необходимы для действия каждой скидки, и эти скидки не могут использоваться вместе.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The discounts in this example are <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Скидки в данном примере являются скидками <bpt id="p1">**</bpt>Лучшая цена<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Both products qualify for both discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Обе скидки распространяются на оба продукта.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Here are the two discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Здесь приведены две скидки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Example of two Best price discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Пример двух скидок "Лучшая цена"</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For any two products, the better of these two discounts depends on the prices of the two products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Для любых двух продуктов лучшая из этих двух скидок зависит от цен этих двух продуктов.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When the price of both products is equal or almost equal, discount 1 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Когда цены обоих продуктов равны или почти равны, лучше скидка 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>When the price of one product is significantly less than the price of the other product, discount 2 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Когда цена одного продукта существенно меньше цены другого продукта, лучше скидка 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Here is the mathematical rule for evaluating these two discounts against each other.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Вот математические правило для оценки этих двух скидок относительно друг друга.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Rule for evaluating the discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Правило оценки скидок</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>When the price of product 1 is equal to two-thirds of the price of product 2, the two discounts are equal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Обратите внимание, что когда цена продукта 1 составляет две трети от цены продукта 2, две скидки равны.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In this example, the effective discount percentage for discount 1 varies from a few percent (when the prices of the two products are far apart) to a maximum of 25 percent (when the two products have the same price).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В этом примере эффективный процент скидки для скидки 1 меняется от нескольких процентов (когда цены на два продукта сильно различаются) до максимального значения 25 процентов (когда два продукта имеют одинаковую цену).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The effective discount percentage for discount 2 is fixed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Эффективный процент скидки для скидки 2 является фиксированным.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>It's always 20 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Это всегда 20 процентов.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Because the effective discount percentage for discount 1 has a range that can be more than or less than discount 2, the best discount depends on the prices of the two products that must be discounted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Поскольку эффективный процент скидки для скидки 1 имеет диапазон, который может быть больше или меньше, чем скидка 2, лучшая скидка зависит от цен двух продуктов, для которых должна быть предоставлена скидка.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In this example, the calculation is completed quickly, because only two discounts are applied on only two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В этом примере расчет выполняется быстро, поскольку только две скидки применяются только к двум продуктам.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>There are only two possible combinations: one application of discount 1 or one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Существует только два возможных варианта: одно применение скидки 1 или одно применение скидки 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>There are no permutations to calculate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Не требуется рассчитывать никакие перестановки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The value of each discount is calculated by using both products, and the best discount is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Значение каждой скидки вычисляется с использованием обоих продуктов, и используется наибольшая скидка.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Example 2: Four products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Пример 2. Четыре продукта и две скидки</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Next, we will use four products and the same two discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Далее мы будет использовать четыре продуктов и эти же две скидки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>All four products qualify for both discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">На все четыре продукта распространяются обе скидки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>There are twelve possible combinations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Существует 12 возможных комбинаций.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In the end, two discounts will be applied to the transaction in one of three combinations: two applications of discount 1, two applications of discount 2, or one application of discount 1 and one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В итоге две скидки будут применяться к проводке в одной из трех комбинаций: два применения скидки 1, два применения скидки 2 или одно применение скидки 1 и одно применение скидки 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To illustrate the possible combinations, we will look at two different sets of four products that have different prices:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Чтобы проиллюстрировать возможных комбинаций, рассмотрим два разных набора четырех продуктов, имеющих разные цены:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>All four products have the same price, $15.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Все четыре товара имеют одинаковую цену $15,00.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In this case, the best discount combination is two applications of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В этом случае наилучшее сочетание скидок — два применения скидки 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Two products will be full price, and two will be 50 percent off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Два продукта по полной цене, и два продукта со скидкой 50 процентов.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The discounted total for the transaction is $45 (15 + 15 + 7.50 + 7.50), which is $15 (25 percent) off the undiscounted total of $60.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Итоговая сумма со скидкой для проводки составляет $45 (15 + 15 + 7,50 + 7,50), что на $15 (25 процентов) меньше общей суммы $60 без скидки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Discount 2 is only $12 (20 percent).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Скидка 2 составляет только $12 (20 процентов).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Two products are $20 each, one product is $15, and one product is $5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Два продукта по $20 каждый, один продукт за $15 и один продукт за $5.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In this case, the best discount combination is one application of discount 2 and one application of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В этом случае наилучшее сочетание скидок — одно применение скидки 2 и одно применение скидки 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The following tables illustrates the discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В следующей таблице показаны эти скидки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To read the tables, use one product from a row and one product from a column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Для использования таблиц следует взять один продукт в строке и один продукт в столбце.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For example, in the table for discount 1, when you combine the two $20 products, you get $10 off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Например, в таблице для скидки 1 для сочетания двух продуктов по $20 вы получаете скидку $10.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the table for discount 2, when you combine the $15 product and the $5 product, you get $4 off.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">В таблице для скидки 2 для сочетания продукта за $15 и продукта на $5 вы получаете скидку $4.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Example that uses four products for the same two discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Пример, в котором для одинаковых двух скидок используются четыре продукта</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>First, we find the largest discount that is available from any two products by using either discount.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Сначала мы найдем наибольшую скидку, которая доступна для любых двух продуктов с использованием любой из скидок.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The two tables show the discount amount for all combinations of the two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Эти две таблицы отображает сумму скидки для всех комбинаций двух продуктов.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The shaded portions of the tables represent either cases where a product is paired with itself, which we can't do, or a reverse pairing of two products that produces the same discount amount and can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Затененные части таблицы представляют либо случаи, когда продукт сопоставляется сам себе, что не допускается, или обратный порядок связывания двух продуктов, который дает такую же сумму скидки и может быть пропущен.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>By looking at the tables, you can see that discount 1 for the two $20 items is the largest discount that is available for either discount on all four products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Глядя на таблицы, можно определить, что скидка 1 для двух номенклатур по $20 является наибольшей скидкой, которая доступна для обоих скидок на всех четырех продуктах.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>(This discount is highlighted in green in the first table.) That leaves only the $15 product and the $5 product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Эта скидка выделена зеленым цветом в первой таблице.) Остаются еще продукт за $15 и продукт за $5.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>By looking at the two tables again, you can see that, for these two products, discount 1 gives a $2.50 discount, whereas discount 2 gives a $4 discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Снова проверив эти две таблицы, можно увидеть, что для этих двух продуктов скидка 1 составляет $2,50, в то время как скидка 2 составляет $4.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Therefore, we select discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Поэтому мы выбираем скидку 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The total discount is $14.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Итоговая скидка составляет $14.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>To make this discussion easier to visualize, here are two additional tables that show the effective discount percentage for all possible two-product combinations for both discount 1 and discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Для упрощения визуализации этого обсуждения приведем две дополнительные таблицы, которые показывают процент скидки для всех возможных комбинаций двух продуктов для обоих скидок 1 и 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Only half the list of combinations is included, because, for these two discounts, the order in which the two products are put into the discount doesn't matter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Только половина списка комбинаций включена, поскольку для этих двух скидок не имеет значения порядок, в котором два продукта помещаются в скидку.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The highest effective discount (25 percent) is highlighted in green, and the lowest effective discount (10 percent) is highlighted in red.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Самая высокая эффективная скидка (25 процентов) выделена зеленым цветом, а самая низкая эффективная скидка (10 процентов) выделена красным цветом.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Effective discount percentage for all two-product combinations for both discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Действительный процент скидки для всех комбинаций двух продуктов для обеих скидок</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>When prices vary, and two or more discount compete, the only way to guarantee the best combination of discounts is to evaluate both discounts and compare them.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Когда цены различаются и возможно применение двух разных взаимоисключающих скидок, единственным способом обеспечения лучшего сочетания скидок является расчет обеих скидок и сравнение их.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Total possible combinations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Общее число возможных комбинаций</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section continues the example from the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В этом разделе продолжается пример из предыдущего раздела.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>We will add more products and another discount, and see how many combinations must be calculated and compared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Мы добавим еще продукты и другие скидки и посмотрим, сколько комбинаций необходимо рассчитать и сравнить.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The following table shows the number of possible discount combinations as the product quantity increases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В следующей таблице показано число возможных комбинаций скидок при увеличении количества продуктов.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The table shows what happens both when there are two overlapping discounts, as in the previous example, and when there are three overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В таблице показано, что происходит при наличии двух пересекающихся скидок, как в предыдущем примере, и при наличии трех пересекающихся скидок.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The number of possible discount combinations that must be evaluated soon exceeds what even a fast computer can calculate and compare quickly enough to be acceptable for retail transactions.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Количество возможных комбинациях скидок, которые необходимо оценить, очень быстро превышает значение, которое даже мощный компьютер может рассчитать и сравнить достаточно быстро, чтобы это было приемлемо для проводок в розничной торговле.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Number of possible discount combinations as the product quantity increases</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Число возможных комбинаций скидок при увеличении количества продуктов</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>When even larger quantities or more overlapping discounts are applied, the total number of possible discount combinations quickly goes into the millions, and the time that is required in order to evaluate and select the best possible combination quickly becomes noticeable.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Если продуктов еще большее или применяется еще больше пересекающихся скидок, общее число возможных комбинаций скидок быстро начинает превышать миллионы, и время, необходимое для расчета и выбора наилучшего сочетания, быстро становится заметным.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Some optimizations have been done in the retail price engine to reduce the total number of combinations that must be evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Некоторые оптимизации были выполнены в механизме розничной цены, чтобы сократить общее количество комбинаций, которые необходимо оценить.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>However, because the number overlapping discounts and the quantities in a transaction aren't limited, a large number of combinations will always have to be evaluated whenever there are overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Однако поскольку количество пересекающихся скидок и количества в проводках не ограничены, большое количество сочетаний всегда должно будет вычисляться всякий раз, когда имеются пересекающиеся скидки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This issue is the issue that the marginal value ranking method addresses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Эту проблему решает метод ранжирования по маржинальным значениям.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Marginal value method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Метод маржинальных значений</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>To resolve the issue of an exponentially increasing number of combinations that must be evaluated, an optimization exists that calculates the value per shared product of each discount on the set of products that two or more discounts can be applied to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Для решения проблемы экспоненциального роста числа комбинаций, которые необходимо оценить, существует оптимизация, которая вычисляет значение для каждого общего продукта каждой скидки на наборе продуктов, к которому могут быть применены две и более скидок.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>We refer to this value as the <bpt id="p1">**</bpt>marginal value<ept id="p1">**</ept> of the discount for the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Мы называем это значение <bpt id="p1">**</bpt>маржинальным значением<ept id="p1">**</ept> скидки для общих продуктов.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The marginal value is the average per product increase in the total discount amount when the shared products are included in each discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Маржинальное значение является средним по увеличению продукта в сумме общей скидки, когда общие продукты включены в каждую скидку.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The marginal value is calculated by taking the total discount amount (DTotal), subtracting the discount amount without the shared products (DMinus<ph id="ph1">\\</ph> Shared), and dividing that difference by the number of shared products (ProductsShared).</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Маржинальное значение вычисляется путем определения общей суммы скидки (DTotal), вычитания суммы скидки без общих продуктов (DMinus<ph id="ph1">\\</ph> Shared) и деления этой разницы на количество общих продуктов (ProductsShared).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Formula for calculating marginal value</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Формула для расчета маржинального значения</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>After the marginal value of each discount on a shared set of products is calculated, the discounts are applied to the shared products in order, exhaustively, from highest marginal value to lowest marginal value.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">После расчета маржинального значения каждого скидки на общем наборе продуктов скидки применяются к общим продуктом по порядку, строго, от максимального маржинального значения до минимального маржинального значения.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For this method, all remaining discount possibilities aren't compared every time after a single instance of a discount is applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">В этом методе все остальные варианты скидки не сравниваются каждый раз после применения одного экземпляра скидки.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Instead, the overlapping discounts are compared one time and then applied in order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Вместо этого пересекающиеся скидки сравниваются один раз и затем применяются по порядку.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>No additional comparisons are done.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Дополнительные сравнения не выполняются.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>You can configure the threshold to switch to the marginal value method on the <bpt id="p1">**</bpt>Discount<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Пороговое значение для переключения на метод маржинальных значений можно настроить на вкладке <bpt id="p1">**</bpt>Скидка<ept id="p1">**</ept> на странице <bpt id="p2">**</bpt>Параметры розничной торговли<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The acceptable time to calculate the total discount varies across retail industries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Допустимое время расчета общей скидки зависит от отрасли розничной торговли.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>However, this time generally falls in the range of tens of milliseconds to one second.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Однако обычно это время лежит в диапазоне от десятков миллисекунд до одной секунды.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>