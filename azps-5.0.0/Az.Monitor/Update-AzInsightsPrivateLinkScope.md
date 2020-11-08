---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247619"
---
# <span data-ttu-id="043dc-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="043dc-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="043dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="043dc-102">SYNOPSIS</span></span>
<span data-ttu-id="043dc-103">Обновление области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="043dc-103">Update for private link scope</span></span>

## <span data-ttu-id="043dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="043dc-104">SYNTAX</span></span>

### <span data-ttu-id="043dc-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="043dc-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="043dc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="043dc-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="043dc-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="043dc-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="043dc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="043dc-108">DESCRIPTION</span></span>
<span data-ttu-id="043dc-109">Обновление области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="043dc-109">Update for private link scope</span></span>

## <span data-ttu-id="043dc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="043dc-110">EXAMPLES</span></span>

### <span data-ttu-id="043dc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="043dc-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="043dc-112">Обновление области личных ссылок с именем "scope_name" в группе ресурсов "rg_name" для использования тега "Key: value"</span><span class="sxs-lookup"><span data-stu-id="043dc-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="043dc-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="043dc-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="043dc-114">Обновление области личных ссылок с помощью идентификатора ресурса для использования тега "Key: value"</span><span class="sxs-lookup"><span data-stu-id="043dc-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="043dc-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="043dc-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="043dc-116">Обновление области личных ссылок с помощью объекта области ввода закрытой ссылки для использования тега "Key: value"</span><span class="sxs-lookup"><span data-stu-id="043dc-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="043dc-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="043dc-117">PARAMETERS</span></span>

### <span data-ttu-id="043dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="043dc-118">-DefaultProfile</span></span>
<span data-ttu-id="043dc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="043dc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="043dc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="043dc-120">-InputObject</span></span>
<span data-ttu-id="043dc-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="043dc-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="043dc-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="043dc-122">-Name</span></span>
<span data-ttu-id="043dc-123">Имя области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="043dc-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="043dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="043dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="043dc-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="043dc-125">Resource Group Name</span></span>

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

### <span data-ttu-id="043dc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="043dc-126">-ResourceId</span></span>
<span data-ttu-id="043dc-127">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="043dc-127">Resource Id</span></span>

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

### <span data-ttu-id="043dc-128">-Теги</span><span class="sxs-lookup"><span data-stu-id="043dc-128">-Tags</span></span>
<span data-ttu-id="043dc-129">Embed</span><span class="sxs-lookup"><span data-stu-id="043dc-129">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043dc-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="043dc-130">-Confirm</span></span>
<span data-ttu-id="043dc-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="043dc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="043dc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="043dc-132">-WhatIf</span></span>
<span data-ttu-id="043dc-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="043dc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="043dc-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="043dc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="043dc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="043dc-135">CommonParameters</span></span>
<span data-ttu-id="043dc-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="043dc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="043dc-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="043dc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="043dc-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="043dc-138">INPUTS</span></span>

### <span data-ttu-id="043dc-139">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="043dc-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="043dc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="043dc-140">System.String</span></span>

## <span data-ttu-id="043dc-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="043dc-141">OUTPUTS</span></span>

### <span data-ttu-id="043dc-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="043dc-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="043dc-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="043dc-143">NOTES</span></span>

## <span data-ttu-id="043dc-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="043dc-144">RELATED LINKS</span></span>
