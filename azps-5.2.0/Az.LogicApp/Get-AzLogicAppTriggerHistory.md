---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: d20d6ba980b424109e33fd4380eec9be4f7728ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393764"
---
# <span data-ttu-id="c5bc9-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="c5bc9-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="c5bc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bc9-103">Возвращает историю триггеров в приложении логики.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="c5bc9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5bc9-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5bc9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5bc9-105">DESCRIPTION</span></span>
<span data-ttu-id="c5bc9-106">**Cmdlet Get-AzLogicAppTriggerHistory** получает историю триггеров в приложении логики в функции "Приложения логики".</span><span class="sxs-lookup"><span data-stu-id="c5bc9-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="c5bc9-107">Этот cmdlet возвращает объект **WorkflowTriggerHistory.**</span><span class="sxs-lookup"><span data-stu-id="c5bc9-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="c5bc9-108">Укажите приложение логики, группу ресурсов и триггер.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="c5bc9-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c5bc9-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c5bc9-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c5bc9-112">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c5bc9-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5bc9-113">EXAMPLES</span></span>

### <span data-ttu-id="c5bc9-114">Пример 1. Получить историю триггеров приложения логики</span><span class="sxs-lookup"><span data-stu-id="c5bc9-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A15%3A16Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="c5bc9-115">Эта команда получает определенный историю триггера приложения логики для триггера в приложении логики LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="c5bc9-116">Пример 2. Получить триггеры приложения логики</span><span class="sxs-lookup"><span data-stu-id="c5bc9-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
Code        : BadRequest
EndTime     : 1/13/2016 2:43:33 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/CAB46_60e2ad0f0e1947e8b5798716914c5d
              b6_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489106716457817
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:43:33 PM
Status      : Failed
TrackingId  : c91a63f1-48b4-4eae-91eb-8f6dbfa9fe06
Type        : Microsoft.Logic/workflows/triggers/histories

Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="c5bc9-117">Эта команда возвращает истории рабочего процесса для триггера в приложении логики LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="c5bc9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5bc9-118">PARAMETERS</span></span>

### <span data-ttu-id="c5bc9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5bc9-119">-DefaultProfile</span></span>
<span data-ttu-id="c5bc9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c5bc9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc9-121">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="c5bc9-121">-HistoryName</span></span>
<span data-ttu-id="c5bc9-122">Определяет имя истории, которая возвращается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-122">Specifies the name of the history that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c5bc9-123">-Name</span></span>
<span data-ttu-id="c5bc9-124">Имя приложения логики, для которого этот cmdlet получает историю триггеров.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5bc9-125">-ResourceGroupName</span></span>
<span data-ttu-id="c5bc9-126">Имя группы ресурсов, в которой этот cmdlet получает историю.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc9-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="c5bc9-127">-TriggerName</span></span>
<span data-ttu-id="c5bc9-128">Указывает имя триггера, для которого этот cmdlet получает историю.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bc9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bc9-129">CommonParameters</span></span>
<span data-ttu-id="c5bc9-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5bc9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bc9-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5bc9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bc9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5bc9-132">INPUTS</span></span>

### <span data-ttu-id="c5bc9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c5bc9-133">System.String</span></span>

## <span data-ttu-id="c5bc9-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5bc9-134">OUTPUTS</span></span>

### <span data-ttu-id="c5bc9-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="c5bc9-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="c5bc9-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5bc9-136">NOTES</span></span>

## <span data-ttu-id="c5bc9-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5bc9-137">RELATED LINKS</span></span>

[<span data-ttu-id="c5bc9-138">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="c5bc9-138">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="c5bc9-139">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="c5bc9-139">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="c5bc9-140">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c5bc9-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


