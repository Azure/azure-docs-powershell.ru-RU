---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244427"
---
# <span data-ttu-id="88bbc-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="88bbc-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="88bbc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="88bbc-103">Создание ресурса с областью действия частной ссылки</span><span class="sxs-lookup"><span data-stu-id="88bbc-103">create for private link scoped resource</span></span>

## <span data-ttu-id="88bbc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88bbc-104">SYNTAX</span></span>

### <span data-ttu-id="88bbc-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88bbc-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88bbc-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88bbc-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88bbc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88bbc-107">DESCRIPTION</span></span>
<span data-ttu-id="88bbc-108">Создание ресурса с областью действия для закрытой ссылки ресурс с областью действия может быть рабочей областью аналитики журнала или компонент Application Insights</span><span class="sxs-lookup"><span data-stu-id="88bbc-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="88bbc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88bbc-109">EXAMPLES</span></span>

### <span data-ttu-id="88bbc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88bbc-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="88bbc-111">Создание ресурса с областью "scoped_resource_name", связанного с компонентом Application Insights "ai_name"</span><span class="sxs-lookup"><span data-stu-id="88bbc-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="88bbc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88bbc-112">PARAMETERS</span></span>

### <span data-ttu-id="88bbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88bbc-113">-DefaultProfile</span></span>
<span data-ttu-id="88bbc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88bbc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88bbc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88bbc-115">-InputObject</span></span>
<span data-ttu-id="88bbc-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="88bbc-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="88bbc-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="88bbc-117">-LinkedResourceId</span></span>
<span data-ttu-id="88bbc-118">Код ресурса LA/AI для связывания</span><span class="sxs-lookup"><span data-stu-id="88bbc-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="88bbc-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88bbc-119">-Name</span></span>
<span data-ttu-id="88bbc-120">Название ресурса с областью действия</span><span class="sxs-lookup"><span data-stu-id="88bbc-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="88bbc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88bbc-121">-ResourceGroupName</span></span>
<span data-ttu-id="88bbc-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="88bbc-122">Resource Group Name</span></span>

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

### <span data-ttu-id="88bbc-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="88bbc-123">-ScopeName</span></span>
<span data-ttu-id="88bbc-124">Имя области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="88bbc-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="88bbc-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88bbc-125">-Confirm</span></span>
<span data-ttu-id="88bbc-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88bbc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88bbc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88bbc-127">-WhatIf</span></span>
<span data-ttu-id="88bbc-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88bbc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88bbc-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88bbc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88bbc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88bbc-130">CommonParameters</span></span>
<span data-ttu-id="88bbc-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88bbc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88bbc-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88bbc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88bbc-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88bbc-133">INPUTS</span></span>

### <span data-ttu-id="88bbc-134">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="88bbc-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="88bbc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="88bbc-135">System.String</span></span>

## <span data-ttu-id="88bbc-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88bbc-136">OUTPUTS</span></span>

### <span data-ttu-id="88bbc-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="88bbc-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="88bbc-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="88bbc-138">NOTES</span></span>

## <span data-ttu-id="88bbc-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88bbc-139">RELATED LINKS</span></span>
