---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: 83f4fae326920b24d272ae87341c20702a2bf8fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003747"
---
# <span data-ttu-id="683a4-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="683a4-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="683a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="683a4-102">SYNOPSIS</span></span>
<span data-ttu-id="683a4-103">Delete for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="683a4-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="683a4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="683a4-104">SYNTAX</span></span>

### <span data-ttu-id="683a4-105">ByScopeParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="683a4-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="683a4-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="683a4-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="683a4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="683a4-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="683a4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="683a4-108">DESCRIPTION</span></span>
<span data-ttu-id="683a4-109">Delete for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="683a4-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="683a4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="683a4-110">EXAMPLES</span></span>

### <span data-ttu-id="683a4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="683a4-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="683a4-112">Удаление ресурса на ресурсах с областью личных ссылок</span><span class="sxs-lookup"><span data-stu-id="683a4-112">delete private link scoped resource</span></span>

## <span data-ttu-id="683a4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="683a4-113">PARAMETERS</span></span>

### <span data-ttu-id="683a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="683a4-114">-DefaultProfile</span></span>
<span data-ttu-id="683a4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="683a4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="683a4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="683a4-116">-InputObject</span></span>
<span data-ttu-id="683a4-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="683a4-117">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="683a4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="683a4-118">-Name</span></span>
<span data-ttu-id="683a4-119">Имя ресурса с областью</span><span class="sxs-lookup"><span data-stu-id="683a4-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="683a4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="683a4-120">-ResourceGroupName</span></span>
<span data-ttu-id="683a4-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="683a4-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="683a4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="683a4-122">-ResourceId</span></span>
<span data-ttu-id="683a4-123">ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="683a4-123">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="683a4-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="683a4-124">-ScopeName</span></span>
<span data-ttu-id="683a4-125">Имя области приватных ссылок</span><span class="sxs-lookup"><span data-stu-id="683a4-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="683a4-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="683a4-126">-Confirm</span></span>
<span data-ttu-id="683a4-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="683a4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="683a4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="683a4-128">-WhatIf</span></span>
<span data-ttu-id="683a4-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="683a4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="683a4-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="683a4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="683a4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="683a4-131">CommonParameters</span></span>
<span data-ttu-id="683a4-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="683a4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="683a4-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="683a4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="683a4-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="683a4-134">INPUTS</span></span>

### <span data-ttu-id="683a4-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="683a4-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="683a4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="683a4-136">System.String</span></span>

## <span data-ttu-id="683a4-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="683a4-137">OUTPUTS</span></span>

### <span data-ttu-id="683a4-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="683a4-138">System.Boolean</span></span>

## <span data-ttu-id="683a4-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="683a4-139">NOTES</span></span>

## <span data-ttu-id="683a4-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="683a4-140">RELATED LINKS</span></span>
