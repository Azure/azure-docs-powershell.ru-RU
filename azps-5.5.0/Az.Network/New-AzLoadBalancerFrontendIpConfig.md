---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 5b5ca651442a0150461da64bb5e33a37167fec3b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213716"
---
# <span data-ttu-id="b4a78-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4a78-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b4a78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4a78-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a78-103">Создает конфигурацию переднего IP-адреса для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b4a78-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="b4a78-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4a78-104">SYNTAX</span></span>

### <span data-ttu-id="b4a78-105">SetByResourceSubnet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4a78-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a78-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="b4a78-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a78-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b4a78-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a78-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b4a78-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a78-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b4a78-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefixId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4a78-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b4a78-110">SetByResourcePublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefix <PSPublicIpPrefix>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4a78-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4a78-111">DESCRIPTION</span></span>
<span data-ttu-id="b4a78-112">**Новый-AzLoadBalancerFrontendIpConfig** создает конфигурацию переднего IP-адреса для балансиров нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="b4a78-112">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="b4a78-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4a78-113">EXAMPLES</span></span>

### <span data-ttu-id="b4a78-114">Пример 1. Создание конфигурации переднего IP-адреса для балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="b4a78-114">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="b4a78-115">Первая команда создает динамический общедоступный IP-адрес MyPublicIP в группе ресурсов MyResourceGroup, а затем сохраняет его в переменной $publicip.</span><span class="sxs-lookup"><span data-stu-id="b4a78-115">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="b4a78-116">Вторая команда создает конфигурацию переднего IP-адреса FrontendIpConfig01, используя общедоступный IP-адрес в $publicip.</span><span class="sxs-lookup"><span data-stu-id="b4a78-116">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

### <span data-ttu-id="b4a78-117">Пример 2. Создание передней конфигурации IP-адреса для балансировки нагрузки с помощью префикса IP-адреса</span><span class="sxs-lookup"><span data-stu-id="b4a78-117">Example 2: Create a front-end IP configuration for a load balancer using ip prefix</span></span>
```
PS C:\> $publicipprefix = New-AzPublicIpPrefix -ResourceGroupName "MyResourceGroup" -name "MyPublicIPPrefix" -location "West US" -Sku Standard -PrefixLength 28
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddressPrefix $publicipprefix
```

<span data-ttu-id="b4a78-118">Первая команда создает общедоступный IP-префикс MyPublicIP длины 28 в группе ресурсов MyResourceGroup, а затем сохраняет его в переменной $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="b4a78-118">The first command creates a public ip prefix named MyPublicIP of length 28 in the resource group named MyResourceGroup, and then stores it in the $publicipprefix variable.</span></span>
<span data-ttu-id="b4a78-119">Вторая команда создает конфигурацию переднего IP-адреса FrontendIpConfig01 с использованием префикса общедоступных IP-адресов в $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="b4a78-119">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP prefix in $publicipprefix.</span></span>

## <span data-ttu-id="b4a78-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4a78-120">PARAMETERS</span></span>

### <span data-ttu-id="b4a78-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a78-121">-DefaultProfile</span></span>
<span data-ttu-id="b4a78-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4a78-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4a78-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b4a78-123">-Name</span></span>
<span data-ttu-id="b4a78-124">Определяет конфигурацию переднего IP-адреса, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4a78-124">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b4a78-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="b4a78-125">-PrivateIpAddress</span></span>
<span data-ttu-id="b4a78-126">Указывает частный IP-адрес балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b4a78-126">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="b4a78-127">Укажите этот параметр только в том случае, если вы указали параметр *Subnet.*</span><span class="sxs-lookup"><span data-stu-id="b4a78-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="b4a78-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b4a78-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="b4a78-129">Версия личных IP-адресов конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="b4a78-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="b4a78-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b4a78-130">-PublicIpAddress</span></span>
<span data-ttu-id="b4a78-131">Указывает объект **PublicIpAddress,** который нужно связать с конфигурацией IP-адреса переднего ip-адреса.</span><span class="sxs-lookup"><span data-stu-id="b4a78-131">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b4a78-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="b4a78-132">-PublicIpAddressId</span></span>
<span data-ttu-id="b4a78-133">Определяет ID объекта **PublicIpAddress,** который нужно связать с конфигурацией IP-адреса переднего.</span><span class="sxs-lookup"><span data-stu-id="b4a78-133">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b4a78-134">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b4a78-134">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="b4a78-135">Указывает объект **PublicIpAddressPrefix,** который нужно связать с конфигурацией IP-адреса переднего.</span><span class="sxs-lookup"><span data-stu-id="b4a78-135">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b4a78-136">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="b4a78-136">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="b4a78-137">Определяет ID объекта **PublicIpAddressPrefix,** который нужно связать с конфигурацией переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="b4a78-137">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b4a78-138">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b4a78-138">-Subnet</span></span>
<span data-ttu-id="b4a78-139">Объект **подсети,** в котором нужно создать конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="b4a78-139">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b4a78-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b4a78-140">-SubnetId</span></span>
<span data-ttu-id="b4a78-141">Определяет ИД подсети, в которой нужно создать конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="b4a78-141">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b4a78-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="b4a78-142">-Zone</span></span>
<span data-ttu-id="b4a78-143">Список зон доступности, обозначающий IP-адрес, выделенный для ресурса.</span><span class="sxs-lookup"><span data-stu-id="b4a78-143">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="b4a78-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4a78-144">-Confirm</span></span>
<span data-ttu-id="b4a78-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4a78-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4a78-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4a78-146">-WhatIf</span></span>
<span data-ttu-id="b4a78-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4a78-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4a78-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b4a78-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4a78-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a78-149">CommonParameters</span></span>
<span data-ttu-id="b4a78-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4a78-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a78-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4a78-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a78-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4a78-152">INPUTS</span></span>

### <span data-ttu-id="b4a78-153">System.String</span><span class="sxs-lookup"><span data-stu-id="b4a78-153">System.String</span></span>

### <span data-ttu-id="b4a78-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b4a78-154">System.String[]</span></span>

### <span data-ttu-id="b4a78-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b4a78-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="b4a78-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b4a78-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="b4a78-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4a78-157">OUTPUTS</span></span>

### <span data-ttu-id="b4a78-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4a78-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="b4a78-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4a78-159">NOTES</span></span>

## <span data-ttu-id="b4a78-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4a78-160">RELATED LINKS</span></span>

[<span data-ttu-id="b4a78-161">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4a78-161">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b4a78-162">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4a78-162">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b4a78-163">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b4a78-163">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="b4a78-164">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4a78-164">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b4a78-165">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4a78-165">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


