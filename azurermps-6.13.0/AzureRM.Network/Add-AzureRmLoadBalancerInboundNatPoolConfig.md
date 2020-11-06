---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 2245fa10d160fc0f6b085a039214f9bcd72404a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560112"
---
# <span data-ttu-id="ba4a7-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ba4a7-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="ba4a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba4a7-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba4a7-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba4a7-103">SYNTAX</span></span>

### <span data-ttu-id="ba4a7-104">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba4a7-104">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba4a7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba4a7-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba4a7-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba4a7-106">DESCRIPTION</span></span>

## <span data-ttu-id="ba4a7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba4a7-107">EXAMPLES</span></span>

### <span data-ttu-id="ba4a7-108">1: Добавление</span><span class="sxs-lookup"><span data-stu-id="ba4a7-108">1: Add</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="ba4a7-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba4a7-109">PARAMETERS</span></span>

### <span data-ttu-id="ba4a7-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ba4a7-110">-BackendPort</span></span>
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

### <span data-ttu-id="ba4a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba4a7-111">-DefaultProfile</span></span>
<span data-ttu-id="ba4a7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba4a7-113">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="ba4a7-113">-EnableFloatingIP</span></span>
<span data-ttu-id="ba4a7-114">Настраивает конечную точку виртуальной машины для плавающей IP-способности, необходимой для настройки группы доступности SQL AlwaysOn.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-114">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="ba4a7-115">Этот параметр является обязательным при использовании групп доступности SQL AlwaysOn в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-115">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="ba4a7-116">Этот параметр невозможно изменить после создания конечной точки.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-116">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="ba4a7-117">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ba4a7-117">-EnableTcpReset</span></span>
<span data-ttu-id="ba4a7-118">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-118">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="ba4a7-119">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-119">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ba4a7-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba4a7-120">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="ba4a7-121">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ba4a7-121">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="ba4a7-122">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="ba4a7-122">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="ba4a7-123">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="ba4a7-123">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="ba4a7-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ba4a7-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ba4a7-125">Таймаут бездействия в соединении TCP.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-125">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="ba4a7-126">Значение может быть установлено между 4 и 30 минутами.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-126">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="ba4a7-127">Значение по умолчанию — 4 минуты.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-127">The default value is 4 minutes.</span></span> <span data-ttu-id="ba4a7-128">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ba4a7-129">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="ba4a7-129">-LoadBalancer</span></span>
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

### <span data-ttu-id="ba4a7-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba4a7-130">-Name</span></span>
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

### <span data-ttu-id="ba4a7-131">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="ba4a7-131">-Protocol</span></span>
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

### <span data-ttu-id="ba4a7-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba4a7-132">-Confirm</span></span>
<span data-ttu-id="ba4a7-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba4a7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba4a7-134">-WhatIf</span></span>
<span data-ttu-id="ba4a7-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba4a7-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba4a7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba4a7-137">CommonParameters</span></span>
<span data-ttu-id="ba4a7-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba4a7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba4a7-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba4a7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba4a7-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba4a7-140">INPUTS</span></span>

### <span data-ttu-id="ba4a7-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ba4a7-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="ba4a7-142">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ba4a7-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="ba4a7-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba4a7-143">OUTPUTS</span></span>

### <span data-ttu-id="ba4a7-144">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ba4a7-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ba4a7-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba4a7-145">NOTES</span></span>

## <span data-ttu-id="ba4a7-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba4a7-146">RELATED LINKS</span></span>
