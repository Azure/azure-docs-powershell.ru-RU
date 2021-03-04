---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 3feb6a9cfa06e06a4759c34e3c0b2cd624559d2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955651"
---
# <span data-ttu-id="e07a8-101">Update-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="e07a8-101">Update-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="e07a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e07a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e07a8-103">Обновление автоматического ответа (действие правила оповещения).</span><span class="sxs-lookup"><span data-stu-id="e07a8-103">Update an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="e07a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e07a8-104">SYNTAX</span></span>

### <span data-ttu-id="e07a8-105">ActionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e07a8-105">ActionId (Default)</span></span>
```
Update-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07a8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e07a8-106">InputObject</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String>
 -InputObject <PSSentinelActionResponse> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e07a8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e07a8-107">ResourceId</span></span>
```
Update-AzSentinelAlertRuleAction -LogicAppResourceId <String> -TriggerUri <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e07a8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e07a8-108">DESCRIPTION</span></span>
<span data-ttu-id="e07a8-109">Для обновления закладки в указанной рабочей области будет обновлена **cmdlet Update-AzSentinelAlertRuleAction.**</span><span class="sxs-lookup"><span data-stu-id="e07a8-109">The **Update-AzSentinelAlertRuleAction** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="e07a8-110">Объект **AlertRuleAction** можно передать в качестве параметра или с помощью оператора конвейера. Кроме того, можно указать *параметры AlertRuleId* и *ActionId.*</span><span class="sxs-lookup"><span data-stu-id="e07a8-110">You can pass an **AlertRuleAction** object as a parameter or by using the pipeline operator, or alternatively you can specify the *AlertRuleId* and *ActionId* parameters.</span></span>
<span data-ttu-id="e07a8-111">С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e07a8-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="e07a8-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e07a8-112">EXAMPLES</span></span>

### <span data-ttu-id="e07a8-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e07a8-113">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="e07a8-114">Этот пример обновляет действие **AlertRuleAction,** заменяя существующее действие *новыми* свойствами.</span><span class="sxs-lookup"><span data-stu-id="e07a8-114">This example updates an **AlertRuleAction** replacing an existing *Action* with new properties.</span></span>

### <span data-ttu-id="e07a8-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e07a8-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
PS C:\> Update-AzSentinelAlertRuleAction -InputObject $AlertRuleAction -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="e07a8-116">В этом примере **оповещениеRuleAction** обновляется с помощью объекта InputObject, заменяя существующее действие *новыми* свойствами.</span><span class="sxs-lookup"><span data-stu-id="e07a8-116">This example updates an **AlertRuleAction** using an InputObject replacing an existing *Action* with new properties.</span></span>

## <span data-ttu-id="e07a8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e07a8-117">PARAMETERS</span></span>

### <span data-ttu-id="e07a8-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="e07a8-118">-ActionId</span></span>
<span data-ttu-id="e07a8-119">ИД действия.</span><span class="sxs-lookup"><span data-stu-id="e07a8-119">Action Id.</span></span>

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

### <span data-ttu-id="e07a8-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="e07a8-120">-AlertRuleId</span></span>
<span data-ttu-id="e07a8-121">ИД правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="e07a8-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="e07a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07a8-122">-DefaultProfile</span></span>
<span data-ttu-id="e07a8-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e07a8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e07a8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e07a8-124">-InputObject</span></span>
<span data-ttu-id="e07a8-125">InputObject.</span><span class="sxs-lookup"><span data-stu-id="e07a8-125">InputObject.</span></span>

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

### <span data-ttu-id="e07a8-126">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="e07a8-126">-LogicAppResourceId</span></span>
<span data-ttu-id="e07a8-127">ИД ресурса приложения "Логика действий".</span><span class="sxs-lookup"><span data-stu-id="e07a8-127">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="e07a8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e07a8-128">-ResourceGroupName</span></span>
<span data-ttu-id="e07a8-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e07a8-129">Resource group name.</span></span>

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

### <span data-ttu-id="e07a8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e07a8-130">-ResourceId</span></span>
<span data-ttu-id="e07a8-131">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="e07a8-131">Resource Id.</span></span>

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

### <span data-ttu-id="e07a8-132">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="e07a8-132">-TriggerUri</span></span>
<span data-ttu-id="e07a8-133">Uri триггера приложения "Логика действий".</span><span class="sxs-lookup"><span data-stu-id="e07a8-133">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="e07a8-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e07a8-134">-WorkspaceName</span></span>
<span data-ttu-id="e07a8-135">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e07a8-135">Workspace Name.</span></span>

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

### <span data-ttu-id="e07a8-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e07a8-136">-Confirm</span></span>
<span data-ttu-id="e07a8-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e07a8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e07a8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e07a8-138">-WhatIf</span></span>
<span data-ttu-id="e07a8-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e07a8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e07a8-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e07a8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e07a8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07a8-141">CommonParameters</span></span>
<span data-ttu-id="e07a8-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e07a8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07a8-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e07a8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07a8-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e07a8-144">INPUTS</span></span>

### <span data-ttu-id="e07a8-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="e07a8-145">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="e07a8-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="e07a8-146">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

### <span data-ttu-id="e07a8-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e07a8-147">System.String</span></span>

## <span data-ttu-id="e07a8-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e07a8-148">OUTPUTS</span></span>

### <span data-ttu-id="e07a8-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="e07a8-149">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>

## <span data-ttu-id="e07a8-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e07a8-150">NOTES</span></span>

## <span data-ttu-id="e07a8-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e07a8-151">RELATED LINKS</span></span>
