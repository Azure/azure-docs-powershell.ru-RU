---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734619"
---
# <span data-ttu-id="91524-101">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="91524-101">Get-AzureRmFirewall</span></span>

## <span data-ttu-id="91524-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91524-102">SYNOPSIS</span></span>
<span data-ttu-id="91524-103">Получает брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="91524-103">Gets a Azure Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91524-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91524-104">SYNTAX</span></span>

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91524-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91524-105">DESCRIPTION</span></span>
<span data-ttu-id="91524-106">Командлет **Get-AzureRmFirewall** получает один или несколько брандмауэров в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91524-106">The **Get-AzureRmFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="91524-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91524-107">EXAMPLES</span></span>

### <span data-ttu-id="91524-108">1: получение всех брандмауэров в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="91524-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

<span data-ttu-id="91524-109">В этом примере извлекаются все брандмауэры в группе ресурсов "rgName".</span><span class="sxs-lookup"><span data-stu-id="91524-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="91524-110">2. Загрузка брандмауэра по имени</span><span class="sxs-lookup"><span data-stu-id="91524-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

<span data-ttu-id="91524-111">В этом примере извлекается брандмауэр с именем "azFw" в группе ресурсов "rgName".</span><span class="sxs-lookup"><span data-stu-id="91524-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="91524-112">3. получение доступа к брандмауэру и Добавление набора правил приложения в брандмауэр</span><span class="sxs-lookup"><span data-stu-id="91524-112">3:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="91524-113">В этом примере извлекается брандмауэр, после чего в брандмауэр добавляется коллекция правил приложений, вызывая метод AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="91524-113">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="91524-114">4. Извлеките брандмауэр и добавьте в брандмауэр коллекцию сетевых правил.</span><span class="sxs-lookup"><span data-stu-id="91524-114">4:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="91524-115">В этом примере извлекается брандмауэр, после чего в брандмауэр добавляется коллекция сетевых правил, вызывая метод AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="91524-115">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="91524-116">5. Извлеките брандмауэр и выберите в контекстном меню набор правил приложения, используя имя из брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="91524-116">5:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="91524-117">В этом примере извлекается брандмауэр и затем получается коллекция правил по имени, вызывающему метод GetApplicationRuleCollectionByName для объекта Firewall.</span><span class="sxs-lookup"><span data-stu-id="91524-117">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="91524-118">Имя набора правил для метода GetApplicationRuleCollectionByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="91524-118">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="91524-119">6. Извлеките брандмауэр и выберите в списке Сетевое правило по имени из брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="91524-119">6:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="91524-120">В этом примере извлекается брандмауэр и затем получается коллекция правил по имени, вызывающему метод GetNetworkRuleCollectionByName для объекта Firewall.</span><span class="sxs-lookup"><span data-stu-id="91524-120">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="91524-121">Имя набора правил для метода GetNetworkRuleCollectionByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="91524-121">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="91524-122">7. получение брандмауэра и удаление набора правил приложения по имени из брандмауэра</span><span class="sxs-lookup"><span data-stu-id="91524-122">7:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="91524-123">В этом примере извлекается брандмауэр, после чего коллекция правил удаляется по имени, вызывая метод RemoveApplicationRuleCollectionByName для объекта Firewall.</span><span class="sxs-lookup"><span data-stu-id="91524-123">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="91524-124">Имя набора правил для метода RemoveApplicationRuleCollectionByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="91524-124">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="91524-125">8. получение брандмауэра и удаление из него семейства сетевых правил по имени из брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="91524-125">8:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="91524-126">В этом примере извлекается брандмауэр, после чего коллекция правил удаляется по имени, вызывая метод RemoveNetworkRuleCollectionByName для объекта Firewall.</span><span class="sxs-lookup"><span data-stu-id="91524-126">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="91524-127">Имя набора правил для метода RemoveNetworkRuleCollectionByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="91524-127">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="91524-128">9: получение брандмауэра и его выделение</span><span class="sxs-lookup"><span data-stu-id="91524-128">9:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="91524-129">В этом примере извлекается брандмауэр и вызываются функции выделения ресурсов в брандмауэре, чтобы запустить службу брандмауэра с помощью конфигурации (коллекций приложений и сетевых правил), связанных с брандмауэром.</span><span class="sxs-lookup"><span data-stu-id="91524-129">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="91524-130">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91524-130">PARAMETERS</span></span>

### <span data-ttu-id="91524-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91524-131">-DefaultProfile</span></span>
<span data-ttu-id="91524-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91524-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91524-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="91524-133">-Name</span></span>
<span data-ttu-id="91524-134">Указывает имя брандмауэра, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="91524-134">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91524-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91524-135">-ResourceGroupName</span></span>
<span data-ttu-id="91524-136">Указывает имя группы ресурсов, к которой относится брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="91524-136">Specifies the name of the resource group that Firewall belongs to.</span></span>

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

### <span data-ttu-id="91524-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91524-137">CommonParameters</span></span>
<span data-ttu-id="91524-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91524-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91524-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91524-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91524-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91524-140">INPUTS</span></span>

### <span data-ttu-id="91524-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="91524-141">None</span></span>
<span data-ttu-id="91524-142">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="91524-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="91524-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91524-143">OUTPUTS</span></span>

### <span data-ttu-id="91524-144">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="91524-144">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="91524-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="91524-145">NOTES</span></span>

## <span data-ttu-id="91524-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91524-146">RELATED LINKS</span></span>

[<span data-ttu-id="91524-147">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="91524-147">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="91524-148">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="91524-148">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="91524-149">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="91524-149">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
