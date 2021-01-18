---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 03eb85c423b06642a15db616b1ba1e0343c94963
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517525"
---
# <span data-ttu-id="145cb-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="145cb-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="145cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="145cb-102">SYNOPSIS</span></span>
<span data-ttu-id="145cb-103">Обновление автоматического ответа (действие правила оповещения).</span><span class="sxs-lookup"><span data-stu-id="145cb-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="145cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="145cb-104">SYNTAX</span></span>

### <span data-ttu-id="145cb-105">ActionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="145cb-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="145cb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="145cb-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="145cb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="145cb-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="145cb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="145cb-108">DESCRIPTION</span></span>
<span data-ttu-id="145cb-109">Для обновления закладки в указанной рабочей области обновляется **cmdlet Update-AzSentinelAlertRuleAction.**</span><span class="sxs-lookup"><span data-stu-id="145cb-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="145cb-110">Объект **AlertRuleAction** можно передать в качестве параметра или с помощью оператора конвейера. Кроме того, можно указать *параметры AlertRuleId* и *ActionId.*</span><span class="sxs-lookup"><span data-stu-id="145cb-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="145cb-111">Параметр Confirm  и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="145cb-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="145cb-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="145cb-112">EXAMPLES</span></span>

### <span data-ttu-id="145cb-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="145cb-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="145cb-114">Этот пример обновляет действие **AlertRuleAction,** заменяя существующее действие *новыми* свойствами.</span><span class="sxs-lookup"><span data-stu-id="145cb-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="145cb-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="145cb-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="145cb-116">В этом примере **обновление alertRuleAction с помощью** объекта InputObject, заменив существующее действие новыми свойствами. </span><span class="sxs-lookup"><span data-stu-id="145cb-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="145cb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="145cb-117">PARAMETERS</span></span>

### <span data-ttu-id="145cb-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="145cb-118">-ActionId</span></span>
<span data-ttu-id="145cb-119">ИД действия.</span><span class="sxs-lookup"><span data-stu-id="145cb-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145cb-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="145cb-120">-AlertRuleId</span></span>
<span data-ttu-id="145cb-121">ИД правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="145cb-121">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145cb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="145cb-122">-DefaultProfile</span></span>
<span data-ttu-id="145cb-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="145cb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="145cb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="145cb-124">-InputObject</span></span>
<span data-ttu-id="145cb-125">InputObject.</span><span class="sxs-lookup"><span data-stu-id="145cb-125">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="145cb-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="145cb-126">-LogicAppResourceId</span></span>
<span data-ttu-id="145cb-127">ИД ресурса приложения Action Logic.</span><span class="sxs-lookup"><span data-stu-id="145cb-127">Action Logic App Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145cb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="145cb-128">-ResourceGroupName</span></span>
<span data-ttu-id="145cb-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="145cb-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145cb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="145cb-130">-ResourceId</span></span>
<span data-ttu-id="145cb-131">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="145cb-131">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="145cb-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="145cb-132">-TriggerUri</span></span>
<span data-ttu-id="145cb-133">Uri триггера приложения "Логика действий".</span><span class="sxs-lookup"><span data-stu-id="145cb-133">Action Logic App Trigger Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145cb-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="145cb-134">-WorkspaceName</span></span>
<span data-ttu-id="145cb-135">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="145cb-135">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145cb-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="145cb-136">-Confirm</span></span>
<span data-ttu-id="145cb-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="145cb-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145cb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="145cb-138">-WhatIf</span></span>
<span data-ttu-id="145cb-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="145cb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="145cb-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="145cb-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="145cb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145cb-141">CommonParameters</span></span>
<span data-ttu-id="145cb-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="145cb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145cb-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="145cb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145cb-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="145cb-144">INPUTS</span></span>

### <span data-ttu-id="145cb-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="145cb-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="145cb-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="145cb-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="145cb-147">System.String</span><span class="sxs-lookup"><span data-stu-id="145cb-147">System.String</span></span>

## <span data-ttu-id="145cb-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="145cb-148">OUTPUTS</span></span>

### <span data-ttu-id="145cb-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="145cb-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="145cb-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="145cb-150">NOTES</span></span>

## <span data-ttu-id="145cb-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="145cb-151">RELATED LINKS</span></span>
