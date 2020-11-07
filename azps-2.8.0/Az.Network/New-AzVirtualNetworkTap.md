---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 11939edc15d49614d2a1fd1692825cd07cd82b2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902057"
---
# <span data-ttu-id="6a78a-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a78a-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="6a78a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a78a-102">SYNOPSIS</span></span>
<span data-ttu-id="6a78a-103">Создает ресурс VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="6a78a-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="6a78a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a78a-104">SYNTAX</span></span>

### <span data-ttu-id="6a78a-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6a78a-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a78a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a78a-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a78a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a78a-107">DESCRIPTION</span></span>
<span data-ttu-id="6a78a-108">Командлет **New-AzVirtualNetworkTap** создает ресурс TAP виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="6a78a-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="6a78a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a78a-109">EXAMPLES</span></span>

### <span data-ttu-id="6a78a-110">Пример 1: создание виртуальной сети в меню "Пуск" Azure</span><span class="sxs-lookup"><span data-stu-id="6a78a-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="6a78a-111">Эта команда создает объект TAP для виртуальной сети с именем "VirtualNetworkTap1", который содержит сведения о конфигурации целевой виртуальной машины (DestinationIpConfiguration, DestinationPort).</span><span class="sxs-lookup"><span data-stu-id="6a78a-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="6a78a-112">Весь трафик настроенной виртуальной машины для исходного пункта будет перенаправляться на этот конечный IP-порт.</span><span class="sxs-lookup"><span data-stu-id="6a78a-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="6a78a-113">Пример 2: Создание связи виртуальной сети Azure с помощью IP-адреса подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="6a78a-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="6a78a-114">Эта команда создает объект TAP для виртуальной сети с именем "VirtualNetworkTap1", который содержит сведения о конфигурации целевой виртуальной машины (FrontEndIpConfiguration).</span><span class="sxs-lookup"><span data-stu-id="6a78a-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="6a78a-115">Весь трафик настроенной виртуальной машины для исходного пункта будет перенаправляться в эту конфигурацию подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6a78a-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="6a78a-116">Порт назначения по умолчанию — 4789.</span><span class="sxs-lookup"><span data-stu-id="6a78a-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="6a78a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a78a-117">PARAMETERS</span></span>

### <span data-ttu-id="6a78a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a78a-118">-AsJob</span></span>
<span data-ttu-id="6a78a-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6a78a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a78a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a78a-120">-DefaultProfile</span></span>
<span data-ttu-id="6a78a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a78a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a78a-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a78a-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="6a78a-123">Ссылка на серверный ресурс целевой подсистемы балансировки нагрузки IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6a78a-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="6a78a-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6a78a-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="6a78a-125">Ссылка на серверный ресурс целевой подсистемы балансировки нагрузки IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6a78a-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="6a78a-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a78a-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="6a78a-127">Ссылка на ресурс IP-конфигурации конечного сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6a78a-127">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="6a78a-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6a78a-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="6a78a-129">Ссылка на ресурс IP-конфигурации конечного сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6a78a-129">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="6a78a-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6a78a-130">-DestinationPort</span></span>
<span data-ttu-id="6a78a-131">Порт назначения сборщика пакетов</span><span class="sxs-lookup"><span data-stu-id="6a78a-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="6a78a-132">-Force</span><span class="sxs-lookup"><span data-stu-id="6a78a-132">-Force</span></span>
<span data-ttu-id="6a78a-133">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="6a78a-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6a78a-134">-Location</span><span class="sxs-lookup"><span data-stu-id="6a78a-134">-Location</span></span>
<span data-ttu-id="6a78a-135">Расположение.</span><span class="sxs-lookup"><span data-stu-id="6a78a-135">The location.</span></span>

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

### <span data-ttu-id="6a78a-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6a78a-136">-Name</span></span>
<span data-ttu-id="6a78a-137">Имя TAP.</span><span class="sxs-lookup"><span data-stu-id="6a78a-137">The name of the tap.</span></span>

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

### <span data-ttu-id="6a78a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a78a-138">-ResourceGroupName</span></span>
<span data-ttu-id="6a78a-139">Имя группы ресурсов, в которой будет нажата виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="6a78a-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="6a78a-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="6a78a-140">-Tag</span></span>
<span data-ttu-id="6a78a-141">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a78a-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6a78a-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a78a-142">-Confirm</span></span>
<span data-ttu-id="6a78a-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6a78a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a78a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a78a-144">-WhatIf</span></span>
<span data-ttu-id="6a78a-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6a78a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a78a-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6a78a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a78a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a78a-147">CommonParameters</span></span>
<span data-ttu-id="6a78a-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a78a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a78a-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a78a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a78a-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a78a-150">INPUTS</span></span>

### <span data-ttu-id="6a78a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="6a78a-151">System.String</span></span>

### <span data-ttu-id="6a78a-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6a78a-152">System.Int32</span></span>

### <span data-ttu-id="6a78a-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6a78a-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6a78a-154">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a78a-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="6a78a-155">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a78a-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="6a78a-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a78a-156">OUTPUTS</span></span>

### <span data-ttu-id="6a78a-157">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a78a-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="6a78a-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a78a-158">NOTES</span></span>

## <span data-ttu-id="6a78a-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a78a-159">RELATED LINKS</span></span>

[<span data-ttu-id="6a78a-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a78a-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="6a78a-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a78a-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="6a78a-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a78a-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
