---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: af33bf23e6cd488f98e38c9bd2696029b5510aca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984511"
---
# <span data-ttu-id="cba92-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cba92-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="cba92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cba92-102">SYNOPSIS</span></span>
<span data-ttu-id="cba92-103">Удаление области частных ссылок</span><span class="sxs-lookup"><span data-stu-id="cba92-103">delete private link scope</span></span>

## <span data-ttu-id="cba92-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cba92-104">SYNTAX</span></span>

### <span data-ttu-id="cba92-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cba92-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cba92-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cba92-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cba92-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cba92-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cba92-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cba92-108">DESCRIPTION</span></span>
<span data-ttu-id="cba92-109">Удаление области частных ссылок</span><span class="sxs-lookup"><span data-stu-id="cba92-109">delete private link scope</span></span>

## <span data-ttu-id="cba92-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cba92-110">EXAMPLES</span></span>

### <span data-ttu-id="cba92-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cba92-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="cba92-112">Удалить частную область ссылок с именем "scope_name" в группе ресурсов "rg_name"</span><span class="sxs-lookup"><span data-stu-id="cba92-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="cba92-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cba92-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="cba92-114">Удаление области частных связей с помощью ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="cba92-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="cba92-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cba92-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="cba92-116">Удалить частную область ссылок с объектом input private link scope</span><span class="sxs-lookup"><span data-stu-id="cba92-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="cba92-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cba92-117">PARAMETERS</span></span>

### <span data-ttu-id="cba92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba92-118">-DefaultProfile</span></span>
<span data-ttu-id="cba92-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cba92-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cba92-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cba92-120">-InputObject</span></span>
<span data-ttu-id="cba92-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cba92-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="cba92-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cba92-122">-Name</span></span>
<span data-ttu-id="cba92-123">Имя области приватных ссылок</span><span class="sxs-lookup"><span data-stu-id="cba92-123">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba92-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba92-124">-ResourceGroupName</span></span>
<span data-ttu-id="cba92-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cba92-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba92-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cba92-126">-ResourceId</span></span>
<span data-ttu-id="cba92-127">ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="cba92-127">Resource Id</span></span>

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

### <span data-ttu-id="cba92-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cba92-128">-Confirm</span></span>
<span data-ttu-id="cba92-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cba92-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cba92-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cba92-130">-WhatIf</span></span>
<span data-ttu-id="cba92-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cba92-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cba92-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cba92-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cba92-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba92-133">CommonParameters</span></span>
<span data-ttu-id="cba92-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cba92-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba92-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cba92-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba92-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cba92-136">INPUTS</span></span>

### <span data-ttu-id="cba92-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cba92-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="cba92-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cba92-138">System.String</span></span>

## <span data-ttu-id="cba92-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cba92-139">OUTPUTS</span></span>

### <span data-ttu-id="cba92-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cba92-140">System.Boolean</span></span>

## <span data-ttu-id="cba92-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cba92-141">NOTES</span></span>

## <span data-ttu-id="cba92-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cba92-142">RELATED LINKS</span></span>
