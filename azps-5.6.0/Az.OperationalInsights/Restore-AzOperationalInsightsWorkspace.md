---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1035d918870a15000be066fd59cc72913d8d8cf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989750"
---
# <span data-ttu-id="29bf4-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="29bf4-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="29bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="29bf4-103">Восстановление удаленной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="29bf4-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="29bf4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="29bf4-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29bf4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="29bf4-106">Восстановление удаленной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="29bf4-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="29bf4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="29bf4-107">EXAMPLES</span></span>

### <span data-ttu-id="29bf4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="29bf4-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="29bf4-109">Восстановление удаленной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="29bf4-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="29bf4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29bf4-110">PARAMETERS</span></span>

### <span data-ttu-id="29bf4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29bf4-111">-DefaultProfile</span></span>
<span data-ttu-id="29bf4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29bf4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29bf4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="29bf4-113">-Force</span></span>
<span data-ttu-id="29bf4-114">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="29bf4-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="29bf4-115">-Location</span><span class="sxs-lookup"><span data-stu-id="29bf4-115">-Location</span></span>
<span data-ttu-id="29bf4-116">Географический регион, в который будет создана рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="29bf4-116">The geographic region that the workspace will be created in.</span></span>

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

### <span data-ttu-id="29bf4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="29bf4-117">-Name</span></span>
<span data-ttu-id="29bf4-118">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="29bf4-118">The workspace name.</span></span>

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

### <span data-ttu-id="29bf4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29bf4-119">-ResourceGroupName</span></span>
<span data-ttu-id="29bf4-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29bf4-120">The resource group name.</span></span>

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

### <span data-ttu-id="29bf4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29bf4-121">-Confirm</span></span>
<span data-ttu-id="29bf4-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29bf4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29bf4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29bf4-123">-WhatIf</span></span>
<span data-ttu-id="29bf4-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29bf4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29bf4-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="29bf4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29bf4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bf4-126">CommonParameters</span></span>
<span data-ttu-id="29bf4-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29bf4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bf4-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29bf4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bf4-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29bf4-129">INPUTS</span></span>

### <span data-ttu-id="29bf4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="29bf4-130">System.String</span></span>

## <span data-ttu-id="29bf4-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="29bf4-131">OUTPUTS</span></span>

### <span data-ttu-id="29bf4-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="29bf4-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="29bf4-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="29bf4-133">NOTES</span></span>

## <span data-ttu-id="29bf4-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29bf4-134">RELATED LINKS</span></span>
