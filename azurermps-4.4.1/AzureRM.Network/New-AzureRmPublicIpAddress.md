---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 8437c6037b52fd274415a59bea6ee66a2f9c0588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562475"
---
# <span data-ttu-id="2cb11-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2cb11-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="2cb11-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2cb11-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb11-103">Создание общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2cb11-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cb11-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2cb11-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cb11-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cb11-105">DESCRIPTION</span></span>
<span data-ttu-id="2cb11-106">Командлет **New-AzureRmPublicIpAddress** создает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2cb11-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="2cb11-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2cb11-107">EXAMPLES</span></span>

### <span data-ttu-id="2cb11-108">1: создание нового общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="2cb11-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="2cb11-109">Эта команда создает новый ресурс общего IP-адреса. Создается запись DNS для $dnsPrefix. $location. cloudapp.azure.com, указывающая на общедоступный IP-адрес этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="2cb11-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="2cb11-110">Общедоступный IP-адрес немедленно выделяется этому ресурсу, так как для AllocationMethod задано значение "static".</span><span class="sxs-lookup"><span data-stu-id="2cb11-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="2cb11-111">Если задано значение Dynamic, общедоступный IP-адрес выделяется только при запуске (или создании) связанного ресурса (например, ВМ или подсистемы балансировки нагрузки).</span><span class="sxs-lookup"><span data-stu-id="2cb11-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="2cb11-112">2. Создание общедоступного IP-адреса с помощью обратного доменного имени</span><span class="sxs-lookup"><span data-stu-id="2cb11-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="2cb11-113">Эта команда создает новый ресурс общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2cb11-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="2cb11-114">С помощью параметра-ReverseFqdn Azure создает PTR-запись DNS (обратный просмотр) для общедоступного IP-адреса, выделенного для этого ресурса, указывающего на $customFqdn, указанный в команде.</span><span class="sxs-lookup"><span data-stu-id="2cb11-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="2cb11-115">В качестве предварительной версии $customFqdn (скажем, webapp.contoso.com) должна иметь DNS-запись CNAME ("вперед-Просмотр"), указывающую на $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="2cb11-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="2cb11-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2cb11-116">PARAMETERS</span></span>

### <span data-ttu-id="2cb11-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="2cb11-117">-AllocationMethod</span></span>
<span data-ttu-id="2cb11-118">Указывает метод выделения общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2cb11-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="2cb11-119">Допустимые значения этого параметра: Static или Dynamic.</span><span class="sxs-lookup"><span data-stu-id="2cb11-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb11-120">-DefaultProfile</span></span>
<span data-ttu-id="2cb11-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cb11-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cb11-122">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="2cb11-122">-DomainNameLabel</span></span>
<span data-ttu-id="2cb11-123">Указывает относительное DNS-имя для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2cb11-123">Specifies the relative DNS name for a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb11-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2cb11-124">-Force</span></span>
<span data-ttu-id="2cb11-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2cb11-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2cb11-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2cb11-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2cb11-127">Указывает тайм-фактор простоя (в минутах).</span><span class="sxs-lookup"><span data-stu-id="2cb11-127">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="2cb11-128">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="2cb11-128">-IpAddressVersion</span></span>
<span data-ttu-id="2cb11-129">Указывает версию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="2cb11-129">Specifies the version of the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb11-130">-Location</span><span class="sxs-lookup"><span data-stu-id="2cb11-130">-Location</span></span>
<span data-ttu-id="2cb11-131">Указывает область, в которой нужно создать общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2cb11-131">Specifies the region in which to create a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb11-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2cb11-132">-Name</span></span>
<span data-ttu-id="2cb11-133">Указывает имя общедоступного IP-адреса, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2cb11-133">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb11-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb11-134">-ResourceGroupName</span></span>
<span data-ttu-id="2cb11-135">Указывает имя группы ресурсов, в которой нужно создать общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="2cb11-135">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="2cb11-136">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="2cb11-136">-ReverseFqdn</span></span>
<span data-ttu-id="2cb11-137">Задает обратное полное доменное имя (FQDN).</span><span class="sxs-lookup"><span data-stu-id="2cb11-137">Specifies a reverse fully qualified domain name (FQDN).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb11-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="2cb11-138">-Sku</span></span>
<span data-ttu-id="2cb11-139">Имя общедоступной IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2cb11-139">The public IP Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb11-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="2cb11-140">-Tag</span></span>
<span data-ttu-id="2cb11-141">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2cb11-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2cb11-142">Например:</span><span class="sxs-lookup"><span data-stu-id="2cb11-142">For example:</span></span>

<span data-ttu-id="2cb11-143">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2cb11-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cb11-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="2cb11-144">-Zone</span></span>
<span data-ttu-id="2cb11-145">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="2cb11-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="2cb11-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cb11-146">-Confirm</span></span>
<span data-ttu-id="2cb11-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2cb11-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb11-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cb11-148">-WhatIf</span></span>
<span data-ttu-id="2cb11-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2cb11-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cb11-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2cb11-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb11-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb11-151">CommonParameters</span></span>
<span data-ttu-id="2cb11-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2cb11-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb11-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cb11-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb11-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2cb11-154">INPUTS</span></span>

## <span data-ttu-id="2cb11-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cb11-155">OUTPUTS</span></span>

### <span data-ttu-id="2cb11-156">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2cb11-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="2cb11-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="2cb11-157">NOTES</span></span>

## <span data-ttu-id="2cb11-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cb11-158">RELATED LINKS</span></span>

[<span data-ttu-id="2cb11-159">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2cb11-159">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="2cb11-160">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2cb11-160">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="2cb11-161">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2cb11-161">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
