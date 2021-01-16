---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a16b625c4624753943659ba796b169ef338888f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519902"
---
# <span data-ttu-id="ca0c6-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca0c6-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="ca0c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ca0c6-103">Обновляет конфигурацию ПЕРЕДНЕГО IP-адреса для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="ca0c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ca0c6-104">SYNTAX</span></span>

### <span data-ttu-id="ca0c6-105">SetByResourceSubnet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca0c6-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca0c6-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="ca0c6-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca0c6-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca0c6-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca0c6-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca0c6-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca0c6-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ca0c6-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca0c6-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ca0c6-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca0c6-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca0c6-111">DESCRIPTION</span></span>
<span data-ttu-id="ca0c6-112">Для **балансиров нагрузки проектлет Set-AzLoadBalancerFrontendIpConfig** обновляет конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="ca0c6-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ca0c6-113">EXAMPLES</span></span>

### <span data-ttu-id="ca0c6-114">Пример 1. Изменение конфигурации IP-адреса переднего ip-адреса для балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="ca0c6-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="ca0c6-115">Первая команда получает виртуальную подсеть "Подсеть", а затем сохраняет ее в $Subnet переменной.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="ca0c6-116">Вторая команда получает связанный балансиров нагрузки MyLoadBalancer и сохраняет его в переменной $slb загрузки.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="ca0c6-117">Третья команда использует оператор конвейера для передать балансировку нагрузки в $slb в add-AzLoadBalancerFrontendIpConfig, который создает конфигурацию переднего IP-адреса с именем NewFrontend для $slb.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="ca0c6-118">Четвертая команда передает баланс загрузки в $slb **Set-AzLoadBalancerFrontendIpConfig,** который сохраняет и обновляет конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="ca0c6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca0c6-119">PARAMETERS</span></span>

### <span data-ttu-id="ca0c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca0c6-120">-DefaultProfile</span></span>
<span data-ttu-id="ca0c6-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca0c6-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ca0c6-122">-LoadBalancer</span></span>
<span data-ttu-id="ca0c6-123">Определяет балансировую нагрузку.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-123">Specifies a load balancer.</span></span>
<span data-ttu-id="ca0c6-124">Этот cmdlet обновляет переднюю конфигурацию балансира нагрузки, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ca0c6-125">-Name</span></span>
<span data-ttu-id="ca0c6-126">Имя ip-конфигурации переднего ip-адреса, который нужно установить.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="ca0c6-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca0c6-127">-PrivateIpAddress</span></span>
<span data-ttu-id="ca0c6-128">Указывает частный IP-адрес балансира нагрузки, связанного с ip-конфигурацией переднего IP-адреса, которую нужно установить.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="ca0c6-129">Укажите этот параметр только в том случае, если вы указали параметр *Subnet.*</span><span class="sxs-lookup"><span data-stu-id="ca0c6-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="ca0c6-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="ca0c6-131">Версия конфигурации IP-адреса личного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-131">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca0c6-132">-PublicIpAddress</span></span>
<span data-ttu-id="ca0c6-133">Указывает объект **PublicIpAddress,** связанный с ip-конфигурацией переднего ip-адреса, которую нужно установить.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="ca0c6-134">-PublicIpAddressId</span></span>
<span data-ttu-id="ca0c6-135">Задает код объекта **PublicIpAddress,** связанного с ip-конфигурацией переднего ip-адреса, которую задает этот набор cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ca0c6-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="ca0c6-137">Указывает объект **PublicIpAddressPrefix,** который нужно связать с конфигурацией IP-адреса переднего.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="ca0c6-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="ca0c6-139">Определяет ID объекта **PublicIpAddressPrefix,** который нужно связать с конфигурацией переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-140">-Subnet</span><span class="sxs-lookup"><span data-stu-id="ca0c6-140">-Subnet</span></span>
<span data-ttu-id="ca0c6-141">Задает объект **Подсети,** который содержит конфигурацию ip-адреса переднего ip-адреса, которую задает этот набор cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ca0c6-142">-SubnetId</span></span>
<span data-ttu-id="ca0c6-143">Задает код подсети, которая содержит конфигурацию переднего IP-адреса, заданную этим набором cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="ca0c6-144">-Zone</span></span>
<span data-ttu-id="ca0c6-145">Список зон доступности, обозначающий IP-адрес, выделенный для ресурса.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0c6-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca0c6-146">-Confirm</span></span>
<span data-ttu-id="ca0c6-147">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca0c6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca0c6-148">-WhatIf</span></span>
<span data-ttu-id="ca0c6-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca0c6-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca0c6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca0c6-151">CommonParameters</span></span>
<span data-ttu-id="ca0c6-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca0c6-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca0c6-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca0c6-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca0c6-154">INPUTS</span></span>

### <span data-ttu-id="ca0c6-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ca0c6-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="ca0c6-156">System.String</span><span class="sxs-lookup"><span data-stu-id="ca0c6-156">System.String</span></span>

### <span data-ttu-id="ca0c6-157">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ca0c6-157">System.String[]</span></span>

### <span data-ttu-id="ca0c6-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="ca0c6-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="ca0c6-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca0c6-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="ca0c6-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ca0c6-160">OUTPUTS</span></span>

### <span data-ttu-id="ca0c6-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ca0c6-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ca0c6-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ca0c6-162">NOTES</span></span>

## <span data-ttu-id="ca0c6-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca0c6-163">RELATED LINKS</span></span>

[<span data-ttu-id="ca0c6-164">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca0c6-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ca0c6-165">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ca0c6-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ca0c6-166">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca0c6-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ca0c6-167">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ca0c6-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="ca0c6-168">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca0c6-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ca0c6-169">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ca0c6-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


