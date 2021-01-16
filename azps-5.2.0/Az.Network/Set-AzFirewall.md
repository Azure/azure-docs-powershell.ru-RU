---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326986"
---
# <span data-ttu-id="eadd3-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="eadd3-101">Set-AzFirewall</span></span>

## <span data-ttu-id="eadd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eadd3-102">SYNOPSIS</span></span>
<span data-ttu-id="eadd3-103">Сохранение измененного брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="eadd3-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="eadd3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eadd3-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eadd3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eadd3-105">DESCRIPTION</span></span>
<span data-ttu-id="eadd3-106">С **помощью cmdlet set-AzFirewall** обновляется брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="eadd3-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="eadd3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eadd3-107">EXAMPLES</span></span>

### <span data-ttu-id="eadd3-108">1. Обновление приоритета для коллекции правил брандмауэра</span><span class="sxs-lookup"><span data-stu-id="eadd3-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="eadd3-109">В этом примере обновляется приоритет существующего сбора правил брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="eadd3-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="eadd3-110">Предположим, что брандмауэр Azure "AzureFirewall" в группе ресурсов "rg" содержит коллекцию правил приложения "ruleCollectionName", команды выше изменят приоритет этого сбора правил и обновят брандмауэр Azure после этого.</span><span class="sxs-lookup"><span data-stu-id="eadd3-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="eadd3-111">Без Set-AzFirewall команды все операции, выполняемые с локальным объектом $azFw, не отражаются на сервере.</span><span class="sxs-lookup"><span data-stu-id="eadd3-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="eadd3-112">2. Создание брандмауэра Azure и настройка коллекции правил приложения позже</span><span class="sxs-lookup"><span data-stu-id="eadd3-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="eadd3-113">В этом примере сначала создается брандмауэр без коллекций правил приложений.</span><span class="sxs-lookup"><span data-stu-id="eadd3-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="eadd3-114">После создания правила приложения и коллекции правил приложения объект брандмауэра будет изменен в памяти, не влияя на реальные настройки в облаке.</span><span class="sxs-lookup"><span data-stu-id="eadd3-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="eadd3-115">Чтобы изменения отображались в облаке, Set-AzFirewall должны быть вызваны.</span><span class="sxs-lookup"><span data-stu-id="eadd3-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="eadd3-116">3. Обновление режима операции Intel с угрозами брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="eadd3-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="eadd3-117">Этот пример обновляет режим операции Threat Intel брандмауэра Azure "AzureFirewall" в группе ресурсов "rg".</span><span class="sxs-lookup"><span data-stu-id="eadd3-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="eadd3-118">Без Set-AzFirewall команды все операции, выполняемые с локальным объектом $azFw, не отражаются на сервере.</span><span class="sxs-lookup"><span data-stu-id="eadd3-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="eadd3-119">4. Поиск и выделение брандмауэра</span><span class="sxs-lookup"><span data-stu-id="eadd3-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="eadd3-120">В этом примере извлекает и сохраняет брандмауэр, а также поиск брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="eadd3-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="eadd3-121">Команда Deallocate удаляет запущенную службу, но сохраняет конфигурацию брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="eadd3-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="eadd3-122">Чтобы изменения отображались в облаке, Set-AzFirewall должны быть вызваны.</span><span class="sxs-lookup"><span data-stu-id="eadd3-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="eadd3-123">Если пользователь хочет снова запустить службу, в брандмауэре следует использовать метод "Выделить".</span><span class="sxs-lookup"><span data-stu-id="eadd3-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="eadd3-124">Новые IP-адреса VNet и Public IP должны быть в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="eadd3-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="eadd3-125">Кроме того, для отражения изменений в облаке необходимо Set-AzFirewall должны быть вызваны.</span><span class="sxs-lookup"><span data-stu-id="eadd3-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="eadd3-126">5. Выделение с общедоступным IP-адресом управления для сценариев принудительного туннелинга</span><span class="sxs-lookup"><span data-stu-id="eadd3-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="eadd3-127">В этом примере брандмауэр с общедоступным IP-адресом и подсетей управления выделяется для сценариев принудительного туннелизации.</span><span class="sxs-lookup"><span data-stu-id="eadd3-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="eadd3-128">VNet должна содержать подсеть AzureFirewallManagementSubnet.</span><span class="sxs-lookup"><span data-stu-id="eadd3-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="eadd3-129">6. Добавление обще доступного IP-адреса в брандмауэр Azure</span><span class="sxs-lookup"><span data-stu-id="eadd3-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="eadd3-130">В этом примере общедоступный IP-адрес azFwPublicIp1, присоединенный к брандмауэру.</span><span class="sxs-lookup"><span data-stu-id="eadd3-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="eadd3-131">7. Удаление общеугодного IP-адреса из брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="eadd3-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="eadd3-132">В этом примере общедоступный IP-адрес azFwPublicIp1 будет отсоединен от брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="eadd3-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="eadd3-133">8. Изменение общеуправленного IP-адреса в брандмауэре Azure</span><span class="sxs-lookup"><span data-stu-id="eadd3-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="eadd3-134">В этом примере общедоступный IP-адрес управления брандмауэра будет изменен на "AzFwMgmtPublicIp2".</span><span class="sxs-lookup"><span data-stu-id="eadd3-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="eadd3-135">9. Добавление конфигурации DNS в брандмауэр Azure</span><span class="sxs-lookup"><span data-stu-id="eadd3-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="eadd3-136">В этом примере конфигурации DNS-прокси и DNS Server подключены к брандмауэру.</span><span class="sxs-lookup"><span data-stu-id="eadd3-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="eadd3-137">10. Обновление назначения существующего правила в коллекции правил брандмауэра приложения</span><span class="sxs-lookup"><span data-stu-id="eadd3-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="eadd3-138">В этом примере обновляется назначение существующего правила в коллекции правил брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="eadd3-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="eadd3-139">Это позволяет автоматически обновлять правила при динамическом изменении IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="eadd3-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="eadd3-140">11. Разрешение active FTP в брандмауэре Azure</span><span class="sxs-lookup"><span data-stu-id="eadd3-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="eadd3-141">В этом примере в брандмауэре разрешена активная FTP-возможность.</span><span class="sxs-lookup"><span data-stu-id="eadd3-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="eadd3-142">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eadd3-142">PARAMETERS</span></span>

