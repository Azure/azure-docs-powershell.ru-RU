---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911787"
---
# <span data-ttu-id="21660-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="21660-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="21660-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21660-102">SYNOPSIS</span></span>
<span data-ttu-id="21660-103">Удаление области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="21660-103">delete private link scope</span></span>

## <span data-ttu-id="21660-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21660-104">SYNTAX</span></span>

### <span data-ttu-id="21660-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21660-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21660-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21660-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21660-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21660-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21660-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21660-108">DESCRIPTION</span></span>
<span data-ttu-id="21660-109">Удаление области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="21660-109">delete private link scope</span></span>

## <span data-ttu-id="21660-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21660-110">EXAMPLES</span></span>

### <span data-ttu-id="21660-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="21660-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="21660-112">Удаление области личных ссылок с именем "scope_name" в разделе "Группа ресурсов" rg_name "</span><span class="sxs-lookup"><span data-stu-id="21660-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="21660-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="21660-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="21660-114">Удаление области личных ссылок с ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="21660-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="21660-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="21660-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="21660-116">Удаление области личных ссылок с объектом области ввода закрытой ссылки</span><span class="sxs-lookup"><span data-stu-id="21660-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="21660-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21660-117">PARAMETERS</span></span>

### <span data-ttu-id="21660-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21660-118">-DefaultProfile</span></span>
<span data-ttu-id="21660-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21660-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21660-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21660-120">-InputObject</span></span>
<span data-ttu-id="21660-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="21660-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="21660-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="21660-122">-Name</span></span>
<span data-ttu-id="21660-123">Имя области личных ссылок</span><span class="sxs-lookup"><span data-stu-id="21660-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="21660-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21660-124">-ResourceGroupName</span></span>
<span data-ttu-id="21660-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="21660-125">Resource Group Name</span></span>

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

### <span data-ttu-id="21660-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21660-126">-ResourceId</span></span>
<span data-ttu-id="21660-127">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="21660-127">Resource Id</span></span>

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

### <span data-ttu-id="21660-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21660-128">-Confirm</span></span>
<span data-ttu-id="21660-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="21660-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21660-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21660-130">-WhatIf</span></span>
<span data-ttu-id="21660-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="21660-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21660-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="21660-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21660-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21660-133">CommonParameters</span></span>
<span data-ttu-id="21660-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21660-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21660-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21660-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21660-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21660-136">INPUTS</span></span>

### <span data-ttu-id="21660-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="21660-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="21660-138">System. String</span><span class="sxs-lookup"><span data-stu-id="21660-138">System.String</span></span>

## <span data-ttu-id="21660-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21660-139">OUTPUTS</span></span>

### <span data-ttu-id="21660-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="21660-140">System.Boolean</span></span>

## <span data-ttu-id="21660-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="21660-141">NOTES</span></span>

## <span data-ttu-id="21660-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21660-142">RELATED LINKS</span></span>
