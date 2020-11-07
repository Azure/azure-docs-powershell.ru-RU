---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: 032090bb494718a6420f54960106fe9c5fa9871c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914034"
---
# <span data-ttu-id="2b4d9-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b4d9-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="2b4d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b4d9-102">SYNOPSIS</span></span>
<span data-ttu-id="2b4d9-103">Создание общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b4d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b4d9-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b4d9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b4d9-105">DESCRIPTION</span></span>
<span data-ttu-id="2b4d9-106">Командлет **New-AzureRmPublicIpAddress** создает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="2b4d9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b4d9-107">EXAMPLES</span></span>

### <span data-ttu-id="2b4d9-108">1: создание нового общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="2b4d9-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="2b4d9-109">Эта команда создает новый ресурс общего IP-адреса. Создается запись DNS для $dnsPrefix. $location. cloudapp.azure.com, указывающая на общедоступный IP-адрес этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="2b4d9-110">Общедоступный IP-адрес немедленно выделяется этому ресурсу, так как для AllocationMethod задано значение "static".</span><span class="sxs-lookup"><span data-stu-id="2b4d9-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="2b4d9-111">Если задано значение Dynamic, общедоступный IP-адрес выделяется только при запуске (или создании) связанного ресурса (например, ВМ или подсистемы балансировки нагрузки).</span><span class="sxs-lookup"><span data-stu-id="2b4d9-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="2b4d9-112">2. Создание общедоступного IP-адреса с помощью обратного доменного имени</span><span class="sxs-lookup"><span data-stu-id="2b4d9-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="2b4d9-113">Эта команда создает новый ресурс общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="2b4d9-114">С помощью параметра-ReverseFqdn Azure создает PTR-запись DNS (обратный просмотр) для общедоступного IP-адреса, выделенного для этого ресурса, указывающего на $customFqdn, указанный в команде.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="2b4d9-115">В качестве предварительной версии $customFqdn (скажем, webapp.contoso.com) должна иметь DNS-запись CNAME ("вперед-Просмотр"), указывающую на $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="2b4d9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b4d9-116">PARAMETERS</span></span>

### <span data-ttu-id="2b4d9-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="2b4d9-117">-AllocationMethod</span></span>
<span data-ttu-id="2b4d9-118">Указывает метод выделения общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="2b4d9-119">Допустимые значения этого параметра: Static или Dynamic.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="2b4d9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b4d9-120">-AsJob</span></span>
<span data-ttu-id="2b4d9-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2b4d9-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b4d9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b4d9-122">-DefaultProfile</span></span>
<span data-ttu-id="2b4d9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b4d9-124">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="2b4d9-124">-DomainNameLabel</span></span>
<span data-ttu-id="2b4d9-125">Указывает относительное DNS-имя для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-125">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="2b4d9-126">-Force</span><span class="sxs-lookup"><span data-stu-id="2b4d9-126">-Force</span></span>
<span data-ttu-id="2b4d9-127">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b4d9-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2b4d9-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2b4d9-129">Указывает тайм-фактор простоя (в минутах).</span><span class="sxs-lookup"><span data-stu-id="2b4d9-129">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="2b4d9-130">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="2b4d9-130">-IpAddressVersion</span></span>
<span data-ttu-id="2b4d9-131">Указывает версию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-131">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="2b4d9-132">-Location</span><span class="sxs-lookup"><span data-stu-id="2b4d9-132">-Location</span></span>
<span data-ttu-id="2b4d9-133">Указывает область, в которой нужно создать общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-133">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="2b4d9-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2b4d9-134">-Name</span></span>
<span data-ttu-id="2b4d9-135">Указывает имя общедоступного IP-адреса, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-135">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2b4d9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b4d9-136">-ResourceGroupName</span></span>
<span data-ttu-id="2b4d9-137">Указывает имя группы ресурсов, в которой нужно создать общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-137">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="2b4d9-138">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="2b4d9-138">-ReverseFqdn</span></span>
<span data-ttu-id="2b4d9-139">Задает обратное полное доменное имя (FQDN).</span><span class="sxs-lookup"><span data-stu-id="2b4d9-139">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="2b4d9-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="2b4d9-140">-Sku</span></span>
<span data-ttu-id="2b4d9-141">Имя общедоступной IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-141">The public IP Sku name.</span></span>

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

### <span data-ttu-id="2b4d9-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="2b4d9-142">-Tag</span></span>
<span data-ttu-id="2b4d9-143">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2b4d9-144">Например:</span><span class="sxs-lookup"><span data-stu-id="2b4d9-144">For example:</span></span>

<span data-ttu-id="2b4d9-145">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2b4d9-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2b4d9-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="2b4d9-146">-Zone</span></span>
<span data-ttu-id="2b4d9-147">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-147">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="2b4d9-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b4d9-148">-Confirm</span></span>
<span data-ttu-id="2b4d9-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b4d9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b4d9-150">-WhatIf</span></span>
<span data-ttu-id="2b4d9-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b4d9-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b4d9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b4d9-153">CommonParameters</span></span>
<span data-ttu-id="2b4d9-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b4d9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b4d9-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b4d9-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b4d9-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b4d9-156">INPUTS</span></span>

## <span data-ttu-id="2b4d9-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b4d9-157">OUTPUTS</span></span>

### <span data-ttu-id="2b4d9-158">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b4d9-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="2b4d9-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b4d9-159">NOTES</span></span>

## <span data-ttu-id="2b4d9-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b4d9-160">RELATED LINKS</span></span>

[<span data-ttu-id="2b4d9-161">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b4d9-161">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="2b4d9-162">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b4d9-162">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="2b4d9-163">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b4d9-163">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
