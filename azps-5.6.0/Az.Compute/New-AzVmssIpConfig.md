---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 30dbe52805017a00f24cc95c832386545ae036e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965043"
---
# <span data-ttu-id="30761-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="30761-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="30761-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30761-102">SYNOPSIS</span></span>
<span data-ttu-id="30761-103">Создает конфигурацию IP-адреса для сетевого интерфейса VMSS.</span><span class="sxs-lookup"><span data-stu-id="30761-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="30761-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="30761-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30761-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30761-105">DESCRIPTION</span></span>
<span data-ttu-id="30761-106">С **помощью cmdlet New-AzVmssIpConfig** создается объект конфигурации IP-адреса для сетевого интерфейса набора виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="30761-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="30761-107">Укажите конфигурацию из этого cmdlet в качестве параметра *IPConfiguration* для Add-AzVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30761-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="30761-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="30761-108">EXAMPLES</span></span>

### <span data-ttu-id="30761-109">Пример 1. Создание объекта конфигурации IP для интерфейса VMSS</span><span class="sxs-lookup"><span data-stu-id="30761-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="30761-110">Эта команда создает объект конфигурации IP-адреса с именем ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="30761-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="30761-111">Для этой команды используется ранее определенный ИД подсети, который хранится в $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="30761-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="30761-112">Команда сохраняет параметры конфигурации в переменной $IPConfiguration для использования с **Add-AzVmssNetworkInterfaceConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="30761-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="30761-113">Пример 2. Создание объекта конфигурации IP-адреса, который содержит параметры пула NAT</span><span class="sxs-lookup"><span data-stu-id="30761-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="30761-114">Эта команда создает объект конфигурации IP-адреса с именем ContosoVmssInterface03, а затем сохраняет его в переменной $IPConfiguration для использования в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="30761-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="30761-115">Для этой команды используется ранее определенный ИД подсети, который хранится в $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="30761-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="30761-116">Команда сохраняет параметры конфигурации в переменной $IPConfiguration для использования в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="30761-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="30761-117">Команда определяет значения параметров *LoadBalancerInboundNatPoolsId* и *LoadBalancerBackendAddressPoolsId.*</span><span class="sxs-lookup"><span data-stu-id="30761-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="30761-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30761-118">PARAMETERS</span></span>

### <span data-ttu-id="30761-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="30761-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="30761-120">Указывает массив ссылок, которые нужно объединить с пулами адресов нагрузки.</span><span class="sxs-lookup"><span data-stu-id="30761-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="30761-121">Такой набор может ссылаться на пул адресов внутреннего и внутреннего пула общедоступных адресов.</span><span class="sxs-lookup"><span data-stu-id="30761-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="30761-122">В нескольких наборах нельзя использовать один и тот же баланс загрузки.</span><span class="sxs-lookup"><span data-stu-id="30761-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="30761-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30761-123">-DefaultProfile</span></span>
<span data-ttu-id="30761-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30761-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30761-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="30761-125">-DnsSetting</span></span>
<span data-ttu-id="30761-126">Параметры DNS, которые будут применяться к общедоступным IP-адресам.</span><span class="sxs-lookup"><span data-stu-id="30761-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="30761-127">Метка доменного имени, которая будет применена к параметрам DNS на общедоступных IP-адресах.</span><span class="sxs-lookup"><span data-stu-id="30761-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="30761-128">Совмещение метки доменного имени и индекса vm будет меткой доменного имени для ресурсов, которые будут созданы для общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="30761-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="30761-129">-Id</span><span class="sxs-lookup"><span data-stu-id="30761-129">-Id</span></span>
<span data-ttu-id="30761-130">Определяет ИД.</span><span class="sxs-lookup"><span data-stu-id="30761-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="30761-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="30761-131">-IpTag</span></span>
<span data-ttu-id="30761-132">Массив объектов IP-тегов.</span><span class="sxs-lookup"><span data-stu-id="30761-132">Specifies an array of Ip Tag objects.</span></span>

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

