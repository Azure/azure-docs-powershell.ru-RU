---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506050"
---
# <span data-ttu-id="87da5-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="87da5-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="87da5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87da5-102">SYNOPSIS</span></span>
<span data-ttu-id="87da5-103">Восстановление удаленной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="87da5-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="87da5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="87da5-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87da5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87da5-105">DESCRIPTION</span></span>
<span data-ttu-id="87da5-106">Восстановление удаленной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="87da5-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="87da5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="87da5-107">EXAMPLES</span></span>

### <span data-ttu-id="87da5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87da5-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="87da5-109">Восстановление удаленной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="87da5-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="87da5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87da5-110">PARAMETERS</span></span>

### <span data-ttu-id="87da5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87da5-111">-DefaultProfile</span></span>
<span data-ttu-id="87da5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87da5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87da5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="87da5-113">-Force</span></span>
<span data-ttu-id="87da5-114">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="87da5-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="87da5-115">-Location</span><span class="sxs-lookup"><span data-stu-id="87da5-115">-Location</span></span>
<span data-ttu-id="87da5-116">Географический регион, в который будет создана рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="87da5-116">The geographic region that the workspace will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87da5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="87da5-117">-Name</span></span>
<span data-ttu-id="87da5-118">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="87da5-118">The workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87da5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87da5-119">-ResourceGroupName</span></span>
<span data-ttu-id="87da5-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87da5-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87da5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87da5-121">-Confirm</span></span>
<span data-ttu-id="87da5-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="87da5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87da5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87da5-123">-WhatIf</span></span>
<span data-ttu-id="87da5-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87da5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87da5-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="87da5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87da5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87da5-126">CommonParameters</span></span>
<span data-ttu-id="87da5-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87da5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87da5-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87da5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87da5-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87da5-129">INPUTS</span></span>

### <span data-ttu-id="87da5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="87da5-130">System.String</span></span>

## <span data-ttu-id="87da5-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87da5-131">OUTPUTS</span></span>

### <span data-ttu-id="87da5-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="87da5-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="87da5-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="87da5-133">NOTES</span></span>

## <span data-ttu-id="87da5-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87da5-134">RELATED LINKS</span></span>
