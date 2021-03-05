---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: 10ae3aab71cd977d3447501d13870eb10a8129ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009507"
---
# <span data-ttu-id="1eb13-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="1eb13-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="1eb13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eb13-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb13-103">Создать для ресурса с областью частных связей</span><span class="sxs-lookup"><span data-stu-id="1eb13-103">create for private link scoped resource</span></span>

## <span data-ttu-id="1eb13-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1eb13-104">SYNTAX</span></span>

### <span data-ttu-id="1eb13-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1eb13-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1eb13-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eb13-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1eb13-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eb13-107">DESCRIPTION</span></span>
<span data-ttu-id="1eb13-108">Создать для частного ресурса с областью действия ссылки, область действия ресурса может быть рабочей областью аналитики журнала или компонентом Application Insights</span><span class="sxs-lookup"><span data-stu-id="1eb13-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="1eb13-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1eb13-109">EXAMPLES</span></span>

### <span data-ttu-id="1eb13-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1eb13-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="1eb13-111">создание области действия "scoped_resource_name", связанной с компонентом статистики приложения "ai_name"</span><span class="sxs-lookup"><span data-stu-id="1eb13-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="1eb13-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1eb13-112">PARAMETERS</span></span>

### <span data-ttu-id="1eb13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb13-113">-DefaultProfile</span></span>
<span data-ttu-id="1eb13-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb13-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eb13-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1eb13-115">-InputObject</span></span>
<span data-ttu-id="1eb13-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="1eb13-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="1eb13-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="1eb13-117">-LinkedResourceId</span></span>
<span data-ttu-id="1eb13-118">LA/AI Resource Id to Link</span><span class="sxs-lookup"><span data-stu-id="1eb13-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="1eb13-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1eb13-119">-Name</span></span>
<span data-ttu-id="1eb13-120">Имя ресурса с областью</span><span class="sxs-lookup"><span data-stu-id="1eb13-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="1eb13-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb13-121">-ResourceGroupName</span></span>
<span data-ttu-id="1eb13-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1eb13-122">Resource Group Name</span></span>

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

### <span data-ttu-id="1eb13-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="1eb13-123">-ScopeName</span></span>
<span data-ttu-id="1eb13-124">Имя области приватных ссылок</span><span class="sxs-lookup"><span data-stu-id="1eb13-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="1eb13-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1eb13-125">-Confirm</span></span>
<span data-ttu-id="1eb13-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eb13-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eb13-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb13-127">-WhatIf</span></span>
<span data-ttu-id="1eb13-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eb13-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eb13-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1eb13-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eb13-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb13-130">CommonParameters</span></span>
<span data-ttu-id="1eb13-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb13-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb13-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1eb13-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb13-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1eb13-133">INPUTS</span></span>

### <span data-ttu-id="1eb13-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="1eb13-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="1eb13-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1eb13-135">System.String</span></span>

## <span data-ttu-id="1eb13-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1eb13-136">OUTPUTS</span></span>

### <span data-ttu-id="1eb13-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="1eb13-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="1eb13-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1eb13-138">NOTES</span></span>

## <span data-ttu-id="1eb13-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1eb13-139">RELATED LINKS</span></span>
