---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dfc0e6616113a163771d214a7ebe7f8df593173c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317129"
---
# <span data-ttu-id="dfb3c-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dfb3c-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="dfb3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dfb3c-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb3c-103">Создание конфигурации входящего пула NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="dfb3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dfb3c-104">SYNTAX</span></span>

### <span data-ttu-id="dfb3c-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dfb3c-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfb3c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dfb3c-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfb3c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfb3c-107">DESCRIPTION</span></span>
<span data-ttu-id="dfb3c-108">Командлет **New-AzLoadBalancerInboundNatPoolConfig** создает конфигурацию ВХОДЯЩЕГО пула NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="dfb3c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dfb3c-109">EXAMPLES</span></span>

### <span data-ttu-id="dfb3c-110">Пример 1: новое</span><span class="sxs-lookup"><span data-stu-id="dfb3c-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="dfb3c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dfb3c-111">PARAMETERS</span></span>

### <span data-ttu-id="dfb3c-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="dfb3c-112">-BackendPort</span></span>
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

### <span data-ttu-id="dfb3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb3c-113">-DefaultProfile</span></span>
<span data-ttu-id="dfb3c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfb3c-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="dfb3c-115">-EnableFloatingIP</span></span>
<span data-ttu-id="dfb3c-116">Настраивает конечную точку виртуальной машины для плавающей IP-способности, необходимой для настройки группы доступности SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="dfb3c-117">Этот параметр является обязательным при использовании групп доступности SQL AlwaysOn в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="dfb3c-118">Этот параметр невозможно изменить после создания конечной точки.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="dfb3c-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="dfb3c-119">-EnableTcpReset</span></span>
<span data-ttu-id="dfb3c-120">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="dfb3c-121">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="dfb3c-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfb3c-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="dfb3c-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dfb3c-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="dfb3c-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="dfb3c-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="dfb3c-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="dfb3c-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="dfb3c-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="dfb3c-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="dfb3c-127">Таймаут бездействия в соединении TCP.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="dfb3c-128">Значение может быть установлено между 4 и 30 минутами.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="dfb3c-129">Значение по умолчанию — 4 минуты.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-129">The default value is 4 minutes.</span></span> <span data-ttu-id="dfb3c-130">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="dfb3c-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dfb3c-131">-Name</span></span>
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

### <span data-ttu-id="dfb3c-132">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="dfb3c-132">-Protocol</span></span>
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

### <span data-ttu-id="dfb3c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfb3c-133">-Confirm</span></span>
<span data-ttu-id="dfb3c-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfb3c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfb3c-135">-WhatIf</span></span>
<span data-ttu-id="dfb3c-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfb3c-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfb3c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb3c-138">CommonParameters</span></span>
<span data-ttu-id="dfb3c-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dfb3c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb3c-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfb3c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb3c-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dfb3c-141">INPUTS</span></span>

### <span data-ttu-id="dfb3c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="dfb3c-142">System.String</span></span>

### <span data-ttu-id="dfb3c-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dfb3c-143">System.Int32</span></span>

### <span data-ttu-id="dfb3c-144">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfb3c-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="dfb3c-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfb3c-145">OUTPUTS</span></span>

### <span data-ttu-id="dfb3c-146">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="dfb3c-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="dfb3c-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="dfb3c-147">NOTES</span></span>

## <span data-ttu-id="dfb3c-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfb3c-148">RELATED LINKS</span></span>

[<span data-ttu-id="dfb3c-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dfb3c-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="dfb3c-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dfb3c-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="dfb3c-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dfb3c-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="dfb3c-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="dfb3c-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
