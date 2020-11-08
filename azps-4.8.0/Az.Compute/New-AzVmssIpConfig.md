---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243110"
---
# <span data-ttu-id="e75b2-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="e75b2-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="e75b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e75b2-102">SYNOPSIS</span></span>
<span data-ttu-id="e75b2-103">Создание IP-конфигурации для сетевого интерфейса VMSS.</span><span class="sxs-lookup"><span data-stu-id="e75b2-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="e75b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e75b2-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e75b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e75b2-105">DESCRIPTION</span></span>
<span data-ttu-id="e75b2-106">Командлет **New-AzVmssIpConfig** создает объект конфигурации IP для сетевого интерфейса набора масштабирования виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e75b2-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e75b2-107">Укажите конфигурацию из этого командлета в качестве параметра *IP* для командлета Add-AzVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e75b2-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="e75b2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e75b2-108">EXAMPLES</span></span>

### <span data-ttu-id="e75b2-109">Пример 1: создание объекта конфигурации IP для интерфейса VMSS</span><span class="sxs-lookup"><span data-stu-id="e75b2-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="e75b2-110">Эта команда создает объект конфигурации IP с именем ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="e75b2-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="e75b2-111">В команде используется ранее определенный идентификатор подсети, хранящийся в $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="e75b2-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="e75b2-112">Команда сохраняет параметры конфигурации в переменной $IPConfiguration для последующего использования с помощью **Add-AzVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e75b2-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="e75b2-113">Пример 2: создание объекта конфигурации IP, включающего параметры пула NAT</span><span class="sxs-lookup"><span data-stu-id="e75b2-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="e75b2-114">Эта команда создает объект конфигурации IP с именем ContosoVmssInterface03 и сохраняет его в переменной $IPConfiguration для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="e75b2-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="e75b2-115">В команде используется ранее определенный идентификатор подсети, хранящийся в $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="e75b2-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="e75b2-116">Команда сохраняет параметры конфигурации в переменной $IPConfiguration для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="e75b2-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="e75b2-117">Команда задает значения для параметров *LoadBalancerInboundNatPoolsId* и *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="e75b2-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="e75b2-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e75b2-118">PARAMETERS</span></span>