### <span data-ttu-id="30761-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="30761-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="30761-134">Указывает массив ссылок на пулы сетевых адресов для перевода входящих сетевых адресов (NAT) балансиры нагрузки.</span><span class="sxs-lookup"><span data-stu-id="30761-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="30761-135">Набор масштаба может ссылаться на входящие пулы NAT одного открытого и одного внутреннего балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="30761-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="30761-136">В нескольких наборах нельзя использовать один и тот же баланс загрузки.</span><span class="sxs-lookup"><span data-stu-id="30761-136">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="30761-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="30761-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="30761-138">Указывает массив ссылок на входящие пулы NAT для балансиры нагрузки.</span><span class="sxs-lookup"><span data-stu-id="30761-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="30761-139">Набор масштаба может ссылаться на входящие пулы NAT одного открытого и одного внутреннего балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="30761-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="30761-140">В нескольких наборах нельзя использовать один и тот же баланс загрузки.</span><span class="sxs-lookup"><span data-stu-id="30761-140">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="30761-141">-Name</span><span class="sxs-lookup"><span data-stu-id="30761-141">-Name</span></span>
<span data-ttu-id="30761-142">Указывает имя конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="30761-142">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="30761-143">-Primary</span><span class="sxs-lookup"><span data-stu-id="30761-143">-Primary</span></span>
<span data-ttu-id="30761-144">Указывает основную конфигурацию IP-адреса, если сетевой интерфейс имеет несколько конфигураций IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="30761-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="30761-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="30761-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="30761-146">Укажите конфигурацию IP-адреса для личного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="30761-146">Specify the IP configuration for private IP address.</span></span>  <span data-ttu-id="30761-147">Значение по умолчанию — IPv4.</span><span class="sxs-lookup"><span data-stu-id="30761-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="30761-148">Возможные значения: IPv4 и IPv6.</span><span class="sxs-lookup"><span data-stu-id="30761-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="30761-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="30761-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="30761-150">Время ожидания неавтного времени ожидания для общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="30761-150">The idle timeout of the public IP address.</span></span>

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

### <span data-ttu-id="30761-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="30761-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="30761-152">Имя конфигурации адреса publicIP.</span><span class="sxs-lookup"><span data-stu-id="30761-152">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="30761-153">-PublicIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="30761-153">-PublicIPAddressVersion</span></span>
<span data-ttu-id="30761-154">Укажите конфигурацию IP-адреса для общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="30761-154">Specify the IP configuration for public IP address.</span></span>  <span data-ttu-id="30761-155">Значение по умолчанию — IPv4.</span><span class="sxs-lookup"><span data-stu-id="30761-155">Default is taken as IPv4.</span></span>  <span data-ttu-id="30761-156">Возможные значения: IPv4 и IPv6.</span><span class="sxs-lookup"><span data-stu-id="30761-156">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="30761-157">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="30761-157">-PublicIPPrefix</span></span>
<span data-ttu-id="30761-158">ID of Public IP Prefix (Префикс общего IP-адреса)</span><span class="sxs-lookup"><span data-stu-id="30761-158">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="30761-159">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="30761-159">-SubnetId</span></span>
<span data-ttu-id="30761-160">Определяет ИД подсети, в которой создается сетевой интерфейс VMSS в конфигурации.</span><span class="sxs-lookup"><span data-stu-id="30761-160">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="30761-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30761-161">-Confirm</span></span>
<span data-ttu-id="30761-162">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30761-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30761-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30761-163">-WhatIf</span></span>
<span data-ttu-id="30761-164">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30761-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30761-165">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="30761-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30761-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30761-166">CommonParameters</span></span>
<span data-ttu-id="30761-167">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30761-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30761-168">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30761-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30761-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30761-169">INPUTS</span></span>

### <span data-ttu-id="30761-170">System.String</span><span class="sxs-lookup"><span data-stu-id="30761-170">System.String</span></span>

### <span data-ttu-id="30761-171">System.String[]</span><span class="sxs-lookup"><span data-stu-id="30761-171">System.String[]</span></span>

### <span data-ttu-id="30761-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="30761-172">System.Int32</span></span>

### <span data-ttu-id="30761-173">Microsoft.Azure.Management.Compute.Models.VirtualMa modelseScaleSetIpTag[]</span><span class="sxs-lookup"><span data-stu-id="30761-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="30761-174">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="30761-174">OUTPUTS</span></span>

### <span data-ttu-id="30761-175">Microsoft.Azure.Management.Compute.Models.VirtualMa modelseScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="30761-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="30761-176">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="30761-176">NOTES</span></span>

## <span data-ttu-id="30761-177">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30761-177">RELATED LINKS</span></span>

[<span data-ttu-id="30761-178">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="30761-178">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


