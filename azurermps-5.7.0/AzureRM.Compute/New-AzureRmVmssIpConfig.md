---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 448f6236f5c9545ff1a1194c8103463f78a8fefd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563680"
---
# <span data-ttu-id="f9d5a-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="f9d5a-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="f9d5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d5a-103">Создание IP-конфигурации для сетевого интерфейса VMSS.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9d5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9d5a-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9d5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9d5a-105">DESCRIPTION</span></span>
<span data-ttu-id="f9d5a-106">Командлет **New-AzureRmVmssIpConfig** создает объект конфигурации IP для сетевого интерфейса набора масштабирования виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f9d5a-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f9d5a-107">Укажите конфигурацию из этого командлета в качестве параметра *IP* для командлета Add-AzureRmVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="f9d5a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9d5a-108">EXAMPLES</span></span>

### <span data-ttu-id="f9d5a-109">Пример 1: создание объекта конфигурации IP для интерфейса VMSS</span><span class="sxs-lookup"><span data-stu-id="f9d5a-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="f9d5a-110">Эта команда создает объект конфигурации IP с именем ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="f9d5a-111">В команде используется ранее определенный идентификатор подсети, хранящийся в $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="f9d5a-112">Команда сохраняет параметры конфигурации в переменной $IPConfiguration для последующего использования с помощью **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="f9d5a-113">Пример 2: создание объекта конфигурации IP, включающего параметры пула NAT</span><span class="sxs-lookup"><span data-stu-id="f9d5a-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="f9d5a-114">Эта команда создает объект конфигурации IP с именем ContosoVmssInterface03 и сохраняет его в переменной $IPConfiguration для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="f9d5a-115">В команде используется ранее определенный идентификатор подсети, хранящийся в $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="f9d5a-116">Команда сохраняет параметры конфигурации в переменной $IPConfiguration для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="f9d5a-117">Команда задает значения для параметров *LoadBalancerInboundNatPoolsId* и *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="f9d5a-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="f9d5a-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9d5a-118">PARAMETERS</span></span>

### <span data-ttu-id="f9d5a-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="f9d5a-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="f9d5a-120">Указывает массив ссылок на серверные пулы адресных пулов подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="f9d5a-121">Набор масштабов может ссылаться на пулы серверных адресов одного открытого и одного внутреннего подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="f9d5a-122">Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5a-123">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="f9d5a-123">-DnsSetting</span></span>
<span data-ttu-id="f9d5a-124">Параметры DNS, применяемые к адресам publicIP.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-124">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="f9d5a-125">Метка доменного имени параметров DNS, которые будут применяться к publicIP адресам.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-125">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="f9d5a-126">Объединение метки доменного имени и индекса ВМ — это метки доменных имен ресурсов общедоступного IP-адреса, которые будут созданы.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-126">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5a-127">-ID</span><span class="sxs-lookup"><span data-stu-id="f9d5a-127">-Id</span></span>
<span data-ttu-id="f9d5a-128">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-128">Specifies an ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5a-129">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="f9d5a-129">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="f9d5a-130">Задает массив ссылок на пулы NAT для подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-130">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="f9d5a-131">Набор масштабов может ссылаться на входящие пулы NAT для одной открытой и одной внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-131">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="f9d5a-132">Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-132">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5a-133">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="f9d5a-133">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="f9d5a-134">Указывает массив ссылок на входящие пулы NAT для подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-134">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="f9d5a-135">Набор масштабов может ссылаться на входящие пулы NAT для одной открытой и одной внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="f9d5a-136">Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5a-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f9d5a-137">-Name</span></span>
<span data-ttu-id="f9d5a-138">Указывает имя конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-138">Specifies the name of the IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5a-139">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f9d5a-139">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="f9d5a-140">Укажите IP-конфигурацию: либо IPv4, либо IPv6.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-140">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="f9d5a-141">По умолчанию используется протокол IPv4.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-141">Default is taken as IPv4.</span></span>  <span data-ttu-id="f9d5a-142">Возможные значения: "IPv4" и "IPv6".</span><span class="sxs-lookup"><span data-stu-id="f9d5a-142">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5a-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f9d5a-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="f9d5a-144">Таймаут простоя общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-144">The idle timeout of the public IP address.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5a-145">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f9d5a-145">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="f9d5a-146">Имя конфигурации адреса publicIP.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-146">The publicIP address configuration name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5a-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f9d5a-147">-SubnetId</span></span>
<span data-ttu-id="f9d5a-148">Указывает идентификатор подсети, в котором конфигурация создает сетевой интерфейс VMSS.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-148">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5a-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9d5a-149">-Confirm</span></span>
<span data-ttu-id="f9d5a-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9d5a-151">-WhatIf</span></span>
<span data-ttu-id="f9d5a-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9d5a-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d5a-154">CommonParameters</span></span>
<span data-ttu-id="f9d5a-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d5a-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9d5a-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d5a-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9d5a-157">INPUTS</span></span>

### <span data-ttu-id="f9d5a-158">Ничего</span><span class="sxs-lookup"><span data-stu-id="f9d5a-158">None</span></span>
<span data-ttu-id="f9d5a-159">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f9d5a-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f9d5a-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9d5a-160">OUTPUTS</span></span>

## <span data-ttu-id="f9d5a-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9d5a-161">NOTES</span></span>

## <span data-ttu-id="f9d5a-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9d5a-162">RELATED LINKS</span></span>

[<span data-ttu-id="f9d5a-163">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9d5a-163">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