### <span data-ttu-id="e75b2-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="e75b2-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="e75b2-120">Указывает массив ссылок на серверные пулы адресных пулов подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e75b2-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="e75b2-121">Набор масштабов может ссылаться на пулы серверных адресов одного открытого и одного внутреннего подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e75b2-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="e75b2-122">Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e75b2-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e75b2-123">-DefaultProfile</span></span>
<span data-ttu-id="e75b2-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e75b2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e75b2-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="e75b2-125">-DnsSetting</span></span>
<span data-ttu-id="e75b2-126">Параметры DNS, применяемые к адресам publicIP.</span><span class="sxs-lookup"><span data-stu-id="e75b2-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="e75b2-127">Метка доменного имени параметров DNS, которые будут применяться к publicIP адресам.</span><span class="sxs-lookup"><span data-stu-id="e75b2-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="e75b2-128">Объединение метки доменного имени и индекса ВМ — это метки доменных имен ресурсов общедоступного IP-адреса, которые будут созданы.</span><span class="sxs-lookup"><span data-stu-id="e75b2-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b2-129">-ID</span><span class="sxs-lookup"><span data-stu-id="e75b2-129">-Id</span></span>
<span data-ttu-id="e75b2-130">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="e75b2-130">Specifies an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b2-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="e75b2-131">-IpTag</span></span>
<span data-ttu-id="e75b2-132">Указывает массив объектов IP-тегов.</span><span class="sxs-lookup"><span data-stu-id="e75b2-132">Specifies an array of Ip Tag objects.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b2-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="e75b2-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="e75b2-134">Задает массив ссылок на пулы NAT для подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e75b2-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="e75b2-135">Набор масштабов может ссылаться на входящие пулы NAT для одной открытой и одной внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e75b2-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="e75b2-136">Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e75b2-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b2-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="e75b2-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="e75b2-138">Указывает массив ссылок на входящие пулы NAT для подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e75b2-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="e75b2-139">Набор масштабов может ссылаться на входящие пулы NAT для одной открытой и одной внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e75b2-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="e75b2-140">Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e75b2-140">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b2-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e75b2-141">-Name</span></span>
<span data-ttu-id="e75b2-142">Указывает имя конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="e75b2-142">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b2-143">-Primary</span><span class="sxs-lookup"><span data-stu-id="e75b2-143">-Primary</span></span>
<span data-ttu-id="e75b2-144">Определяет основную конфигурацию IP-адреса в случае, если сетевой интерфейс имеет несколько конфигураций IP.</span><span class="sxs-lookup"><span data-stu-id="e75b2-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="e75b2-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e75b2-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="e75b2-146">Укажите IP-конфигурацию для частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e75b2-146">Specify the IP configuration for private IP address.</span></span>  <span data-ttu-id="e75b2-147">По умолчанию используется протокол IPv4.</span><span class="sxs-lookup"><span data-stu-id="e75b2-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="e75b2-148">Возможные значения: "IPv4" и "IPv6".</span><span class="sxs-lookup"><span data-stu-id="e75b2-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="e75b2-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e75b2-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="e75b2-150">Таймаут простоя общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e75b2-150">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b2-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e75b2-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="e75b2-152">Имя конфигурации адреса publicIP.</span><span class="sxs-lookup"><span data-stu-id="e75b2-152">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b2-153">-PublicIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e75b2-153">-PublicIPAddressVersion</span></span>
<span data-ttu-id="e75b2-154">Укажите IP-конфигурацию для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e75b2-154">Specify the IP configuration for public IP address.</span></span>  <span data-ttu-id="e75b2-155">По умолчанию используется протокол IPv4.</span><span class="sxs-lookup"><span data-stu-id="e75b2-155">Default is taken as IPv4.</span></span>  <span data-ttu-id="e75b2-156">Возможные значения: "IPv4" и "IPv6".</span><span class="sxs-lookup"><span data-stu-id="e75b2-156">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="e75b2-157">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="e75b2-157">-PublicIPPrefix</span></span>
<span data-ttu-id="e75b2-158">Идентификатор префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="e75b2-158">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="e75b2-159">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e75b2-159">-SubnetId</span></span>
<span data-ttu-id="e75b2-160">Указывает идентификатор подсети, в котором конфигурация создает сетевой интерфейс VMSS.</span><span class="sxs-lookup"><span data-stu-id="e75b2-160">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b2-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e75b2-161">-Confirm</span></span>
<span data-ttu-id="e75b2-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e75b2-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e75b2-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e75b2-163">-WhatIf</span></span>
<span data-ttu-id="e75b2-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e75b2-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e75b2-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e75b2-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e75b2-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e75b2-166">CommonParameters</span></span>
<span data-ttu-id="e75b2-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e75b2-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e75b2-168">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e75b2-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e75b2-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e75b2-169">INPUTS</span></span>

### <span data-ttu-id="e75b2-170">System. String</span><span class="sxs-lookup"><span data-stu-id="e75b2-170">System.String</span></span>

### <span data-ttu-id="e75b2-171">System. String []</span><span class="sxs-lookup"><span data-stu-id="e75b2-171">System.String[]</span></span>

### <span data-ttu-id="e75b2-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e75b2-172">System.Int32</span></span>

### <span data-ttu-id="e75b2-173">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIpTag []</span><span class="sxs-lookup"><span data-stu-id="e75b2-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="e75b2-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e75b2-174">OUTPUTS</span></span>

### <span data-ttu-id="e75b2-175">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e75b2-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="e75b2-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="e75b2-176">NOTES</span></span>

## <span data-ttu-id="e75b2-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e75b2-177">RELATED LINKS</span></span>

[<span data-ttu-id="e75b2-178">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e75b2-178">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


