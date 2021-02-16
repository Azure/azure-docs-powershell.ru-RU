---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: 415a4156831d00672aba5709d3f915625adac106
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235780"
---
# <span data-ttu-id="6fbc2-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="6fbc2-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="6fbc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fbc2-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbc2-103">Удаление аналитического сообщения.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-103">Delete an Analytic.</span></span>

## <span data-ttu-id="6fbc2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6fbc2-104">SYNTAX</span></span>

### <span data-ttu-id="6fbc2-105">AlertRuleId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6fbc2-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbc2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6fbc2-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fbc2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fbc2-107">DESCRIPTION</span></span>
<span data-ttu-id="6fbc2-108">**Cmdlet Remove-AzSentinelAlertRule** окончательно удаляет правило оповещения из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="6fbc2-109">Вы можете передать объект **AlertRule** с помощью оператора конвейера или указать необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="6fbc2-110">Параметр Confirm и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="6fbc2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6fbc2-111">EXAMPLES</span></span>

### <span data-ttu-id="6fbc2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6fbc2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="6fbc2-113">Эта команда удаляет правило оповещения из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="6fbc2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fbc2-114">PARAMETERS</span></span>

### <span data-ttu-id="6fbc2-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="6fbc2-115">-AlertRuleId</span></span>
<span data-ttu-id="6fbc2-116">ИД правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="6fbc2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbc2-117">-DefaultProfile</span></span>
<span data-ttu-id="6fbc2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fbc2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fbc2-119">-InputObject</span></span>
<span data-ttu-id="6fbc2-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-120">InputObject.</span></span>

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

### <span data-ttu-id="6fbc2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fbc2-121">-PassThru</span></span>
<span data-ttu-id="6fbc2-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="6fbc2-122">PassThru</span></span>

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

### <span data-ttu-id="6fbc2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fbc2-123">-ResourceGroupName</span></span>
<span data-ttu-id="6fbc2-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-124">Resource group name.</span></span>

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

### <span data-ttu-id="6fbc2-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6fbc2-125">-WorkspaceName</span></span>
<span data-ttu-id="6fbc2-126">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-126">Workspace Name.</span></span>

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

### <span data-ttu-id="6fbc2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fbc2-127">-Confirm</span></span>
<span data-ttu-id="6fbc2-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fbc2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fbc2-129">-WhatIf</span></span>
<span data-ttu-id="6fbc2-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fbc2-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fbc2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbc2-132">CommonParameters</span></span>
<span data-ttu-id="6fbc2-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fbc2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbc2-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fbc2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbc2-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fbc2-135">INPUTS</span></span>

### <span data-ttu-id="6fbc2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6fbc2-136">System.String</span></span>
### <span data-ttu-id="6fbc2-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="6fbc2-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="6fbc2-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6fbc2-138">OUTPUTS</span></span>

### <span data-ttu-id="6fbc2-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="6fbc2-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="6fbc2-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6fbc2-140">NOTES</span></span>

## <span data-ttu-id="6fbc2-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fbc2-141">RELATED LINKS</span></span>
