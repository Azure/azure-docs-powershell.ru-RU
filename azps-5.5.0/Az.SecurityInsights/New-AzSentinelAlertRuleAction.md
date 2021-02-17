---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235812"
---
# <span data-ttu-id="ddbfd-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="ddbfd-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="ddbfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddbfd-102">SYNOPSIS</span></span>
<span data-ttu-id="ddbfd-103">Добавление автоматического ответа в аалталию.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="ddbfd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ddbfd-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddbfd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddbfd-105">DESCRIPTION</span></span>
<span data-ttu-id="ddbfd-106">Для правила оповещения в указанной рабочей области создается автоматический ответ для правила оповещения **New-AzSentinelAlertRuleAction.**</span><span class="sxs-lookup"><span data-stu-id="ddbfd-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="ddbfd-107">Необходимо предоставить Id resorce приложения Logic и Uri триггера, которые можно найти с помощью модуля Logic App.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="ddbfd-108">Параметр Confirm  и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="ddbfd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ddbfd-109">EXAMPLES</span></span>

### <span data-ttu-id="ddbfd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ddbfd-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="ddbfd-111">В этом примере создается правило **AlertRuleAction** для заданного правила оповещения с использованием свойств приложения "Логика", а затем оно сохраняется в переменной $AlertRuleAction оповещения.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="ddbfd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddbfd-112">PARAMETERS</span></span>

### <span data-ttu-id="ddbfd-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="ddbfd-113">-ActionId</span></span>
<span data-ttu-id="ddbfd-114">ИД действия.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-114">Action Id.</span></span>

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

### <span data-ttu-id="ddbfd-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="ddbfd-115">-AlertRuleId</span></span>
<span data-ttu-id="ddbfd-116">ИД правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="ddbfd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddbfd-117">-DefaultProfile</span></span>
<span data-ttu-id="ddbfd-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddbfd-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="ddbfd-119">-LogicAppResourceId</span></span>
<span data-ttu-id="ddbfd-120">ИД ресурса приложения Action Logic.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="ddbfd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddbfd-121">-ResourceGroupName</span></span>
<span data-ttu-id="ddbfd-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-122">Resource group name.</span></span>

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

### <span data-ttu-id="ddbfd-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="ddbfd-123">-TriggerUri</span></span>
<span data-ttu-id="ddbfd-124">Uri триггера приложения "Логика действий".</span><span class="sxs-lookup"><span data-stu-id="ddbfd-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="ddbfd-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ddbfd-125">-WorkspaceName</span></span>
<span data-ttu-id="ddbfd-126">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-126">Workspace Name.</span></span>

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

### <span data-ttu-id="ddbfd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddbfd-127">-Confirm</span></span>
<span data-ttu-id="ddbfd-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddbfd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddbfd-129">-WhatIf</span></span>
<span data-ttu-id="ddbfd-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddbfd-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddbfd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddbfd-132">CommonParameters</span></span>
<span data-ttu-id="ddbfd-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddbfd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddbfd-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddbfd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddbfd-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddbfd-135">INPUTS</span></span>

### <span data-ttu-id="ddbfd-136">Нет</span><span class="sxs-lookup"><span data-stu-id="ddbfd-136">None</span></span>
## <span data-ttu-id="ddbfd-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ddbfd-137">OUTPUTS</span></span>

### <span data-ttu-id="ddbfd-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="ddbfd-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="ddbfd-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ddbfd-139">NOTES</span></span>

## <span data-ttu-id="ddbfd-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddbfd-140">RELATED LINKS</span></span>
