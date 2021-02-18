---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 993b1a3987427f096ecd061199663b35b6577b08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228036"
---
# <span data-ttu-id="7bb48-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7bb48-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="7bb48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bb48-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb48-103">Добавляет входящий пул NAT в балансировую нагрузку.</span><span class="sxs-lookup"><span data-stu-id="7bb48-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="7bb48-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7bb48-104">SYNTAX</span></span>

### <span data-ttu-id="7bb48-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7bb48-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb48-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7bb48-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bb48-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bb48-107">DESCRIPTION</span></span>
<span data-ttu-id="7bb48-108">Cmdlet **Add-AzLoadBalancerInboundNatPoolConfig** добавляет входящий пул NAT к балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="7bb48-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="7bb48-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7bb48-109">EXAMPLES</span></span>

### <span data-ttu-id="7bb48-110">Пример 1. Добавление</span><span class="sxs-lookup"><span data-stu-id="7bb48-110">Example 1: Add</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="7bb48-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bb48-111">PARAMETERS</span></span>

### <span data-ttu-id="7bb48-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="7bb48-112">-BackendPort</span></span>
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

### <span data-ttu-id="7bb48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb48-113">-DefaultProfile</span></span>
<span data-ttu-id="7bb48-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7bb48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bb48-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="7bb48-115">-EnableFloatingIP</span></span>
<span data-ttu-id="7bb48-116">Настраивает конечную точку виртуальной машины для плавающей возможности IP-адреса, необходимой для настройки группы доступности SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="7bb48-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="7bb48-117">Этот параметр необходим при использовании групп доступности SQL AlwaysOn в SQL сервере.</span><span class="sxs-lookup"><span data-stu-id="7bb48-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="7bb48-118">Этот параметр нельзя изменить после создания конечной точки.</span><span class="sxs-lookup"><span data-stu-id="7bb48-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="7bb48-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="7bb48-119">-EnableTcpReset</span></span>
<span data-ttu-id="7bb48-120">Получение перенаправленного TCP-сброса при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="7bb48-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="7bb48-121">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="7bb48-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="7bb48-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bb48-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="7bb48-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7bb48-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="7bb48-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="7bb48-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="7bb48-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="7bb48-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="7bb48-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7bb48-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7bb48-127">Время ожидания для неавтайного подключения TCP.</span><span class="sxs-lookup"><span data-stu-id="7bb48-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="7bb48-128">Это значение можно установить от 4 до 30 минут.</span><span class="sxs-lookup"><span data-stu-id="7bb48-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="7bb48-129">Значение по умолчанию — 4 минуты.</span><span class="sxs-lookup"><span data-stu-id="7bb48-129">The default value is 4 minutes.</span></span> <span data-ttu-id="7bb48-130">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="7bb48-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="7bb48-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7bb48-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="7bb48-132">-Name</span><span class="sxs-lookup"><span data-stu-id="7bb48-132">-Name</span></span>
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

### <span data-ttu-id="7bb48-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7bb48-133">-Protocol</span></span>
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

### <span data-ttu-id="7bb48-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bb48-134">-Confirm</span></span>
<span data-ttu-id="7bb48-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7bb48-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bb48-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb48-136">-WhatIf</span></span>
<span data-ttu-id="7bb48-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bb48-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bb48-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7bb48-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bb48-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb48-139">CommonParameters</span></span>
<span data-ttu-id="7bb48-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bb48-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb48-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bb48-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb48-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bb48-142">INPUTS</span></span>

### <span data-ttu-id="7bb48-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7bb48-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="7bb48-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7bb48-144">System.String</span></span>

### <span data-ttu-id="7bb48-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7bb48-145">System.Int32</span></span>

### <span data-ttu-id="7bb48-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bb48-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="7bb48-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7bb48-147">OUTPUTS</span></span>

### <span data-ttu-id="7bb48-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7bb48-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7bb48-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7bb48-149">NOTES</span></span>

## <span data-ttu-id="7bb48-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7bb48-150">RELATED LINKS</span></span>

[<span data-ttu-id="7bb48-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7bb48-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7bb48-152">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7bb48-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7bb48-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7bb48-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7bb48-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7bb48-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
