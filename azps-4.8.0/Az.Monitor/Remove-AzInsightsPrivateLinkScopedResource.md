---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236087"
---
# <span data-ttu-id="fe732-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="fe732-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="fe732-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe732-102">SYNOPSIS</span></span>
<span data-ttu-id="fe732-103">Удаление ресурса с областью личных ссылок</span><span class="sxs-lookup"><span data-stu-id="fe732-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="fe732-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe732-104">SYNTAX</span></span>

### <span data-ttu-id="fe732-105">ByScopeParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe732-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe732-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe732-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe732-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe732-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe732-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe732-108">DESCRIPTION</span></span>
<span data-ttu-id="fe732-109">Удаление ресурса с областью личных ссылок</span><span class="sxs-lookup"><span data-stu-id="fe732-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="fe732-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe732-110">EXAMPLES</span></span>

### <span data-ttu-id="fe732-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe732-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="fe732-112">Удаление ресурса с областью действия частной ссылки</span><span class="sxs-lookup"><span data-stu-id="fe732-112">delete private link scoped resource</span></span>

## <span data-ttu-id="fe732-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe732-113">PARAMETERS</span></span>

### <span data-ttu-id="fe732-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe732-114">-DefaultProfile</span></span>
<span data-ttu-id="fe732-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe732-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe732-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe732-116">-InputObject</span></span>
<span data-ttu-id="fe732-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="fe732-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="fe732-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fe732-118">-Name</span></span>
<span data-ttu-id="fe732-119">Название ресурса с областью действия</span><span class="sxs-lookup"><span data-stu-id="fe732-119">Scoped resource Name</span></span>

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

### <span data-ttu-id="fe732-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe732-120">-ResourceGroupName</span></span>
<span data-ttu-id="fe732-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fe732-121">Resource Group Name</span></span>

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

### <span data-ttu-id="fe732-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe732-122">-ResourceId</span></span>
<span data-ttu-id="fe732-123">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="fe732-123">Resource Id</span></span>

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

### <span data-ttu-id="fe732-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="fe732-124">-ScopeName</span></span>
<span data-ttu-id="fe732-125">Имя области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="fe732-125">Private Link Scope Name</span></span>

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

### <span data-ttu-id="fe732-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe732-126">-Confirm</span></span>
<span data-ttu-id="fe732-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe732-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe732-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe732-128">-WhatIf</span></span>
<span data-ttu-id="fe732-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe732-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe732-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe732-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe732-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe732-131">CommonParameters</span></span>
<span data-ttu-id="fe732-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe732-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe732-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe732-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe732-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe732-134">INPUTS</span></span>

### <span data-ttu-id="fe732-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="fe732-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="fe732-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fe732-136">System.String</span></span>

## <span data-ttu-id="fe732-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe732-137">OUTPUTS</span></span>

### <span data-ttu-id="fe732-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe732-138">System.Boolean</span></span>

## <span data-ttu-id="fe732-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe732-139">NOTES</span></span>

## <span data-ttu-id="fe732-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe732-140">RELATED LINKS</span></span>
