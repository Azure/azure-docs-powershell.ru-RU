---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: ef9121f0962cc5ba06aa9c040d4647a1365fdf80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963912"
---
# <span data-ttu-id="f235d-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f235d-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="f235d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f235d-102">SYNOPSIS</span></span>
<span data-ttu-id="f235d-103">Обновляет конфигурацию ip-адреса переднего ip-адреса для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f235d-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="f235d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f235d-104">SYNTAX</span></span>

### <span data-ttu-id="f235d-105">SetByResourceSubnet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f235d-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f235d-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="f235d-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f235d-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f235d-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f235d-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f235d-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f235d-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f235d-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f235d-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f235d-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f235d-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f235d-111">DESCRIPTION</span></span>
<span data-ttu-id="f235d-112">Для **балансиров нагрузки проектлет Set-AzLoadBalancerFrontendIpConfig** обновляет конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="f235d-112">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="f235d-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f235d-113">EXAMPLES</span></span>

### <span data-ttu-id="f235d-114">Пример 1. Изменение конфигурации IP-адреса переднего ip-адреса для балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="f235d-114">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```powershell
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="f235d-115">Первая команда получает виртуальную подсеть "Подсеть", а затем сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="f235d-115">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="f235d-116">Вторая команда получает связанный баланс нагрузки MyLoadBalancer и сохраняет его в переменной $slb загрузки.</span><span class="sxs-lookup"><span data-stu-id="f235d-116">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="f235d-117">Третья команда использует оператор конвейера для передать балансировку нагрузки в $slb в add-AzLoadBalancerFrontendIpConfig, который создает конфигурацию переднего IP-адреса с именем NewFrontend для $slb.</span><span class="sxs-lookup"><span data-stu-id="f235d-117">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="f235d-118">Четвертая команда передает баланс загрузки в $slb **Set-AzLoadBalancerFrontendIpConfig,** который сохраняет и обновляет конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="f235d-118">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig**, which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="f235d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f235d-119">PARAMETERS</span></span>

### <span data-ttu-id="f235d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f235d-120">-DefaultProfile</span></span>
<span data-ttu-id="f235d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f235d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f235d-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f235d-122">-LoadBalancer</span></span>
<span data-ttu-id="f235d-123">Определяет балансировую нагрузку.</span><span class="sxs-lookup"><span data-stu-id="f235d-123">Specifies a load balancer.</span></span>
<span data-ttu-id="f235d-124">Этот cmdlet обновляет переднюю конфигурацию балансира нагрузки, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="f235d-124">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f235d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f235d-125">-Name</span></span>
<span data-ttu-id="f235d-126">Указывает имя ip-конфигурации переднего ip-адреса, который нужно установить.</span><span class="sxs-lookup"><span data-stu-id="f235d-126">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="f235d-127">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f235d-127">-PrivateIpAddress</span></span>
<span data-ttu-id="f235d-128">Указывает частный IP-адрес балансира нагрузки, связанного с ip-конфигурацией переднего ip-адреса, которую нужно установить.</span><span class="sxs-lookup"><span data-stu-id="f235d-128">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="f235d-129">Укажите этот параметр только в том случае, если вы указали параметр *Subnet.*</span><span class="sxs-lookup"><span data-stu-id="f235d-129">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="f235d-130">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f235d-130">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="f235d-131">Версия личных IP-адресов конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="f235d-131">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="f235d-132">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f235d-132">-PublicIpAddress</span></span>
<span data-ttu-id="f235d-133">Указывает объект **PublicIpAddress,** связанный с ip-конфигурацией переднего ip-адреса, которую нужно установить.</span><span class="sxs-lookup"><span data-stu-id="f235d-133">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="f235d-134">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f235d-134">-PublicIpAddressId</span></span>
<span data-ttu-id="f235d-135">Задает код объекта **PublicIpAddress,** связанного с ip-конфигурацией переднего ip-адреса, которую задает этот набор cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f235d-135">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f235d-136">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f235d-136">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="f235d-137">Указывает объект **PublicIpAddressPrefix,** который нужно связать с конфигурацией IP-адреса переднего.</span><span class="sxs-lookup"><span data-stu-id="f235d-137">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f235d-138">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="f235d-138">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="f235d-139">Определяет ID объекта **PublicIpAddressPrefix,** который нужно связать с конфигурацией переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="f235d-139">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="f235d-140">-Subnet</span><span class="sxs-lookup"><span data-stu-id="f235d-140">-Subnet</span></span>
<span data-ttu-id="f235d-141">Задает объект **Подсети,** который содержит конфигурацию ip-адреса переднего ip-адреса, которую задает этот набор cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f235d-141">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f235d-142">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f235d-142">-SubnetId</span></span>
<span data-ttu-id="f235d-143">Задает код подсети, которая содержит конфигурацию переднего IP-адреса, заданную этим набором cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f235d-143">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="f235d-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="f235d-144">-Zone</span></span>
<span data-ttu-id="f235d-145">Список зон доступности, обозначающий IP-адрес, выделенный для ресурса.</span><span class="sxs-lookup"><span data-stu-id="f235d-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f235d-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f235d-146">-Confirm</span></span>
<span data-ttu-id="f235d-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f235d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f235d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f235d-148">-WhatIf</span></span>
<span data-ttu-id="f235d-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f235d-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f235d-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f235d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f235d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f235d-151">CommonParameters</span></span>
<span data-ttu-id="f235d-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f235d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f235d-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f235d-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f235d-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f235d-154">INPUTS</span></span>

### <span data-ttu-id="f235d-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f235d-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f235d-156">System.String</span><span class="sxs-lookup"><span data-stu-id="f235d-156">System.String</span></span>

### <span data-ttu-id="f235d-157">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f235d-157">System.String[]</span></span>

### <span data-ttu-id="f235d-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f235d-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="f235d-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f235d-159">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f235d-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f235d-160">OUTPUTS</span></span>

### <span data-ttu-id="f235d-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f235d-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f235d-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f235d-162">NOTES</span></span>

## <span data-ttu-id="f235d-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f235d-163">RELATED LINKS</span></span>

[<span data-ttu-id="f235d-164">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f235d-164">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f235d-165">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f235d-165">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f235d-166">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f235d-166">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f235d-167">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f235d-167">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f235d-168">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f235d-168">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="f235d-169">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f235d-169">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


