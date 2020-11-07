---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 308758942a160b95f1a5bea89a476c15a0dcf003
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909634"
---
# <span data-ttu-id="42923-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="42923-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="42923-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42923-102">SYNOPSIS</span></span>
<span data-ttu-id="42923-103">Создание общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="42923-103">Creates a public IP address.</span></span>

## <span data-ttu-id="42923-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42923-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42923-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42923-105">DESCRIPTION</span></span>
<span data-ttu-id="42923-106">Командлет **New-AzPublicIpAddress** создает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="42923-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="42923-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42923-107">EXAMPLES</span></span>

### <span data-ttu-id="42923-108">1: создание нового общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="42923-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="42923-109">Эта команда создает новый ресурс общего IP-адреса. Создается запись DNS для $dnsPrefix. $location. cloudapp.azure.com, указывающая на общедоступный IP-адрес этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="42923-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="42923-110">Общедоступный IP-адрес немедленно выделяется этому ресурсу, так как для AllocationMethod задано значение "static".</span><span class="sxs-lookup"><span data-stu-id="42923-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="42923-111">Если задано значение Dynamic, общедоступный IP-адрес выделяется только при запуске (или создании) связанного ресурса (например, ВМ или подсистемы балансировки нагрузки).</span><span class="sxs-lookup"><span data-stu-id="42923-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="42923-112">2. Создание общедоступного IP-адреса с помощью обратного доменного имени</span><span class="sxs-lookup"><span data-stu-id="42923-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="42923-113">Эта команда создает новый ресурс общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="42923-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="42923-114">С помощью параметра-ReverseFqdn Azure создает PTR-запись DNS (обратный просмотр) для общедоступного IP-адреса, выделенного для этого ресурса, указывающего на $customFqdn, указанный в команде.</span><span class="sxs-lookup"><span data-stu-id="42923-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="42923-115">В качестве предварительной версии $customFqdn (скажем, webapp.contoso.com) должна иметь DNS-запись CNAME ("вперед-Просмотр"), указывающую на $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="42923-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="42923-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42923-116">PARAMETERS</span></span>

### <span data-ttu-id="42923-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="42923-117">-AllocationMethod</span></span>
<span data-ttu-id="42923-118">Указывает метод выделения общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="42923-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="42923-119">Допустимые значения этого параметра: Static или Dynamic.</span><span class="sxs-lookup"><span data-stu-id="42923-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="42923-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42923-120">-AsJob</span></span>
<span data-ttu-id="42923-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="42923-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42923-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42923-122">-DefaultProfile</span></span>
<span data-ttu-id="42923-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42923-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42923-124">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="42923-124">-DomainNameLabel</span></span>
<span data-ttu-id="42923-125">Указывает относительное DNS-имя для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="42923-125">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="42923-126">-Force</span><span class="sxs-lookup"><span data-stu-id="42923-126">-Force</span></span>
<span data-ttu-id="42923-127">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="42923-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="42923-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="42923-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="42923-129">Указывает тайм-фактор простоя (в минутах).</span><span class="sxs-lookup"><span data-stu-id="42923-129">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="42923-130">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="42923-130">-IpAddressVersion</span></span>
<span data-ttu-id="42923-131">Указывает версию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="42923-131">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="42923-132">-Location</span><span class="sxs-lookup"><span data-stu-id="42923-132">-Location</span></span>
<span data-ttu-id="42923-133">Указывает область, в которой нужно создать общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="42923-133">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="42923-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42923-134">-Name</span></span>
<span data-ttu-id="42923-135">Указывает имя общедоступного IP-адреса, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="42923-135">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="42923-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42923-136">-ResourceGroupName</span></span>
<span data-ttu-id="42923-137">Указывает имя группы ресурсов, в которой нужно создать общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="42923-137">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="42923-138">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="42923-138">-ReverseFqdn</span></span>
<span data-ttu-id="42923-139">Задает обратное полное доменное имя (FQDN).</span><span class="sxs-lookup"><span data-stu-id="42923-139">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="42923-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="42923-140">-Sku</span></span>
<span data-ttu-id="42923-141">Имя общедоступной IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="42923-141">The public IP Sku name.</span></span>

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

### <span data-ttu-id="42923-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="42923-142">-Tag</span></span>
<span data-ttu-id="42923-143">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="42923-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="42923-144">Например:</span><span class="sxs-lookup"><span data-stu-id="42923-144">For example:</span></span>

<span data-ttu-id="42923-145">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="42923-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="42923-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="42923-146">-Zone</span></span>
<span data-ttu-id="42923-147">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="42923-147">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="42923-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42923-148">-Confirm</span></span>
<span data-ttu-id="42923-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42923-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42923-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42923-150">-WhatIf</span></span>
<span data-ttu-id="42923-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42923-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42923-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42923-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42923-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42923-153">CommonParameters</span></span>
<span data-ttu-id="42923-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42923-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42923-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42923-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42923-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42923-156">INPUTS</span></span>

## <span data-ttu-id="42923-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42923-157">OUTPUTS</span></span>

### <span data-ttu-id="42923-158">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="42923-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="42923-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="42923-159">NOTES</span></span>

## <span data-ttu-id="42923-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42923-160">RELATED LINKS</span></span>

[<span data-ttu-id="42923-161">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="42923-161">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="42923-162">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="42923-162">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="42923-163">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="42923-163">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
