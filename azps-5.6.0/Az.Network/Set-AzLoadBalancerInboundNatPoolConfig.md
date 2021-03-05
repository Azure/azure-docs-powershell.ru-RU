---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 10539a09c8849f1afd5cd3c5bd9e249929577342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963896"
---
# <span data-ttu-id="d50b7-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d50b7-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="d50b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d50b7-102">SYNOPSIS</span></span>
<span data-ttu-id="d50b7-103">Задает конфигурацию входящий пул NAT для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d50b7-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="d50b7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d50b7-104">SYNTAX</span></span>

### <span data-ttu-id="d50b7-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d50b7-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d50b7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d50b7-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d50b7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d50b7-107">DESCRIPTION</span></span>
<span data-ttu-id="d50b7-108">**Cmdlet Set-AzLoadBalancerInboundNatPoolConfig** задает конфигурацию входящий пул NAT для балансиента нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d50b7-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="d50b7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d50b7-109">EXAMPLES</span></span>

### <span data-ttu-id="d50b7-110">Пример 1. Множество</span><span class="sxs-lookup"><span data-stu-id="d50b7-110">Example 1: Set</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
PS C:\> $slb | Set-AzLoadBalancer
```

## <span data-ttu-id="d50b7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d50b7-111">PARAMETERS</span></span>

### <span data-ttu-id="d50b7-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="d50b7-112">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d50b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d50b7-113">-DefaultProfile</span></span>
<span data-ttu-id="d50b7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d50b7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d50b7-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d50b7-115">-EnableFloatingIP</span></span>
<span data-ttu-id="d50b7-116">Настраивает конечную точку виртуальной машины для плавающей возможности IP-адреса, необходимой для настройки группы SQL доступности AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="d50b7-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="d50b7-117">Этот параметр необходим при использовании групп доступности SQL AlwaysOn в SQL сервере.</span><span class="sxs-lookup"><span data-stu-id="d50b7-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="d50b7-118">Этот параметр нельзя изменить после создания конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d50b7-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="d50b7-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="d50b7-119">-EnableTcpReset</span></span>
<span data-ttu-id="d50b7-120">Получите раздвивный TCP-сброс при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="d50b7-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="d50b7-121">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="d50b7-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d50b7-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d50b7-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="d50b7-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d50b7-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="d50b7-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="d50b7-124">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d50b7-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="d50b7-125">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d50b7-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d50b7-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d50b7-127">Время ожидания для неавтного подключения TCP.</span><span class="sxs-lookup"><span data-stu-id="d50b7-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="d50b7-128">Это значение можно установить от 4 до 30 минут.</span><span class="sxs-lookup"><span data-stu-id="d50b7-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="d50b7-129">Значение по умолчанию — 4 минуты.</span><span class="sxs-lookup"><span data-stu-id="d50b7-129">The default value is 4 minutes.</span></span> <span data-ttu-id="d50b7-130">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="d50b7-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d50b7-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d50b7-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="d50b7-132">-Name</span><span class="sxs-lookup"><span data-stu-id="d50b7-132">-Name</span></span>
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

### <span data-ttu-id="d50b7-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d50b7-133">-Protocol</span></span>
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

### <span data-ttu-id="d50b7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d50b7-134">-Confirm</span></span>
<span data-ttu-id="d50b7-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d50b7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d50b7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d50b7-136">-WhatIf</span></span>
<span data-ttu-id="d50b7-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d50b7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d50b7-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d50b7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d50b7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d50b7-139">CommonParameters</span></span>
<span data-ttu-id="d50b7-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d50b7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d50b7-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d50b7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d50b7-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d50b7-142">INPUTS</span></span>

### <span data-ttu-id="d50b7-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d50b7-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="d50b7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d50b7-144">System.String</span></span>

### <span data-ttu-id="d50b7-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d50b7-145">System.Int32</span></span>

### <span data-ttu-id="d50b7-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d50b7-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="d50b7-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d50b7-147">OUTPUTS</span></span>

### <span data-ttu-id="d50b7-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d50b7-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d50b7-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d50b7-149">NOTES</span></span>

## <span data-ttu-id="d50b7-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d50b7-150">RELATED LINKS</span></span>

[<span data-ttu-id="d50b7-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d50b7-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d50b7-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d50b7-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d50b7-153">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d50b7-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d50b7-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d50b7-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
