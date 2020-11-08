---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: fa520056b9e1d098271cd726575e8d521d7c27f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236031"
---
# <span data-ttu-id="91dd2-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="91dd2-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="91dd2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="91dd2-103">Создает интерфейсную конфигурацию IP для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="91dd2-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="91dd2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91dd2-104">SYNTAX</span></span>

### <span data-ttu-id="91dd2-105">SetByResourceSubnet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="91dd2-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91dd2-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="91dd2-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91dd2-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="91dd2-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91dd2-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="91dd2-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91dd2-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91dd2-109">DESCRIPTION</span></span>
<span data-ttu-id="91dd2-110">Командлет **New-AzLoadBalancerFrontendIpConfig** создает интерфейсную конфигурацию IP-конфигурации для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="91dd2-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="91dd2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91dd2-111">EXAMPLES</span></span>

### <span data-ttu-id="91dd2-112">Пример 1: создание интерфейса IP-конфигурации для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="91dd2-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="91dd2-113">Первая команда создает динамический публичный IP-адрес с именем MyPublicIP в группе ресурсов с именем MyResourceGroup и сохраняет его в переменной $publicip.</span><span class="sxs-lookup"><span data-stu-id="91dd2-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="91dd2-114">Вторая команда создает клиентскую IP-конфигурацию с именем FrontendIpConfig01, используя общедоступный IP-адрес в $publicip.</span><span class="sxs-lookup"><span data-stu-id="91dd2-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="91dd2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91dd2-115">PARAMETERS</span></span>

### <span data-ttu-id="91dd2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91dd2-116">-DefaultProfile</span></span>
<span data-ttu-id="91dd2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91dd2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91dd2-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="91dd2-118">-Name</span></span>
<span data-ttu-id="91dd2-119">Задает интерфейсную конфигурацию IP-адресов, которую создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="91dd2-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="91dd2-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="91dd2-120">-PrivateIpAddress</span></span>
<span data-ttu-id="91dd2-121">Задает частный IP-адрес для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="91dd2-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="91dd2-122">Указывайте этот параметр только в том случае, если вы также указали параметр *подсети* .</span><span class="sxs-lookup"><span data-stu-id="91dd2-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="91dd2-123">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="91dd2-123">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="91dd2-124">Версия частного IP-адреса конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="91dd2-124">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="91dd2-125">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="91dd2-125">-PublicIpAddress</span></span>
<span data-ttu-id="91dd2-126">Указывает объект **PublicIpAddress** , который нужно связать с интерфейсной конфигурацией IP.</span><span class="sxs-lookup"><span data-stu-id="91dd2-126">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="91dd2-127">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="91dd2-127">-PublicIpAddressId</span></span>
<span data-ttu-id="91dd2-128">Указывает идентификатор объекта **PublicIpAddress** , который нужно связать с интерфейсной конфигурацией IP.</span><span class="sxs-lookup"><span data-stu-id="91dd2-128">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="91dd2-129">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="91dd2-129">-Subnet</span></span>
<span data-ttu-id="91dd2-130">Указывает объект **подсети** , для которого нужно создать интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="91dd2-130">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="91dd2-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="91dd2-131">-SubnetId</span></span>
<span data-ttu-id="91dd2-132">Указывает идентификатор подсети, в которой нужно создать интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="91dd2-132">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="91dd2-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="91dd2-133">-Zone</span></span>
<span data-ttu-id="91dd2-134">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="91dd2-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="91dd2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91dd2-135">-Confirm</span></span>
<span data-ttu-id="91dd2-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="91dd2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91dd2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91dd2-137">-WhatIf</span></span>
<span data-ttu-id="91dd2-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="91dd2-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91dd2-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="91dd2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91dd2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91dd2-140">CommonParameters</span></span>
<span data-ttu-id="91dd2-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91dd2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91dd2-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91dd2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91dd2-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91dd2-143">INPUTS</span></span>

### <span data-ttu-id="91dd2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="91dd2-144">System.String</span></span>

### <span data-ttu-id="91dd2-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="91dd2-145">System.String[]</span></span>

### <span data-ttu-id="91dd2-146">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="91dd2-146">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="91dd2-147">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="91dd2-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="91dd2-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91dd2-148">OUTPUTS</span></span>

### <span data-ttu-id="91dd2-149">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="91dd2-149">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="91dd2-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="91dd2-150">NOTES</span></span>

## <span data-ttu-id="91dd2-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91dd2-151">RELATED LINKS</span></span>

[<span data-ttu-id="91dd2-152">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="91dd2-152">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="91dd2-153">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="91dd2-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="91dd2-154">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="91dd2-154">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="91dd2-155">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="91dd2-155">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="91dd2-156">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="91dd2-156">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


