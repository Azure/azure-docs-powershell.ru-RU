---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 48566fde735deb5693783f9e71f047f73d5f9336
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235777"
---
# <span data-ttu-id="1c40a-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="1c40a-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="1c40a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c40a-102">SYNOPSIS</span></span>
<span data-ttu-id="1c40a-103">Удаление автоматического ответа из аналитического.</span><span class="sxs-lookup"><span data-stu-id="1c40a-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="1c40a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1c40a-104">SYNTAX</span></span>

### <span data-ttu-id="1c40a-105">ActionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c40a-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c40a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1c40a-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c40a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c40a-107">DESCRIPTION</span></span>
<span data-ttu-id="1c40a-108">С **помощью cmdlet Remove-AzSentinelAlertRuleAction** автоматический ответ удаляется из правила оповещения в указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1c40a-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="1c40a-109">Объект **AlertRuleAction** можно передать с помощью оператора конвейера или указать необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="1c40a-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="1c40a-110">Параметр Confirm и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c40a-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="1c40a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1c40a-111">EXAMPLES</span></span>

### <span data-ttu-id="1c40a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c40a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="1c40a-113">Эта команда удаляет правило оповещения из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1c40a-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="1c40a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c40a-114">PARAMETERS</span></span>

### <span data-ttu-id="1c40a-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="1c40a-115">-ActionId</span></span>
<span data-ttu-id="1c40a-116">ИД действия.</span><span class="sxs-lookup"><span data-stu-id="1c40a-116">Action Id.</span></span>

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

### <span data-ttu-id="1c40a-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="1c40a-117">-AlertRuleId</span></span>
<span data-ttu-id="1c40a-118">ИД правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="1c40a-118">Alert Rule Id.</span></span>

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

### <span data-ttu-id="1c40a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c40a-119">-DefaultProfile</span></span>
<span data-ttu-id="1c40a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c40a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c40a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c40a-121">-InputObject</span></span>
<span data-ttu-id="1c40a-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="1c40a-122">InputObject.</span></span>

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

### <span data-ttu-id="1c40a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c40a-123">-PassThru</span></span>
<span data-ttu-id="1c40a-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="1c40a-124">PassThru</span></span>

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

### <span data-ttu-id="1c40a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c40a-125">-ResourceGroupName</span></span>
<span data-ttu-id="1c40a-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c40a-126">Resource group name.</span></span>

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

### <span data-ttu-id="1c40a-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1c40a-127">-WorkspaceName</span></span>
<span data-ttu-id="1c40a-128">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1c40a-128">Workspace Name.</span></span>

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

### <span data-ttu-id="1c40a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c40a-129">-Confirm</span></span>
<span data-ttu-id="1c40a-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1c40a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c40a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c40a-131">-WhatIf</span></span>
<span data-ttu-id="1c40a-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c40a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c40a-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1c40a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c40a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c40a-134">CommonParameters</span></span>
<span data-ttu-id="1c40a-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c40a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c40a-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c40a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c40a-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c40a-137">INPUTS</span></span>

### <span data-ttu-id="1c40a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1c40a-138">System.String</span></span>
### <span data-ttu-id="1c40a-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="1c40a-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="1c40a-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1c40a-140">OUTPUTS</span></span>

### <span data-ttu-id="1c40a-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="1c40a-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="1c40a-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1c40a-142">NOTES</span></span>

## <span data-ttu-id="1c40a-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c40a-143">RELATED LINKS</span></span>
