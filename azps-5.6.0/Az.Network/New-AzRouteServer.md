---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
ms.openlocfilehash: 24e53b7f7bfd0f09e93184b2862deed4608af544
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958195"
---
# <span data-ttu-id="a1176-101">New-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="a1176-101">New-AzRouteServer</span></span>

## <span data-ttu-id="a1176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1176-102">SYNOPSIS</span></span>
<span data-ttu-id="a1176-103">Создает azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="a1176-103">Creates an Azure RouteServer.</span></span>

## <span data-ttu-id="a1176-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a1176-104">SYNTAX</span></span>

```
New-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> -HostedSubnet <String>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1176-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1176-105">DESCRIPTION</span></span>
<span data-ttu-id="a1176-106">С **его использованием** создается azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="a1176-106">The **New-AzRouteServer** cmdlet creates an Azure RouteServer</span></span>

## <span data-ttu-id="a1176-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a1176-107">EXAMPLES</span></span>

### <span data-ttu-id="a1176-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a1176-108">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzRouteServer -RouteServerName $routeServerName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="a1176-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1176-109">PARAMETERS</span></span>

### <span data-ttu-id="a1176-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1176-110">-AsJob</span></span>
<span data-ttu-id="a1176-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a1176-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1176-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1176-112">-DefaultProfile</span></span>
<span data-ttu-id="a1176-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1176-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1176-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a1176-114">-Force</span></span>
<span data-ttu-id="a1176-115">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="a1176-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a1176-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="a1176-116">-HostedSubnet</span></span>
<span data-ttu-id="a1176-117">Подсеть, в которой находится сервер маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="a1176-117">The subnet where the route server is hosted.</span></span>

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

### <span data-ttu-id="a1176-118">-Location</span><span class="sxs-lookup"><span data-stu-id="a1176-118">-Location</span></span>
<span data-ttu-id="a1176-119">Расположение.</span><span class="sxs-lookup"><span data-stu-id="a1176-119">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1176-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1176-120">-ResourceGroupName</span></span>
<span data-ttu-id="a1176-121">Имя группы ресурсов сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a1176-121">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1176-122">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="a1176-122">-RouteServerName</span></span>
<span data-ttu-id="a1176-123">Имя сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="a1176-123">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1176-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1176-124">-Tag</span></span>
<span data-ttu-id="a1176-125">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="a1176-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1176-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1176-126">-Confirm</span></span>
<span data-ttu-id="a1176-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a1176-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1176-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1176-128">-WhatIf</span></span>
<span data-ttu-id="a1176-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1176-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1176-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a1176-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1176-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1176-131">CommonParameters</span></span>
<span data-ttu-id="a1176-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1176-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1176-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1176-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1176-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1176-134">INPUTS</span></span>

### <span data-ttu-id="a1176-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a1176-135">System.String</span></span>

### <span data-ttu-id="a1176-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a1176-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a1176-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1176-137">OUTPUTS</span></span>

### <span data-ttu-id="a1176-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="a1176-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="a1176-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a1176-139">NOTES</span></span>

## <span data-ttu-id="a1176-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1176-140">RELATED LINKS</span></span>
