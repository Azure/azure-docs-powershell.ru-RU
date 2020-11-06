---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 98ea4632004787626237e5845f3c573b51a91934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568567"
---
# <span data-ttu-id="af570-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="af570-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="af570-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af570-102">SYNOPSIS</span></span>
<span data-ttu-id="af570-103">Создание общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="af570-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af570-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af570-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af570-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af570-105">DESCRIPTION</span></span>
<span data-ttu-id="af570-106">Командлет **New-AzureRmPublicIpAddress** создает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="af570-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="af570-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af570-107">EXAMPLES</span></span>

### <span data-ttu-id="af570-108">1: создание нового общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="af570-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="af570-109">Эта команда создает новый ресурс общего IP-адреса. Создается запись DNS для $dnsPrefix. $location. cloudapp.azure.com, указывающая на общедоступный IP-адрес этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="af570-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="af570-110">Общедоступный IP-адрес немедленно выделяется этому ресурсу, так как для AllocationMethod задано значение "static".</span><span class="sxs-lookup"><span data-stu-id="af570-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="af570-111">Если задано значение Dynamic, общедоступный IP-адрес выделяется только при запуске (или создании) связанного ресурса (например, ВМ или подсистемы балансировки нагрузки).</span><span class="sxs-lookup"><span data-stu-id="af570-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="af570-112">2. Создание общедоступного IP-адреса с помощью обратного доменного имени</span><span class="sxs-lookup"><span data-stu-id="af570-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="af570-113">Эта команда создает новый ресурс общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="af570-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="af570-114">С помощью параметра-ReverseFqdn Azure создает PTR-запись DNS (обратный просмотр) для общедоступного IP-адреса, выделенного для этого ресурса, указывающего на $customFqdn, указанный в команде.</span><span class="sxs-lookup"><span data-stu-id="af570-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="af570-115">В качестве предварительной версии $customFqdn (скажем, webapp.contoso.com) должна иметь DNS-запись CNAME ("вперед-Просмотр"), указывающую на $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="af570-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="af570-116">3: создание нового общедоступного IP-адреса с помощью IpTag</span><span class="sxs-lookup"><span data-stu-id="af570-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="af570-117">Эта команда создает новый ресурс общего IP-адреса. Создается запись DNS для $dnsPrefix. $location. cloudapp.azure.com, указывающая на общедоступный IP-адрес этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="af570-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="af570-118">Общедоступный IP-адрес немедленно выделяется этому ресурсу, так как для AllocationMethod задано значение "static".</span><span class="sxs-lookup"><span data-stu-id="af570-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="af570-119">Если задано значение Dynamic, общедоступный IP-адрес выделяется только при запуске (или создании) связанного ресурса (например, ВМ или подсистемы балансировки нагрузки).</span><span class="sxs-lookup"><span data-stu-id="af570-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="af570-120">Iptag используется для специальных тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="af570-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="af570-121">Iptag можно указать с помощью New-AzureRmPublicIpTag и передается в качестве входных данных через-IpTags.</span><span class="sxs-lookup"><span data-stu-id="af570-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

## <span data-ttu-id="af570-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af570-122">PARAMETERS</span></span>

### <span data-ttu-id="af570-123">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="af570-123">-AllocationMethod</span></span>
<span data-ttu-id="af570-124">Указывает метод выделения общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="af570-124">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="af570-125">Допустимые значения этого параметра: Static или Dynamic.</span><span class="sxs-lookup"><span data-stu-id="af570-125">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af570-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af570-126">-AsJob</span></span>
<span data-ttu-id="af570-127">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="af570-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af570-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af570-128">-DefaultProfile</span></span>
<span data-ttu-id="af570-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af570-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af570-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="af570-130">-DomainNameLabel</span></span>
<span data-ttu-id="af570-131">Указывает относительное DNS-имя для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="af570-131">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="af570-132">-Force</span><span class="sxs-lookup"><span data-stu-id="af570-132">-Force</span></span>
<span data-ttu-id="af570-133">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="af570-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af570-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="af570-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="af570-135">Указывает тайм-фактор простоя (в минутах).</span><span class="sxs-lookup"><span data-stu-id="af570-135">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af570-136">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="af570-136">-IpAddressVersion</span></span>
<span data-ttu-id="af570-137">Указывает версию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="af570-137">Specifies the version of the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af570-138">-IpTag</span><span class="sxs-lookup"><span data-stu-id="af570-138">-IpTag</span></span>
<span data-ttu-id="af570-139">IpTag список.</span><span class="sxs-lookup"><span data-stu-id="af570-139">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af570-140">-Location</span><span class="sxs-lookup"><span data-stu-id="af570-140">-Location</span></span>
<span data-ttu-id="af570-141">Указывает область, в которой нужно создать общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="af570-141">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="af570-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af570-142">-Name</span></span>
<span data-ttu-id="af570-143">Указывает имя общедоступного IP-адреса, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="af570-143">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="af570-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af570-144">-ResourceGroupName</span></span>
<span data-ttu-id="af570-145">Указывает имя группы ресурсов, в которой нужно создать общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="af570-145">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="af570-146">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="af570-146">-ReverseFqdn</span></span>
<span data-ttu-id="af570-147">Задает обратное полное доменное имя (FQDN).</span><span class="sxs-lookup"><span data-stu-id="af570-147">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="af570-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="af570-148">-Sku</span></span>
<span data-ttu-id="af570-149">Имя общедоступной IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="af570-149">The public IP Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af570-150">-Тег</span><span class="sxs-lookup"><span data-stu-id="af570-150">-Tag</span></span>
<span data-ttu-id="af570-151">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="af570-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="af570-152">Например:</span><span class="sxs-lookup"><span data-stu-id="af570-152">For example:</span></span>

<span data-ttu-id="af570-153">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="af570-153">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="af570-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="af570-154">-Zone</span></span>
<span data-ttu-id="af570-155">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="af570-155">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af570-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af570-156">-Confirm</span></span>
<span data-ttu-id="af570-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="af570-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af570-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af570-158">-WhatIf</span></span>
<span data-ttu-id="af570-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="af570-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af570-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="af570-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af570-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af570-161">CommonParameters</span></span>
<span data-ttu-id="af570-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af570-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af570-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af570-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af570-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af570-164">INPUTS</span></span>

### <span data-ttu-id="af570-165">Ничего</span><span class="sxs-lookup"><span data-stu-id="af570-165">None</span></span>
<span data-ttu-id="af570-166">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="af570-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af570-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af570-167">OUTPUTS</span></span>

### <span data-ttu-id="af570-168">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="af570-168">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="af570-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="af570-169">NOTES</span></span>

## <span data-ttu-id="af570-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af570-170">RELATED LINKS</span></span>

[<span data-ttu-id="af570-171">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="af570-171">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="af570-172">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="af570-172">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="af570-173">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="af570-173">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
