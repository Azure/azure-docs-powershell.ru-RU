---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405023"
---
# <span data-ttu-id="1e279-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="1e279-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="1e279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e279-102">SYNOPSIS</span></span>
<span data-ttu-id="1e279-103">Создать для ресурса с областью частных связей</span><span class="sxs-lookup"><span data-stu-id="1e279-103">create for private link scoped resource</span></span>

## <span data-ttu-id="1e279-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1e279-104">SYNTAX</span></span>

### <span data-ttu-id="1e279-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e279-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e279-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e279-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e279-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e279-107">DESCRIPTION</span></span>
<span data-ttu-id="1e279-108">Создать для частного ресурса с областью действия ссылки, область действия ресурса может быть рабочей областью аналитики журнала или компонентом Application Insights</span><span class="sxs-lookup"><span data-stu-id="1e279-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="1e279-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1e279-109">EXAMPLES</span></span>

### <span data-ttu-id="1e279-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1e279-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="1e279-111">создание областей ресурса "scoped_resource_name", связанных с компонентом статистики приложения "ai_name"</span><span class="sxs-lookup"><span data-stu-id="1e279-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="1e279-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e279-112">PARAMETERS</span></span>

### <span data-ttu-id="1e279-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e279-113">-DefaultProfile</span></span>
<span data-ttu-id="1e279-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e279-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e279-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e279-115">-InputObject</span></span>
<span data-ttu-id="1e279-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="1e279-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="1e279-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="1e279-117">-LinkedResourceId</span></span>
<span data-ttu-id="1e279-118">LA/AI Resource Id to Link</span><span class="sxs-lookup"><span data-stu-id="1e279-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="1e279-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1e279-119">-Name</span></span>
<span data-ttu-id="1e279-120">Имя ресурса с областью</span><span class="sxs-lookup"><span data-stu-id="1e279-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="1e279-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e279-121">-ResourceGroupName</span></span>
<span data-ttu-id="1e279-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1e279-122">Resource Group Name</span></span>

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

### <span data-ttu-id="1e279-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="1e279-123">-ScopeName</span></span>
<span data-ttu-id="1e279-124">Имя области приватных ссылок</span><span class="sxs-lookup"><span data-stu-id="1e279-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="1e279-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e279-125">-Confirm</span></span>
<span data-ttu-id="1e279-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1e279-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e279-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e279-127">-WhatIf</span></span>
<span data-ttu-id="1e279-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e279-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e279-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1e279-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e279-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e279-130">CommonParameters</span></span>
<span data-ttu-id="1e279-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e279-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e279-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e279-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e279-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e279-133">INPUTS</span></span>

### <span data-ttu-id="1e279-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="1e279-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="1e279-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1e279-135">System.String</span></span>

## <span data-ttu-id="1e279-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1e279-136">OUTPUTS</span></span>

### <span data-ttu-id="1e279-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="1e279-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="1e279-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1e279-138">NOTES</span></span>

## <span data-ttu-id="1e279-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e279-139">RELATED LINKS</span></span>
