---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244777"
---
# <span data-ttu-id="2de91-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2de91-101">Set-AzFirewall</span></span>

## <span data-ttu-id="2de91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2de91-102">SYNOPSIS</span></span>
<span data-ttu-id="2de91-103">Сохранение измененного брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="2de91-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="2de91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2de91-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2de91-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2de91-105">DESCRIPTION</span></span>
<span data-ttu-id="2de91-106">Командлет **Set-AzFirewall** обновляет брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="2de91-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="2de91-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2de91-107">EXAMPLES</span></span>

### <span data-ttu-id="2de91-108">1: обновление приоритета коллекции правил приложения брандмауэра</span><span class="sxs-lookup"><span data-stu-id="2de91-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="2de91-109">В этом примере обновляется приоритет существующей коллекции правил брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2de91-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="2de91-110">Предполагается, что брандмауэр Azure "AzureFirewall" в группе ресурсов "RG" имеет коллекцию правил приложений с именем "ruleCollectionName", команды выше будут изменять приоритет этой коллекции правил и затем обновлять брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="2de91-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="2de91-111">Без команды Set-AzFirewall все операции, выполненные на локальном объекте $azFw, не отражаются на сервере.</span><span class="sxs-lookup"><span data-stu-id="2de91-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="2de91-112">2. Создание брандмауэра Azure и установка коллекции правил приложений позже</span><span class="sxs-lookup"><span data-stu-id="2de91-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="2de91-113">В этом примере брандмауэр создается в первую очередь без каких-либо коллекций правил приложений.</span><span class="sxs-lookup"><span data-stu-id="2de91-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="2de91-114">После этого создается правило приложения и коллекция правил приложения, а затем объект Firewall изменяется в памяти, не влияя на реальную конфигурацию в облаке.</span><span class="sxs-lookup"><span data-stu-id="2de91-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="2de91-115">Чтобы изменения были отражены в облаке, необходимо вызвать Set-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="2de91-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="2de91-116">3: обновление угрозы в режиме функционирования Intel в брандмауэре Azure</span><span class="sxs-lookup"><span data-stu-id="2de91-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="2de91-117">В этом примере обновляется режим функционирования программного кода Intel для брандмауэра Azure "AzureFirewall" в группе ресурсов "RG".</span><span class="sxs-lookup"><span data-stu-id="2de91-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="2de91-118">Без команды Set-AzFirewall все операции, выполненные на локальном объекте $azFw, не отражаются на сервере.</span><span class="sxs-lookup"><span data-stu-id="2de91-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="2de91-119">4. выделять и выделять брандмауэр</span><span class="sxs-lookup"><span data-stu-id="2de91-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="2de91-120">В этом примере извлекается брандмауэр, размещается брандмауэр и сохраняется.</span><span class="sxs-lookup"><span data-stu-id="2de91-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="2de91-121">Команда "освободить" удаляет запущенную службу, но сохраняет конфигурацию брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="2de91-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="2de91-122">Чтобы изменения были отражены в облаке, необходимо вызвать Set-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="2de91-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="2de91-123">Если пользователь хочет снова запустить службу, необходимо вызвать метод выделения на брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="2de91-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="2de91-124">Новая виртуальная сеть и общедоступный IP-адрес должны находиться в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="2de91-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="2de91-125">Чтобы изменения были отражены в облаке, необходимо вызвать Set-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="2de91-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="2de91-126">5. выделять с общедоступным IP-адресом для управления сценариями принудительного туннелирования</span><span class="sxs-lookup"><span data-stu-id="2de91-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="2de91-127">Этот пример выделяет брандмауэр с общедоступным IP-адресом управления и подсетью для сценариев принудительного туннелирования.</span><span class="sxs-lookup"><span data-stu-id="2de91-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="2de91-128">VNet должен содержать подсеть с именем "AzureFirewallManagementSubnet".</span><span class="sxs-lookup"><span data-stu-id="2de91-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="2de91-129">6. Добавьте общедоступный IP-адрес в брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="2de91-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="2de91-130">В данном примере — общедоступный IP-адрес "azFwPublicIp1", подключенный к межсетевому экрану.</span><span class="sxs-lookup"><span data-stu-id="2de91-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="2de91-131">7. Удаление общедоступного IP-адреса из брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="2de91-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="2de91-132">В этом примере общедоступный IP-адрес "azFwPublicIp1" отделен от брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="2de91-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="2de91-133">8: изменение общедоступного IP-адреса для управления в брандмауэре Azure</span><span class="sxs-lookup"><span data-stu-id="2de91-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="2de91-134">В этом примере общедоступный IP-адрес управления для вашего брандмауэра изменится на "AzFwMgmtPublicIp2".</span><span class="sxs-lookup"><span data-stu-id="2de91-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="2de91-135">9: Добавление конфигурации DNS в брандмауэр Azure</span><span class="sxs-lookup"><span data-stu-id="2de91-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="2de91-136">В этом примере Настройка DNS-прокси и DNS-сервера присоединяется к брандмауэру.</span><span class="sxs-lookup"><span data-stu-id="2de91-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="2de91-137">10: обновление назначения для существующего правила в коллекции правил приложения брандмауэра</span><span class="sxs-lookup"><span data-stu-id="2de91-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="2de91-138">В этом примере вы обновляете назначение существующего правила в коллекции правил брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2de91-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="2de91-139">Это позволяет автоматически обновлять правила при динамическом изменении IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="2de91-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="2de91-140">11: разрешение активного FTP на брандмауэре Azure</span><span class="sxs-lookup"><span data-stu-id="2de91-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="2de91-141">В этом примере в брандмауэре разрешено использование активного FTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="2de91-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="2de91-142">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2de91-142">PARAMETERS</span></span>

### <span data-ttu-id="2de91-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2de91-143">-AsJob</span></span>
<span data-ttu-id="2de91-144">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2de91-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2de91-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2de91-145">-AzureFirewall</span></span>
<span data-ttu-id="2de91-146">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2de91-146">The AzureFirewall</span></span>

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

### <span data-ttu-id="2de91-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de91-147">-DefaultProfile</span></span>
<span data-ttu-id="2de91-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2de91-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2de91-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2de91-149">-Confirm</span></span>
<span data-ttu-id="2de91-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2de91-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2de91-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de91-151">-WhatIf</span></span>
<span data-ttu-id="2de91-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2de91-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2de91-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2de91-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2de91-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de91-154">CommonParameters</span></span>
<span data-ttu-id="2de91-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2de91-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de91-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de91-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de91-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2de91-157">INPUTS</span></span>

### <span data-ttu-id="2de91-158">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2de91-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="2de91-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2de91-159">OUTPUTS</span></span>

### <span data-ttu-id="2de91-160">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2de91-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="2de91-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="2de91-161">NOTES</span></span>

## <span data-ttu-id="2de91-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2de91-162">RELATED LINKS</span></span>

[<span data-ttu-id="2de91-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2de91-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="2de91-164">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2de91-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="2de91-165">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2de91-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
