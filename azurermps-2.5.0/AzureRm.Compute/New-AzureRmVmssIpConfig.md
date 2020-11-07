---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssipconfig
schema: 2.0.0
ms.openlocfilehash: 82c27b6f8f926d273948bdfcb519a10ee1e0a3c7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914570"
---
# <span data-ttu-id="6cfcf-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="6cfcf-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="6cfcf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6cfcf-102">SYNOPSIS</span></span>
<span data-ttu-id="6cfcf-103">Создание IP-конфигурации для сетевого интерфейса VMSS.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cfcf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6cfcf-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cfcf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cfcf-105">DESCRIPTION</span></span>
<span data-ttu-id="6cfcf-106">Командлет **New-AzureRmVmssIpConfig** создает объект конфигурации IP для сетевого интерфейса набора масштабирования виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="6cfcf-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="6cfcf-107">Укажите конфигурацию из этого командлета в качестве параметра *IP* для командлета Add-AzureRmVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="6cfcf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6cfcf-108">EXAMPLES</span></span>

### <span data-ttu-id="6cfcf-109">Пример 1: создание объекта конфигурации IP для интерфейса VMSS</span><span class="sxs-lookup"><span data-stu-id="6cfcf-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="6cfcf-110">Эта команда создает объект конфигурации IP с именем ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="6cfcf-111">В команде используется ранее определенный идентификатор подсети, хранящийся в $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="6cfcf-112">Команда сохраняет параметры конфигурации в переменной $IPConfiguration для последующего использования с помощью **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="6cfcf-113">Пример 2: создание объекта конфигурации IP, включающего параметры пула NAT</span><span class="sxs-lookup"><span data-stu-id="6cfcf-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="6cfcf-114">Эта команда создает объект конфигурации IP с именем ContosoVmssInterface03 и сохраняет его в переменной $IPConfiguration для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="6cfcf-115">В команде используется ранее определенный идентификатор подсети, хранящийся в $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="6cfcf-116">Команда сохраняет параметры конфигурации в переменной $IPConfiguration для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="6cfcf-117">Команда задает значения для параметров *LoadBalancerInboundNatPoolsId* и *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="6cfcf-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="6cfcf-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6cfcf-118">PARAMETERS</span></span>

### <span data-ttu-id="6cfcf-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="6cfcf-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="6cfcf-120">Указывает массив ссылок на серверные пулы адресных пулов подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="6cfcf-121">Набор масштабов может ссылаться на пулы серверных адресов одного открытого и одного внутреннего подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="6cfcf-122">Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="6cfcf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cfcf-123">-DefaultProfile</span></span>
<span data-ttu-id="6cfcf-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cfcf-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="6cfcf-125">-DnsSetting</span></span>
<span data-ttu-id="6cfcf-126">Параметры DNS, применяемые к адресам publicIP.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="6cfcf-127">Метка доменного имени параметров DNS, которые будут применяться к publicIP адресам.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="6cfcf-128">Объединение метки доменного имени и индекса ВМ — это метки доменных имен ресурсов общедоступного IP-адреса, которые будут созданы.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cfcf-129">-ID</span><span class="sxs-lookup"><span data-stu-id="6cfcf-129">-Id</span></span>
<span data-ttu-id="6cfcf-130">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="6cfcf-131">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="6cfcf-131">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="6cfcf-132">Задает массив ссылок на пулы NAT для подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-132">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="6cfcf-133">Набор масштабов может ссылаться на входящие пулы NAT для одной открытой и одной внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-133">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="6cfcf-134">Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-134">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="6cfcf-135">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="6cfcf-135">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="6cfcf-136">Указывает массив ссылок на входящие пулы NAT для подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-136">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="6cfcf-137">Набор масштабов может ссылаться на входящие пулы NAT для одной открытой и одной внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-137">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="6cfcf-138">Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-138">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="6cfcf-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6cfcf-139">-Name</span></span>
<span data-ttu-id="6cfcf-140">Указывает имя конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-140">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="6cfcf-141">-Primary</span><span class="sxs-lookup"><span data-stu-id="6cfcf-141">-Primary</span></span>
<span data-ttu-id="6cfcf-142">Определяет основную конфигурацию IP-адреса в случае, если сетевой интерфейс имеет несколько конфигураций IP.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-142">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cfcf-143">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="6cfcf-143">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="6cfcf-144">Укажите IP-конфигурацию: либо IPv4, либо IPv6.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-144">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="6cfcf-145">По умолчанию используется протокол IPv4.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-145">Default is taken as IPv4.</span></span>  <span data-ttu-id="6cfcf-146">Возможные значения: "IPv4" и "IPv6".</span><span class="sxs-lookup"><span data-stu-id="6cfcf-146">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="6cfcf-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6cfcf-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="6cfcf-148">Таймаут простоя общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-148">The idle timeout of the public IP address.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cfcf-149">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6cfcf-149">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="6cfcf-150">Имя конфигурации адреса publicIP.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-150">The publicIP address configuration name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cfcf-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6cfcf-151">-SubnetId</span></span>
<span data-ttu-id="6cfcf-152">Указывает идентификатор подсети, в котором конфигурация создает сетевой интерфейс VMSS.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-152">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="6cfcf-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6cfcf-153">-Confirm</span></span>
<span data-ttu-id="6cfcf-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cfcf-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cfcf-155">-WhatIf</span></span>
<span data-ttu-id="6cfcf-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cfcf-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cfcf-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cfcf-158">CommonParameters</span></span>
<span data-ttu-id="6cfcf-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cfcf-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cfcf-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cfcf-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6cfcf-161">INPUTS</span></span>

### <span data-ttu-id="6cfcf-162">Ничего</span><span class="sxs-lookup"><span data-stu-id="6cfcf-162">None</span></span>
<span data-ttu-id="6cfcf-163">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6cfcf-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6cfcf-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cfcf-164">OUTPUTS</span></span>

### <span data-ttu-id="6cfcf-165">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cfcf-165">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="6cfcf-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="6cfcf-166">NOTES</span></span>

## <span data-ttu-id="6cfcf-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cfcf-167">RELATED LINKS</span></span>

[<span data-ttu-id="6cfcf-168">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6cfcf-168">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


