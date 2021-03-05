---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 93bc2a622d2bba077b5176c67df4d7894a95d4ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978259"
---
# <span data-ttu-id="77534-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="77534-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="77534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77534-102">SYNOPSIS</span></span>
<span data-ttu-id="77534-103">Создает ресурс VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="77534-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="77534-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="77534-104">SYNTAX</span></span>

### <span data-ttu-id="77534-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77534-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77534-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="77534-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77534-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77534-107">DESCRIPTION</span></span>
<span data-ttu-id="77534-108">Командлет **New-AzVirtualNetworkTap** создает ресурс виртуального сетевого касания Azure.</span><span class="sxs-lookup"><span data-stu-id="77534-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="77534-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="77534-109">EXAMPLES</span></span>

### <span data-ttu-id="77534-110">Пример 1. Создание виртуального касания в сети Azure</span><span class="sxs-lookup"><span data-stu-id="77534-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="77534-111">Эта команда создает виртуальный сетевой касание с именем VirtualNetworkTap1, который имеет сведения о конечной конфигурации VM (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="77534-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="77534-112">Весь исходный трафик, на который настроен трафик VM, будет перенаправлен на этот IP-адрес назначения + порт.</span><span class="sxs-lookup"><span data-stu-id="77534-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="77534-113">Пример 2. Создание виртуального сетевого касания Azure с помощью IP-адреса LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="77534-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="77534-114">Эта команда создает виртуальный сетевой касание с именем VirtualNetworkTap1, который имеет сведения о конечной конфигурации VM (FrontEndIpConfiguration).</span><span class="sxs-lookup"><span data-stu-id="77534-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="77534-115">Весь трафик, касаемыйся источника, настроенного на VM, будет маршрутироваться в эту загрузку LoadBalancer IpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="77534-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="77534-116">Порт назначения по умолчанию — 4789.</span><span class="sxs-lookup"><span data-stu-id="77534-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="77534-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77534-117">PARAMETERS</span></span>

### <span data-ttu-id="77534-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77534-118">-AsJob</span></span>
<span data-ttu-id="77534-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="77534-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77534-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77534-120">-DefaultProfile</span></span>
<span data-ttu-id="77534-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77534-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77534-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="77534-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="77534-123">Ссылка на ресурс конфигурации переднего IP-адреса балансиров нагрузки назначения.</span><span class="sxs-lookup"><span data-stu-id="77534-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77534-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="77534-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="77534-125">Ссылка на ресурс конфигурации переднего IP-адреса балансиров нагрузки назначения.</span><span class="sxs-lookup"><span data-stu-id="77534-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77534-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="77534-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="77534-127">Ссылка на ресурс конфигурации IP-интерфейса конечной сети.</span><span class="sxs-lookup"><span data-stu-id="77534-127">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77534-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="77534-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="77534-129">Ссылка на ресурс конфигурации IP-интерфейса конечной сети.</span><span class="sxs-lookup"><span data-stu-id="77534-129">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77534-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="77534-130">-DestinationPort</span></span>
<span data-ttu-id="77534-131">Порт назначения сборщика пакетов</span><span class="sxs-lookup"><span data-stu-id="77534-131">The Destination Port of the packet collector</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77534-132">-Force</span><span class="sxs-lookup"><span data-stu-id="77534-132">-Force</span></span>
<span data-ttu-id="77534-133">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="77534-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="77534-134">-Location</span><span class="sxs-lookup"><span data-stu-id="77534-134">-Location</span></span>
<span data-ttu-id="77534-135">Расположение.</span><span class="sxs-lookup"><span data-stu-id="77534-135">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77534-136">-Name</span><span class="sxs-lookup"><span data-stu-id="77534-136">-Name</span></span>
<span data-ttu-id="77534-137">Имя касания.</span><span class="sxs-lookup"><span data-stu-id="77534-137">The name of the tap.</span></span>

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

### <span data-ttu-id="77534-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77534-138">-ResourceGroupName</span></span>
<span data-ttu-id="77534-139">Имя группы ресурсов виртуального сетевого касания.</span><span class="sxs-lookup"><span data-stu-id="77534-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="77534-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="77534-140">-Tag</span></span>
<span data-ttu-id="77534-141">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="77534-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="77534-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77534-142">-Confirm</span></span>
<span data-ttu-id="77534-143">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="77534-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77534-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77534-144">-WhatIf</span></span>
<span data-ttu-id="77534-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77534-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77534-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="77534-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77534-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77534-147">CommonParameters</span></span>
<span data-ttu-id="77534-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77534-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77534-149">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77534-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77534-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77534-150">INPUTS</span></span>

### <span data-ttu-id="77534-151">System.String</span><span class="sxs-lookup"><span data-stu-id="77534-151">System.String</span></span>

### <span data-ttu-id="77534-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="77534-152">System.Int32</span></span>

### <span data-ttu-id="77534-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="77534-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="77534-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="77534-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="77534-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="77534-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="77534-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77534-156">OUTPUTS</span></span>

### <span data-ttu-id="77534-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="77534-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="77534-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="77534-158">NOTES</span></span>

## <span data-ttu-id="77534-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77534-159">RELATED LINKS</span></span>

[<span data-ttu-id="77534-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="77534-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="77534-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="77534-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="77534-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="77534-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
