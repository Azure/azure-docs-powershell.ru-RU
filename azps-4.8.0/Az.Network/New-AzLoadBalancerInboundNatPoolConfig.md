---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dfc0e6616113a163771d214a7ebe7f8df593173c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234991"
---
# <span data-ttu-id="c7591-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c7591-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="c7591-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7591-102">SYNOPSIS</span></span>
<span data-ttu-id="c7591-103">Создание конфигурации входящего пула NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c7591-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="c7591-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7591-104">SYNTAX</span></span>

### <span data-ttu-id="c7591-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7591-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7591-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7591-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7591-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7591-107">DESCRIPTION</span></span>
<span data-ttu-id="c7591-108">Командлет **New-AzLoadBalancerInboundNatPoolConfig** создает конфигурацию ВХОДЯЩЕГО пула NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c7591-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="c7591-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7591-109">EXAMPLES</span></span>

### <span data-ttu-id="c7591-110">Пример 1: новое</span><span class="sxs-lookup"><span data-stu-id="c7591-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="c7591-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7591-111">PARAMETERS</span></span>

### <span data-ttu-id="c7591-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c7591-112">-BackendPort</span></span>
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

### <span data-ttu-id="c7591-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7591-113">-DefaultProfile</span></span>
<span data-ttu-id="c7591-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7591-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7591-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c7591-115">-EnableFloatingIP</span></span>
<span data-ttu-id="c7591-116">Настраивает конечную точку виртуальной машины для плавающей IP-способности, необходимой для настройки группы доступности SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="c7591-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="c7591-117">Этот параметр является обязательным при использовании групп доступности SQL AlwaysOn в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c7591-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="c7591-118">Этот параметр невозможно изменить после создания конечной точки.</span><span class="sxs-lookup"><span data-stu-id="c7591-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="c7591-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c7591-119">-EnableTcpReset</span></span>
<span data-ttu-id="c7591-120">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="c7591-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c7591-121">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="c7591-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c7591-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7591-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="c7591-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c7591-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="c7591-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="c7591-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="c7591-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="c7591-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="c7591-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c7591-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c7591-127">Таймаут бездействия в соединении TCP.</span><span class="sxs-lookup"><span data-stu-id="c7591-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="c7591-128">Значение может быть установлено между 4 и 30 минутами.</span><span class="sxs-lookup"><span data-stu-id="c7591-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="c7591-129">Значение по умолчанию — 4 минуты.</span><span class="sxs-lookup"><span data-stu-id="c7591-129">The default value is 4 minutes.</span></span> <span data-ttu-id="c7591-130">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="c7591-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c7591-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7591-131">-Name</span></span>
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

### <span data-ttu-id="c7591-132">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="c7591-132">-Protocol</span></span>
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

### <span data-ttu-id="c7591-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7591-133">-Confirm</span></span>
<span data-ttu-id="c7591-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c7591-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7591-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7591-135">-WhatIf</span></span>
<span data-ttu-id="c7591-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c7591-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7591-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c7591-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7591-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7591-138">CommonParameters</span></span>
<span data-ttu-id="c7591-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7591-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7591-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7591-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7591-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7591-141">INPUTS</span></span>

### <span data-ttu-id="c7591-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c7591-142">System.String</span></span>

### <span data-ttu-id="c7591-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c7591-143">System.Int32</span></span>

### <span data-ttu-id="c7591-144">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7591-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="c7591-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7591-145">OUTPUTS</span></span>

### <span data-ttu-id="c7591-146">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="c7591-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="c7591-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7591-147">NOTES</span></span>

## <span data-ttu-id="c7591-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7591-148">RELATED LINKS</span></span>

[<span data-ttu-id="c7591-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c7591-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c7591-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c7591-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c7591-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c7591-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="c7591-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c7591-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)