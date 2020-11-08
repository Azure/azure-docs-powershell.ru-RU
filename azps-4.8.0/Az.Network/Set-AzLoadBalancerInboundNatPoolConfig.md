---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: ac57c65f670734be6638e71179147490b41085f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078836"
---
# <span data-ttu-id="767df-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="767df-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="767df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="767df-102">SYNOPSIS</span></span>
<span data-ttu-id="767df-103">Задает конфигурацию входящего пула NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="767df-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="767df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="767df-104">SYNTAX</span></span>

### <span data-ttu-id="767df-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="767df-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="767df-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="767df-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="767df-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="767df-107">DESCRIPTION</span></span>
<span data-ttu-id="767df-108">Командлет **Set-AzLoadBalancerInboundNatPoolConfig** задает конфигурацию ВХОДЯЩЕГО пула NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="767df-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="767df-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="767df-109">EXAMPLES</span></span>

### <span data-ttu-id="767df-110">Пример 1: Set</span><span class="sxs-lookup"><span data-stu-id="767df-110">Example 1: Set</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
PS C:\> $slb | Set-AzLoadBalancer
```

## <span data-ttu-id="767df-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="767df-111">PARAMETERS</span></span>

### <span data-ttu-id="767df-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="767df-112">-BackendPort</span></span>
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

### <span data-ttu-id="767df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="767df-113">-DefaultProfile</span></span>
<span data-ttu-id="767df-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="767df-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="767df-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="767df-115">-EnableFloatingIP</span></span>
<span data-ttu-id="767df-116">Настраивает конечную точку виртуальной машины для плавающей IP-способности, необходимой для настройки группы доступности SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="767df-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="767df-117">Этот параметр является обязательным при использовании групп доступности SQL AlwaysOn в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="767df-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="767df-118">Этот параметр невозможно изменить после создания конечной точки.</span><span class="sxs-lookup"><span data-stu-id="767df-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="767df-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="767df-119">-EnableTcpReset</span></span>
<span data-ttu-id="767df-120">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="767df-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="767df-121">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="767df-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="767df-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="767df-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="767df-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="767df-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="767df-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="767df-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="767df-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="767df-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="767df-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="767df-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="767df-127">Таймаут бездействия в соединении TCP.</span><span class="sxs-lookup"><span data-stu-id="767df-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="767df-128">Значение может быть установлено между 4 и 30 минутами.</span><span class="sxs-lookup"><span data-stu-id="767df-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="767df-129">Значение по умолчанию — 4 минуты.</span><span class="sxs-lookup"><span data-stu-id="767df-129">The default value is 4 minutes.</span></span> <span data-ttu-id="767df-130">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="767df-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="767df-131">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="767df-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="767df-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="767df-132">-Name</span></span>
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

### <span data-ttu-id="767df-133">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="767df-133">-Protocol</span></span>
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

### <span data-ttu-id="767df-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="767df-134">-Confirm</span></span>
<span data-ttu-id="767df-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="767df-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="767df-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="767df-136">-WhatIf</span></span>
<span data-ttu-id="767df-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="767df-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="767df-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="767df-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="767df-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="767df-139">CommonParameters</span></span>
<span data-ttu-id="767df-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="767df-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="767df-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="767df-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="767df-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="767df-142">INPUTS</span></span>

### <span data-ttu-id="767df-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="767df-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="767df-144">System. String</span><span class="sxs-lookup"><span data-stu-id="767df-144">System.String</span></span>

### <span data-ttu-id="767df-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="767df-145">System.Int32</span></span>

### <span data-ttu-id="767df-146">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="767df-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="767df-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="767df-147">OUTPUTS</span></span>

### <span data-ttu-id="767df-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="767df-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="767df-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="767df-149">NOTES</span></span>

## <span data-ttu-id="767df-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="767df-150">RELATED LINKS</span></span>

[<span data-ttu-id="767df-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="767df-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="767df-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="767df-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="767df-153">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="767df-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="767df-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="767df-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