### <span data-ttu-id="eadd3-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eadd3-143">-AsJob</span></span>
<span data-ttu-id="eadd3-144">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eadd3-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eadd3-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="eadd3-145">-AzureFirewall</span></span>
<span data-ttu-id="eadd3-146">The AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="eadd3-146">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eadd3-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eadd3-147">-DefaultProfile</span></span>
<span data-ttu-id="eadd3-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eadd3-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eadd3-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eadd3-149">-Confirm</span></span>
<span data-ttu-id="eadd3-150">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eadd3-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eadd3-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eadd3-151">-WhatIf</span></span>
<span data-ttu-id="eadd3-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eadd3-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eadd3-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eadd3-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eadd3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eadd3-154">CommonParameters</span></span>
<span data-ttu-id="eadd3-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eadd3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eadd3-156">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eadd3-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eadd3-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eadd3-157">INPUTS</span></span>

### <span data-ttu-id="eadd3-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="eadd3-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="eadd3-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eadd3-159">OUTPUTS</span></span>

### <span data-ttu-id="eadd3-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="eadd3-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="eadd3-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eadd3-161">NOTES</span></span>

## <span data-ttu-id="eadd3-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eadd3-162">RELATED LINKS</span></span>

[<span data-ttu-id="eadd3-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="eadd3-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="eadd3-164">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="eadd3-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="eadd3-165">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="eadd3-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
