---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: 7c0d34ad56021e2fb4f74aef1bed41ca38c918c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008883"
---
# <span data-ttu-id="b0b23-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="b0b23-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="b0b23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b23-102">SYNOPSIS</span></span>

<span data-ttu-id="b0b23-103">Возвращает историю триггеров в приложении логики.</span><span class="sxs-lookup"><span data-stu-id="b0b23-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="b0b23-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0b23-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0b23-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0b23-105">DESCRIPTION</span></span>

<span data-ttu-id="b0b23-106">**Cmdlet Get-AzLogicAppTriggerHistory** получает историю триггеров в приложении логики в функции "Приложения логики".</span><span class="sxs-lookup"><span data-stu-id="b0b23-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="b0b23-107">Этот cmdlet возвращает объект **WorkflowTriggerHistory.**</span><span class="sxs-lookup"><span data-stu-id="b0b23-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="b0b23-108">Укажите приложение логики, группу ресурсов и триггер.</span><span class="sxs-lookup"><span data-stu-id="b0b23-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="b0b23-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="b0b23-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b0b23-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="b0b23-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b0b23-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="b0b23-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b0b23-112">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="b0b23-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b0b23-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0b23-113">EXAMPLES</span></span>

### <span data-ttu-id="b0b23-114">Пример 1. Получить историю триггеров приложения логики</span><span class="sxs-lookup"><span data-stu-id="b0b23-114">Example 1: Get a trigger history of a logic app</span></span>

```powershell
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

<span data-ttu-id="b0b23-115">Эта команда получает определенный историю триггера приложения логики для триггера в приложении логики LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="b0b23-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="b0b23-116">Пример 2. Получить триггеры приложения логики</span><span class="sxs-lookup"><span data-stu-id="b0b23-116">Example 2: Get trigger histories of a logic app</span></span>

```powershell
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

<span data-ttu-id="b0b23-117">Эта команда возвращает истории рабочего процесса для триггера в приложении логики LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="b0b23-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

### <span data-ttu-id="b0b23-118">Пример 3. Получить весь историю триггера приложения логики</span><span class="sxs-lookup"><span data-stu-id="b0b23-118">Example 3: Get entire trigger history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink
```

<span data-ttu-id="b0b23-119">Эта команда получает весь историю триггера рабочего процесса для триггера в приложении логики LogicApp08, следуя команде NextPageLink.</span><span class="sxs-lookup"><span data-stu-id="b0b23-119">This command gets the entire workflow trigger history for a trigger in the logic app named LogicApp08 by following the NextPageLink.</span></span>

### <span data-ttu-id="b0b23-120">Пример 4</span><span class="sxs-lookup"><span data-stu-id="b0b23-120">Example 4</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="b0b23-121">Эта команда получает первые две страницы истории триггера рабочего процесса для триггера в приложении логики LogicApp09, следуя следующей команде NextPageLink и ограничив размер результатов двумя страницами.</span><span class="sxs-lookup"><span data-stu-id="b0b23-121">This command gets the first two pages of workflow trigger history for a trigger in the logic app named LogicApp09 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="b0b23-122">Каждая страница содержит 30 результатов.</span><span class="sxs-lookup"><span data-stu-id="b0b23-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="b0b23-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0b23-123">PARAMETERS</span></span>

### <span data-ttu-id="b0b23-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b23-124">-DefaultProfile</span></span>

<span data-ttu-id="b0b23-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b0b23-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0b23-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="b0b23-126">-FollowNextPageLink</span></span>

<span data-ttu-id="b0b23-127">Указывает на то, что для cmdlet должны следовать ссылки на следующую страницу.</span><span class="sxs-lookup"><span data-stu-id="b0b23-127">Indicates the cmdlet should follow next page links.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b23-128">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="b0b23-128">-HistoryName</span></span>

<span data-ttu-id="b0b23-129">Определяет имя истории, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0b23-129">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b0b23-130">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="b0b23-130">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="b0b23-131">Количество ссылок на следующую страницу, если используется FollowNextPageLink.</span><span class="sxs-lookup"><span data-stu-id="b0b23-131">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ML

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b23-132">-Name</span><span class="sxs-lookup"><span data-stu-id="b0b23-132">-Name</span></span>

<span data-ttu-id="b0b23-133">Имя приложения логики, для которого этот cmdlet получает историю триггеров.</span><span class="sxs-lookup"><span data-stu-id="b0b23-133">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="b0b23-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b23-134">-ResourceGroupName</span></span>

<span data-ttu-id="b0b23-135">Имя группы ресурсов, в которой этот cmdlet получает историю.</span><span class="sxs-lookup"><span data-stu-id="b0b23-135">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="b0b23-136">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="b0b23-136">-TriggerName</span></span>

<span data-ttu-id="b0b23-137">Указывает имя триггера, для которого этот cmdlet получает историю.</span><span class="sxs-lookup"><span data-stu-id="b0b23-137">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="b0b23-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b23-138">CommonParameters</span></span>

<span data-ttu-id="b0b23-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b23-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b23-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0b23-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b23-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0b23-141">INPUTS</span></span>

### <span data-ttu-id="b0b23-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b0b23-142">System.String</span></span>

## <span data-ttu-id="b0b23-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0b23-143">OUTPUTS</span></span>

### <span data-ttu-id="b0b23-144">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="b0b23-144">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="b0b23-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0b23-145">NOTES</span></span>

## <span data-ttu-id="b0b23-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0b23-146">RELATED LINKS</span></span>

[<span data-ttu-id="b0b23-147">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="b0b23-147">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="b0b23-148">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="b0b23-148">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="b0b23-149">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b0b23-149">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)
