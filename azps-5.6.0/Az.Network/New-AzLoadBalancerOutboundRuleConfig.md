---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 50f3c3a02410adda37b26c88cd5196c4ae232f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971907"
---
# <span data-ttu-id="88f31-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88f31-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="88f31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88f31-102">SYNOPSIS</span></span>
<span data-ttu-id="88f31-103">Создает конфигурацию правил исходящие для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="88f31-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="88f31-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="88f31-104">SYNTAX</span></span>

### <span data-ttu-id="88f31-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88f31-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88f31-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="88f31-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88f31-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88f31-107">DESCRIPTION</span></span>
<span data-ttu-id="88f31-108">**Новый-AzLoadBalancerOutboundRuleConfig** создает конфигурацию правил исходяния для балансиента нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="88f31-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="88f31-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="88f31-109">EXAMPLES</span></span>

### <span data-ttu-id="88f31-110">Пример 1. Создание конфигурации исходящие правила для балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="88f31-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="88f31-111">Первая команда создает общедоступный IP-адрес MyPublicIP в группе ресурсов MyResourceGroup, а затем сохраняет его в переменной $publicip.</span><span class="sxs-lookup"><span data-stu-id="88f31-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="88f31-112">Вторая команда создает конфигурацию переднего IP-адреса с именем FrontendIpConfig01, используя общедоступный IP-адрес в $publicip, а затем сохраняет ее в переменной $frontend.</span><span class="sxs-lookup"><span data-stu-id="88f31-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="88f31-113">Третья команда создает конфигурацию пула адресов с именем BackendAddressPool01 и сохраняет ее в переменной $backend адресов.</span><span class="sxs-lookup"><span data-stu-id="88f31-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="88f31-114">Четвертая команда создает конфигурацию исходящие правил с именем MyOutboundRule, используя объекты переднего и $frontend и $backend.</span><span class="sxs-lookup"><span data-stu-id="88f31-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="88f31-115">Для *создания* конфигурации исходящие правила требуются параметры Protocol (Протокол), *FrontendIPConfiguration (Параметр FrontendIPConfiguration)* и *BackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="88f31-115">The *Protocol*, *FrontendIPConfiguration*, and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="88f31-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="88f31-116">Example 2</span></span>

<span data-ttu-id="88f31-117">Создает конфигурацию правил исходящие для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="88f31-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="88f31-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="88f31-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="88f31-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88f31-119">PARAMETERS</span></span>

### <span data-ttu-id="88f31-120">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="88f31-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="88f31-121">Количество исходящие порты, которые будут использоваться для NAT.</span><span class="sxs-lookup"><span data-stu-id="88f31-121">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="88f31-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="88f31-122">-BackendAddressPool</span></span>
<span data-ttu-id="88f31-123">Ссылка на пул ДИПов.</span><span class="sxs-lookup"><span data-stu-id="88f31-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="88f31-124">Исходящие потоки случайным образом балансирует нагрузка по IP на backend IPS.</span><span class="sxs-lookup"><span data-stu-id="88f31-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88f31-125">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="88f31-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="88f31-126">Ссылка на пул ДИПов.</span><span class="sxs-lookup"><span data-stu-id="88f31-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="88f31-127">Исходящие потоки случайным образом балансирует нагрузка по IP на backend IPS.</span><span class="sxs-lookup"><span data-stu-id="88f31-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88f31-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f31-128">-DefaultProfile</span></span>
<span data-ttu-id="88f31-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88f31-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88f31-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="88f31-130">-EnableTcpReset</span></span>
<span data-ttu-id="88f31-131">Получение перенаправленного TCP-сброса при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="88f31-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="88f31-132">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="88f31-132">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="88f31-133">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="88f31-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="88f31-134">IP-адреса переднего ip-адреса балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="88f31-134">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88f31-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="88f31-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="88f31-136">Время ожидания для неавтайного подключения TCP</span><span class="sxs-lookup"><span data-stu-id="88f31-136">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="88f31-137">-Name</span><span class="sxs-lookup"><span data-stu-id="88f31-137">-Name</span></span>
<span data-ttu-id="88f31-138">Имя правила исходящие.</span><span class="sxs-lookup"><span data-stu-id="88f31-138">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="88f31-139">-Protocol</span><span class="sxs-lookup"><span data-stu-id="88f31-139">-Protocol</span></span>
<span data-ttu-id="88f31-140">Протокол TCP, UDP или All</span><span class="sxs-lookup"><span data-stu-id="88f31-140">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="88f31-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88f31-141">-Confirm</span></span>
<span data-ttu-id="88f31-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88f31-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88f31-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88f31-143">-WhatIf</span></span>
<span data-ttu-id="88f31-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88f31-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88f31-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="88f31-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88f31-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f31-146">CommonParameters</span></span>
<span data-ttu-id="88f31-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88f31-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f31-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88f31-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f31-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88f31-149">INPUTS</span></span>

### <span data-ttu-id="88f31-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="88f31-150">System.Int32</span></span>

### <span data-ttu-id="88f31-151">System.String</span><span class="sxs-lookup"><span data-stu-id="88f31-151">System.String</span></span>

### <span data-ttu-id="88f31-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="88f31-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="88f31-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="88f31-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="88f31-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88f31-154">OUTPUTS</span></span>

### <span data-ttu-id="88f31-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="88f31-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="88f31-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="88f31-156">NOTES</span></span>

## <span data-ttu-id="88f31-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88f31-157">RELATED LINKS</span></span>

[<span data-ttu-id="88f31-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88f31-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="88f31-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88f31-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="88f31-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88f31-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="88f31-161">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88f31-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
