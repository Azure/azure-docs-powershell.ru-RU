---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221452"
---
# <span data-ttu-id="3dcd4-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3dcd4-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="3dcd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dcd4-102">SYNOPSIS</span></span>
<span data-ttu-id="3dcd4-103">Обновление области частных ссылок</span><span class="sxs-lookup"><span data-stu-id="3dcd4-103">Update for private link scope</span></span>

## <span data-ttu-id="3dcd4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3dcd4-104">SYNTAX</span></span>

### <span data-ttu-id="3dcd4-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3dcd4-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dcd4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dcd4-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dcd4-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dcd4-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dcd4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dcd4-108">DESCRIPTION</span></span>
<span data-ttu-id="3dcd4-109">Обновление области частных ссылок</span><span class="sxs-lookup"><span data-stu-id="3dcd4-109">Update for private link scope</span></span>

## <span data-ttu-id="3dcd4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3dcd4-110">EXAMPLES</span></span>

### <span data-ttu-id="3dcd4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3dcd4-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="3dcd4-112">Обновив область приватных ссылок с помощью имени "scope_name" в группе ресурсов "rg_name", чтобы использовать тег "key:value"</span><span class="sxs-lookup"><span data-stu-id="3dcd4-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="3dcd4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3dcd4-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="3dcd4-114">Обновление области личной ссылки с помощью ИД ресурса, чтобы использовать тег "key:value"</span><span class="sxs-lookup"><span data-stu-id="3dcd4-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="3dcd4-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3dcd4-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="3dcd4-116">Обновление области приватных ссылок с использованием объекта входной частной области ссылки для использования тега "key:value"</span><span class="sxs-lookup"><span data-stu-id="3dcd4-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="3dcd4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dcd4-117">PARAMETERS</span></span>

### <span data-ttu-id="3dcd4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dcd4-118">-DefaultProfile</span></span>
<span data-ttu-id="3dcd4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3dcd4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dcd4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dcd4-120">-InputObject</span></span>
<span data-ttu-id="3dcd4-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3dcd4-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="3dcd4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3dcd4-122">-Name</span></span>
<span data-ttu-id="3dcd4-123">Имя области приватных ссылок</span><span class="sxs-lookup"><span data-stu-id="3dcd4-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="3dcd4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dcd4-124">-ResourceGroupName</span></span>
<span data-ttu-id="3dcd4-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3dcd4-125">Resource Group Name</span></span>

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

### <span data-ttu-id="3dcd4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dcd4-126">-ResourceId</span></span>
<span data-ttu-id="3dcd4-127">ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="3dcd4-127">Resource Id</span></span>

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

### <span data-ttu-id="3dcd4-128">-Теги</span><span class="sxs-lookup"><span data-stu-id="3dcd4-128">-Tags</span></span>
<span data-ttu-id="3dcd4-129">Теги</span><span class="sxs-lookup"><span data-stu-id="3dcd4-129">Tags</span></span>

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

### <span data-ttu-id="3dcd4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dcd4-130">-Confirm</span></span>
<span data-ttu-id="3dcd4-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dcd4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dcd4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dcd4-132">-WhatIf</span></span>
<span data-ttu-id="3dcd4-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dcd4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dcd4-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3dcd4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dcd4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dcd4-135">CommonParameters</span></span>
<span data-ttu-id="3dcd4-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dcd4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dcd4-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3dcd4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dcd4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3dcd4-138">INPUTS</span></span>

### <span data-ttu-id="3dcd4-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3dcd4-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="3dcd4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3dcd4-140">System.String</span></span>

## <span data-ttu-id="3dcd4-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3dcd4-141">OUTPUTS</span></span>

### <span data-ttu-id="3dcd4-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3dcd4-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="3dcd4-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3dcd4-143">NOTES</span></span>

## <span data-ttu-id="3dcd4-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3dcd4-144">RELATED LINKS</span></span>
