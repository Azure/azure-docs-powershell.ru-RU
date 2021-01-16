---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 3c3cc0e5da1cc8afbc6160acf13c3ef94eb02e34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506910"
---
# <span data-ttu-id="4f6c5-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="4f6c5-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="4f6c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="4f6c5-103">Возвращает config адреса для возврата балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="4f6c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4f6c5-104">SYNTAX</span></span>

### <span data-ttu-id="4f6c5-105">SetByResourcePublicIpAddress (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4f6c5-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f6c5-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f6c5-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f6c5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f6c5-107">DESCRIPTION</span></span>
<span data-ttu-id="4f6c5-108">Возвращает config адреса для возврата балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="4f6c5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4f6c5-109">EXAMPLES</span></span>

### <span data-ttu-id="4f6c5-110">Пример 1. Новый адресный адрес для загрузки с виртуальной ссылкой на сеть</span><span class="sxs-lookup"><span data-stu-id="4f6c5-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="4f6c5-111">Пример 2. Новый адрес для загрузки с ссылкой на конфигурацию переднего IP-адреса loadbalancer</span><span class="sxs-lookup"><span data-stu-id="4f6c5-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="4f6c5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f6c5-112">PARAMETERS</span></span>

### <span data-ttu-id="4f6c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f6c5-113">-DefaultProfile</span></span>
<span data-ttu-id="4f6c5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f6c5-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="4f6c5-115">-IpAddress</span></span>
<span data-ttu-id="4f6c5-116">IPAddress, который нужно добавить в пул backend</span><span class="sxs-lookup"><span data-stu-id="4f6c5-116">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f6c5-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4f6c5-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="4f6c5-118">Конфигурация переднего ip-адреса балансира нагрузки, связанная с конфигурацией backend Address config</span><span class="sxs-lookup"><span data-stu-id="4f6c5-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceFrontendIPConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f6c5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4f6c5-119">-Name</span></span>
<span data-ttu-id="4f6c5-120">Имя confend Address config</span><span class="sxs-lookup"><span data-stu-id="4f6c5-120">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="4f6c5-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="4f6c5-121">-VirtualNetworkId</span></span>
<span data-ttu-id="4f6c5-122">Виртуальная сеть, связанная с confend Address config</span><span class="sxs-lookup"><span data-stu-id="4f6c5-122">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f6c5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f6c5-123">-Confirm</span></span>
<span data-ttu-id="4f6c5-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f6c5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f6c5-125">-WhatIf</span></span>
<span data-ttu-id="4f6c5-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f6c5-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f6c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f6c5-128">CommonParameters</span></span>
<span data-ttu-id="4f6c5-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f6c5-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f6c5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f6c5-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f6c5-131">INPUTS</span></span>

### <span data-ttu-id="4f6c5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4f6c5-132">System.String</span></span>

### <span data-ttu-id="4f6c5-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f6c5-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4f6c5-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4f6c5-134">OUTPUTS</span></span>

### <span data-ttu-id="4f6c5-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="4f6c5-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="4f6c5-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4f6c5-136">NOTES</span></span>

## <span data-ttu-id="4f6c5-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f6c5-137">RELATED LINKS</span></span>