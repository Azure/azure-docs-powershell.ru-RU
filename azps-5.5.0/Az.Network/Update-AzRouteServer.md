---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
ms.openlocfilehash: 9f00ccfb01cd6e6b0d80b120364f8ac0c81daae0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218196"
---
# <span data-ttu-id="9cdb7-101">Update-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="9cdb7-101">Update-AzRouteServer</span></span>

## <span data-ttu-id="9cdb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cdb7-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdb7-103">Обновив Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-103">Update an Azure RouteServer.</span></span>

## <span data-ttu-id="9cdb7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9cdb7-104">SYNTAX</span></span>

### <span data-ttu-id="9cdb7-105">RouteServerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9cdb7-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cdb7-106">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cdb7-106">RouteServerResourceIdParameterSet</span></span>
```
Update-AzRouteServer [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cdb7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cdb7-107">DESCRIPTION</span></span>
<span data-ttu-id="9cdb7-108">При **настройке Update-AzRouteServer** трафик "ветвь-ветвь" переключается на azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-108">The **Update-AzRouteServer** cmdlet switches the branch-to-branch traffic to an Azure RouteServer.</span></span>

## <span data-ttu-id="9cdb7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9cdb7-109">EXAMPLES</span></span>

### <span data-ttu-id="9cdb7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9cdb7-110">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName -AllowBranchToBranchTraffic
```
<span data-ttu-id="9cdb7-111">Чтобы включить ветвь-трафик для сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-111">To enable branch to branch traffic for route server.</span></span>

### <span data-ttu-id="9cdb7-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9cdb7-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName
```
<span data-ttu-id="9cdb7-113">Отключение ветвного трафика для сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-113">To disable branch to branch traffic for route server.</span></span>

## <span data-ttu-id="9cdb7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cdb7-114">PARAMETERS</span></span>

### <span data-ttu-id="9cdb7-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="9cdb7-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="9cdb7-116">Пометить, чтобы разрешить ветвь-трафик для сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-116">Flag to allow branch to branch traffic for route server.</span></span>

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

### <span data-ttu-id="9cdb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdb7-117">-DefaultProfile</span></span>
<span data-ttu-id="9cdb7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cdb7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cdb7-119">-ResourceGroupName</span></span>
<span data-ttu-id="9cdb7-120">Имя группы ресурсов сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-120">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cdb7-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cdb7-121">-ResourceId</span></span>
<span data-ttu-id="9cdb7-122">ResourceId сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-122">ResourceId of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cdb7-123">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="9cdb7-123">-RouteServerName</span></span>
<span data-ttu-id="9cdb7-124">Имя сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-124">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cdb7-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cdb7-125">-Confirm</span></span>
<span data-ttu-id="9cdb7-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cdb7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cdb7-127">-WhatIf</span></span>
<span data-ttu-id="9cdb7-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cdb7-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cdb7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdb7-130">CommonParameters</span></span>
<span data-ttu-id="9cdb7-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cdb7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdb7-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cdb7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdb7-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cdb7-133">INPUTS</span></span>

### <span data-ttu-id="9cdb7-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9cdb7-134">System.String</span></span>

## <span data-ttu-id="9cdb7-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9cdb7-135">OUTPUTS</span></span>

### <span data-ttu-id="9cdb7-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="9cdb7-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="9cdb7-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9cdb7-137">NOTES</span></span>

## <span data-ttu-id="9cdb7-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cdb7-138">RELATED LINKS</span></span>
