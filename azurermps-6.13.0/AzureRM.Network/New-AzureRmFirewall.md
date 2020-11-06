---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
ms.openlocfilehash: 6486c7db87e8c71b0703b90a765fa30287b82769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568882"
---
# <span data-ttu-id="2e105-101">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2e105-101">New-AzureRmFirewall</span></span>

## <span data-ttu-id="2e105-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e105-102">SYNOPSIS</span></span>
<span data-ttu-id="2e105-103">Создание нового брандмауэра в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2e105-103">Creates a new Firewall in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e105-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e105-104">SYNTAX</span></span>

```
New-AzureRmFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-VirtualNetworkName <String>] [-PublicIpName <String>]
 [-ApplicationRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]>]
 [-NatRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]>]
 [-NetworkRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e105-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e105-105">DESCRIPTION</span></span>
<span data-ttu-id="2e105-106">Командлет **New-AzureRmFirewall** создает брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="2e105-106">The **New-AzureRmFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="2e105-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e105-107">EXAMPLES</span></span>

### <span data-ttu-id="2e105-108">1: создание брандмауэра, подключенного к виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="2e105-108">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="2e105-109">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet, в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="2e105-109">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="2e105-110">Поскольку правила не указаны, брандмауэр блокирует весь трафик (поведение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="2e105-110">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>

### <span data-ttu-id="2e105-111">2. Создание брандмауэра, разрешающего весь трафик HTTPS</span><span class="sxs-lookup"><span data-stu-id="2e105-111">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="2e105-112">В этом примере создается брандмауэр, разрешающий весь трафик HTTPS для порта 443.</span><span class="sxs-lookup"><span data-stu-id="2e105-112">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>

### <span data-ttu-id="2e105-113">3: DNAT-Redirect трафик, направленный на 10.1.2.3:80 в 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="2e105-113">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection
```

<span data-ttu-id="2e105-114">В этом примере создан брандмауэр, который был переведен на IP-адрес назначения и порт всех пакетов, направленных на 10.1.2.3:80 в 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="2e105-114">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>

## <span data-ttu-id="2e105-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e105-115">PARAMETERS</span></span>

### <span data-ttu-id="2e105-116">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2e105-116">-ApplicationRuleCollection</span></span>
<span data-ttu-id="2e105-117">Определяет наборы правил приложений для нового брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="2e105-117">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e105-118">-AsJob</span></span>
<span data-ttu-id="2e105-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2e105-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e105-120">-DefaultProfile</span></span>
<span data-ttu-id="2e105-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e105-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2e105-122">-Force</span></span>
<span data-ttu-id="2e105-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2e105-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-124">-Location</span><span class="sxs-lookup"><span data-stu-id="2e105-124">-Location</span></span>
<span data-ttu-id="2e105-125">Указывает регион для брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="2e105-125">Specifies the region for the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e105-126">-Name</span></span>
<span data-ttu-id="2e105-127">Указывает имя брандмауэра Azure, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2e105-127">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-128">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2e105-128">-NatRuleCollection</span></span>
<span data-ttu-id="2e105-129">Список AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="2e105-129">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-130">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2e105-130">-NetworkRuleCollection</span></span>
<span data-ttu-id="2e105-131">Список AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="2e105-131">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-132">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="2e105-132">-PublicIpName</span></span>
<span data-ttu-id="2e105-133">Общедоступное имя IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2e105-133">Public Ip Name.</span></span> <span data-ttu-id="2e105-134">Общедоступный IP-адрес должен использовать стандартную SKU и должен принадлежать к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="2e105-134">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e105-135">-ResourceGroupName</span></span>
<span data-ttu-id="2e105-136">Указывает имя группы ресурсов, в которой будет содержаться брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="2e105-136">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="2e105-137">-Tag</span></span>
<span data-ttu-id="2e105-138">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2e105-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2e105-139">Например:</span><span class="sxs-lookup"><span data-stu-id="2e105-139">For example:</span></span>

<span data-ttu-id="2e105-140">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2e105-140">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2e105-141">-VirtualNetworkName</span></span>
<span data-ttu-id="2e105-142">Указывает имя виртуальной сети, для которой будет развернут брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="2e105-142">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="2e105-143">Виртуальная сеть и брандмауэр должны принадлежать к одной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2e105-143">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e105-144">-Confirm</span></span>
<span data-ttu-id="2e105-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2e105-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e105-146">-WhatIf</span></span>
<span data-ttu-id="2e105-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2e105-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e105-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2e105-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e105-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e105-149">CommonParameters</span></span>
<span data-ttu-id="2e105-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e105-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e105-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e105-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e105-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e105-152">INPUTS</span></span>

### <span data-ttu-id="2e105-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="2e105-153">None</span></span>
<span data-ttu-id="2e105-154">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2e105-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e105-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e105-155">OUTPUTS</span></span>

### <span data-ttu-id="2e105-156">Microsoft. Azure. Commands. Network. Models. PSFirewall</span><span class="sxs-lookup"><span data-stu-id="2e105-156">Microsoft.Azure.Commands.Network.Models.PSFirewall</span></span>

## <span data-ttu-id="2e105-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e105-157">NOTES</span></span>

## <span data-ttu-id="2e105-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e105-158">RELATED LINKS</span></span>

[<span data-ttu-id="2e105-159">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2e105-159">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="2e105-160">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2e105-160">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="2e105-161">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2e105-161">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)

[<span data-ttu-id="2e105-162">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2e105-162">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="2e105-163">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2e105-163">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="2e105-164">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2e105-164">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)
