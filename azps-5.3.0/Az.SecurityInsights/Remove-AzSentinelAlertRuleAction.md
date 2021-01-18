---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 48566fde735deb5693783f9e71f047f73d5f9336
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517542"
---
# <span data-ttu-id="ad3cb-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="ad3cb-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="ad3cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad3cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3cb-103">Удаление автоматического ответа из аналитического.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="ad3cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad3cb-104">SYNTAX</span></span>

### <span data-ttu-id="ad3cb-105">ActionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad3cb-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad3cb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ad3cb-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad3cb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad3cb-107">DESCRIPTION</span></span>
<span data-ttu-id="ad3cb-108">С **помощью cmdlet Remove-AzSentinelAlertRuleAction** автоматический ответ удаляется из правила оповещения в указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="ad3cb-109">Объект **AlertRuleAction** можно передать с помощью оператора конвейера или указать необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="ad3cb-110">С помощью переменных Confirm и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="ad3cb-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad3cb-111">EXAMPLES</span></span>

### <span data-ttu-id="ad3cb-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad3cb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="ad3cb-113">Эта команда удаляет правило оповещения из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="ad3cb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad3cb-114">PARAMETERS</span></span>

### <span data-ttu-id="ad3cb-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="ad3cb-115">-ActionId</span></span>
<span data-ttu-id="ad3cb-116">ИД действия.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-116">Action Id.</span></span>

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

### <span data-ttu-id="ad3cb-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="ad3cb-117">-AlertRuleId</span></span>
<span data-ttu-id="ad3cb-118">ИД правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-118">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad3cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3cb-119">-DefaultProfile</span></span>
<span data-ttu-id="ad3cb-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad3cb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad3cb-121">-InputObject</span></span>
<span data-ttu-id="ad3cb-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-122">InputObject.</span></span>

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

### <span data-ttu-id="ad3cb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad3cb-123">-PassThru</span></span>
<span data-ttu-id="ad3cb-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="ad3cb-124">PassThru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3cb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad3cb-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad3cb-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad3cb-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ad3cb-127">-WorkspaceName</span></span>
<span data-ttu-id="ad3cb-128">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad3cb-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad3cb-129">-Confirm</span></span>
<span data-ttu-id="ad3cb-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad3cb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad3cb-131">-WhatIf</span></span>
<span data-ttu-id="ad3cb-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad3cb-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad3cb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3cb-134">CommonParameters</span></span>
<span data-ttu-id="ad3cb-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad3cb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3cb-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad3cb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3cb-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad3cb-137">INPUTS</span></span>

### <span data-ttu-id="ad3cb-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ad3cb-138">System.String</span></span>
### <span data-ttu-id="ad3cb-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="ad3cb-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="ad3cb-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad3cb-140">OUTPUTS</span></span>

### <span data-ttu-id="ad3cb-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="ad3cb-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="ad3cb-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad3cb-142">NOTES</span></span>

## <span data-ttu-id="ad3cb-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad3cb-143">RELATED LINKS</span></span>
