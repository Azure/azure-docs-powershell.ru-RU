---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
ms.openlocfilehash: 3cb1fe0fb72182e22c4f7653de26f356ecd823ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951619"
---
# <span data-ttu-id="f0fc4-101">Update-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="f0fc4-101">Update-AzRouteServer</span></span>

## <span data-ttu-id="f0fc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="f0fc4-103">Обновив Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-103">Update an Azure RouteServer.</span></span>

## <span data-ttu-id="f0fc4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0fc4-104">SYNTAX</span></span>

### <span data-ttu-id="f0fc4-105">RouteServerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0fc4-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0fc4-106">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0fc4-106">RouteServerResourceIdParameterSet</span></span>
```
Update-AzRouteServer [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0fc4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0fc4-107">DESCRIPTION</span></span>
<span data-ttu-id="f0fc4-108">При **настройке Update-AzRouteServer** трафик "ветвь-ветвь" переключается на azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-108">The **Update-AzRouteServer** cmdlet switches the branch-to-branch traffic to an Azure RouteServer.</span></span>

## <span data-ttu-id="f0fc4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0fc4-109">EXAMPLES</span></span>

### <span data-ttu-id="f0fc4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0fc4-110">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName -AllowBranchToBranchTraffic
```
<span data-ttu-id="f0fc4-111">Чтобы включить ветвь-трафик для сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-111">To enable branch to branch traffic for route server.</span></span>

### <span data-ttu-id="f0fc4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0fc4-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName
```
<span data-ttu-id="f0fc4-113">Отключение ветвного трафика для сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-113">To disable branch to branch traffic for route server.</span></span>

## <span data-ttu-id="f0fc4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0fc4-114">PARAMETERS</span></span>

### <span data-ttu-id="f0fc4-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="f0fc4-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="f0fc4-116">Пометить, чтобы разрешить ветвь-трафик для сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-116">Flag to allow branch to branch traffic for route server.</span></span>

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

### <span data-ttu-id="f0fc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0fc4-117">-DefaultProfile</span></span>
<span data-ttu-id="f0fc4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0fc4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0fc4-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0fc4-120">Имя группы ресурсов сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-120">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="f0fc4-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0fc4-121">-ResourceId</span></span>
<span data-ttu-id="f0fc4-122">ResourceId сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-122">ResourceId of the route server.</span></span>

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

### <span data-ttu-id="f0fc4-123">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="f0fc4-123">-RouteServerName</span></span>
<span data-ttu-id="f0fc4-124">Имя сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-124">The name of the route server.</span></span>

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

### <span data-ttu-id="f0fc4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0fc4-125">-Confirm</span></span>
<span data-ttu-id="f0fc4-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0fc4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0fc4-127">-WhatIf</span></span>
<span data-ttu-id="f0fc4-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0fc4-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0fc4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0fc4-130">CommonParameters</span></span>
<span data-ttu-id="f0fc4-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0fc4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0fc4-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0fc4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0fc4-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0fc4-133">INPUTS</span></span>

### <span data-ttu-id="f0fc4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f0fc4-134">System.String</span></span>

## <span data-ttu-id="f0fc4-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0fc4-135">OUTPUTS</span></span>

### <span data-ttu-id="f0fc4-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="f0fc4-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="f0fc4-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0fc4-137">NOTES</span></span>

## <span data-ttu-id="f0fc4-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0fc4-138">RELATED LINKS</span></span>
