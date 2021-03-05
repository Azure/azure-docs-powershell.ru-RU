---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: af63ecd604f6ea7e475fcc8034a4e4b6d532069e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963651"
---
# <span data-ttu-id="a6d5f-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="a6d5f-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="a6d5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6d5f-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d5f-103">Удаление аналитического сообщения.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-103">Delete an Analytic.</span></span>

## <span data-ttu-id="a6d5f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6d5f-104">SYNTAX</span></span>

### <span data-ttu-id="a6d5f-105">AlertRuleId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6d5f-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6d5f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a6d5f-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6d5f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6d5f-107">DESCRIPTION</span></span>
<span data-ttu-id="a6d5f-108">**Cmdlet Remove-AzSentinelAlertRule** окончательно удаляет правило оповещения из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="a6d5f-109">Вы можете передать объект **AlertRule** с помощью оператора конвейера или указать необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="a6d5f-110">С помощью переменных Confirm и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="a6d5f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6d5f-111">EXAMPLES</span></span>

### <span data-ttu-id="a6d5f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6d5f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="a6d5f-113">Эта команда удаляет правило оповещения из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="a6d5f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6d5f-114">PARAMETERS</span></span>

### <span data-ttu-id="a6d5f-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="a6d5f-115">-AlertRuleId</span></span>
<span data-ttu-id="a6d5f-116">ИД правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-116">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6d5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d5f-117">-DefaultProfile</span></span>
<span data-ttu-id="a6d5f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6d5f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6d5f-119">-InputObject</span></span>
<span data-ttu-id="a6d5f-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6d5f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6d5f-121">-PassThru</span></span>
<span data-ttu-id="a6d5f-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="a6d5f-122">PassThru</span></span>

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

### <span data-ttu-id="a6d5f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6d5f-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6d5f-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6d5f-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a6d5f-125">-WorkspaceName</span></span>
<span data-ttu-id="a6d5f-126">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6d5f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6d5f-127">-Confirm</span></span>
<span data-ttu-id="a6d5f-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6d5f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6d5f-129">-WhatIf</span></span>
<span data-ttu-id="a6d5f-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6d5f-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6d5f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d5f-132">CommonParameters</span></span>
<span data-ttu-id="a6d5f-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6d5f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d5f-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6d5f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d5f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6d5f-135">INPUTS</span></span>

### <span data-ttu-id="a6d5f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a6d5f-136">System.String</span></span>
### <span data-ttu-id="a6d5f-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="a6d5f-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="a6d5f-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6d5f-138">OUTPUTS</span></span>

### <span data-ttu-id="a6d5f-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="a6d5f-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="a6d5f-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6d5f-140">NOTES</span></span>

## <span data-ttu-id="a6d5f-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6d5f-141">RELATED LINKS</span></span>
