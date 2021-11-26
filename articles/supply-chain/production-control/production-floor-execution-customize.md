---
title: Настройка интерфейса выполнения производственного цеха
description: В этой теме объясняется, как расширить текущие формы или создать новые формы и кнопки для интерфейса выполнения производственного цеха.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 414fe5d6e16ad125bc2b9bb7ed427e5db5180ec9
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790990"
---
# <a name="customize-the-production-floor-execution-interface"></a>Настройка интерфейса выполнения производственного цеха

[!include [banner](../includes/banner.md)]

Разработчики могут расширить текущие формы или создать собственные формы и кнопки для интерфейса выполнения производственного цеха. После добавления кода для этих новых элементов администраторы или руководители цеха могут легко добавлять их в интерфейс с помощью стандартных средств управления конфигурацией.

Например, ниже приведены некоторые возможные решения, если в главной форме требуются новые столбцы:

- Расширьте форму `JmgProductionFloorExecutionMainGrid` и добавьте нужные поля.
- Создайте новую форму и добавьте ее как новое главное представление (вкладка).

## <a name="add-a-new-button-action"></a>Добавление новой кнопки (действие)

Чтобы добавить новую кнопку (действие), выполните следующие шаги, чтобы создать класс, реализующий настраиваемое действие.

1. Создайте новый класс с именем `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, где:

    - `<ExtensionPrefix>` уникально идентифицирует ваше решение, обычно с помощью названия компании.
    - `<ActionName>` — это уникальное имя для класса. Обычно оно идентифицирует вид действия.

1. Новый класс должен расширять класс `JmgProductionFloorExecutionAction`.
1. Переопределите все необходимые методы.

В качестве примеров рассмотрим код для следующих классов:

- `JmgProductionFloorExecutionBreakAction`— класс для простого действия, которое не требует каких-либо записей.
- `JmgProductionFloorExecutionReportFeedbackAction`— класс, обеспечивающий более сложную функциональность.

После завершения новая кнопка (действие) будет автоматически перечислена на странице **Разработка вкладок** в Microsoft Dynamics 365 Supply Chain Management. Там вы (либо администратор или руководитель цеха) можете легко добавить ее к основной или дополнительной панели инструментов, так же как вы можете добавлять стандартные кнопки. Инструкции см. в разделе [Разработка интерфейса выполнения производственного цеха](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Добавление нового основного представления

1. Создайте новую форму, в которой имеются нужные элементы и функции. Обратите внимание, что эта форма является новой формой, а не расширением. Назовите форму `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, где:

    - `<ExtensionPrefix>` уникально идентифицирует ваше решение, обычно с помощью названия компании.
    - `<FormName>` — это уникальное имя для формы.

1. Создайте пункт меню с названием `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Создайте расширение с именем `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, где метод `getMainMenuItemsList` расширяется путем добавления нового пункта меню в список. Следующий код показывает пример.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionForm))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

После завершения новое главное представление будет автоматически перечислено в поле со списком **Главное представление** на странице **Разработка вкладок** в Supply Chain Management. Там вы (либо администратор или руководитель цеха) можете легко его на новые или существующие вкладки, так же как вы можете добавлять стандартные главные представления. Инструкции см. в разделе [Разработка интерфейса выполнения производственного цеха](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Добавление представления сведений

1. Создайте новую форму, в которой имеются нужные элементы и функции. Обратите внимание, что эта форма новая, а не расширение. Назовите форму `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, где: 

    - `<ExtensionPrefix>` уникально идентифицирует ваше решение, обычно с помощью названия компании.
    - `<FormName>` — это уникальное имя для формы.

1. Создайте пункт меню с названием `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Создайте расширение с именем `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, где метод `getDetailsMenuItemList` расширяется путем добавления нового пункта меню в список.

После завершения новое представление сведений будет автоматически перечислено в поле со списком **Представление сведений** на странице **Разработка вкладок** в Supply Chain Management. Там вы (либо администратор или руководитель цеха) можете легко его на новые или существующие вкладки, так же как вы можете добавлять стандартные представления сведений. Инструкции см. в разделе [Разработка интерфейса выполнения производственного цеха](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Добавление цифровой клавиатуры в форму или диалоговое окно

В следующем примере показано, как добавить цифровую клавиатуру в форму.

1. Число контроллеров цифровой клавиатуры, содержащихся в каждой форме, должно равняться числу цифровых клавиатур в этой форме.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Настройте поведение каждого контроллера цифровой клавиатуры и соедините каждый из контроллеров цифровой клавиатуры частью формы цифровой клавиатуры.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Использование цифровой панели в качестве всплывающего диалогового окна

В следующем примере показан один из способов настройки контроллера цифровой клавиатуры для всплывающего диалогового окна.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

В следующем примере показан один из способов вызова всплывающего диалогового окна цифровой клавиатуры.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Стиль интерфейса выполнения производственного цеха](production-floor-execution-styles.md)
- [Разработка интерфейса выполнения производственного цеха](production-floor-execution-tabs.md)
