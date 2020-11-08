---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 3bfed7f4c980ab246f4e38d500860ccd4e2ef09f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078897"
---
# <span data-ttu-id="e048c-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e048c-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="e048c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e048c-102">SYNOPSIS</span></span>
<span data-ttu-id="e048c-103">Создание общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e048c-103">Creates a public IP address.</span></span>

## <span data-ttu-id="e048c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e048c-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-IpTag <PSPublicIpTag[]>]
 [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e048c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e048c-105">DESCRIPTION</span></span>
<span data-ttu-id="e048c-106">Командлет **New-AzPublicIpAddress** создает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e048c-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="e048c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e048c-107">EXAMPLES</span></span>

### <span data-ttu-id="e048c-108">Пример 1: создание нового общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="e048c-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="e048c-109">Эта команда создает новый ресурс общего IP-адреса. Создается запись DNS для $dnsPrefix. $location. cloudapp.azure.com, указывающая на общедоступный IP-адрес этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="e048c-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="e048c-110">Общедоступный IP-адрес немедленно выделяется этому ресурсу, так как для AllocationMethod задано значение "static".</span><span class="sxs-lookup"><span data-stu-id="e048c-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="e048c-111">Если задано значение Dynamic, общедоступный IP-адрес выделяется только при запуске (или создании) связанного ресурса (например, ВМ или подсистемы балансировки нагрузки).</span><span class="sxs-lookup"><span data-stu-id="e048c-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="e048c-112">Пример 2: создание общедоступного IP-адреса с помощью обратного доменного имени</span><span class="sxs-lookup"><span data-stu-id="e048c-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="e048c-113">Эта команда создает новый ресурс общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e048c-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="e048c-114">С помощью параметра-ReverseFqdn Azure создает PTR-запись DNS (обратный просмотр) для общедоступного IP-адреса, выделенного для этого ресурса, указывающего на $customFqdn, указанный в команде.</span><span class="sxs-lookup"><span data-stu-id="e048c-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="e048c-115">В качестве предварительной версии $customFqdn (скажем, webapp.contoso.com) должна иметь DNS-запись CNAME ("вперед-Просмотр"), указывающую на $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="e048c-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="e048c-116">Пример 3: создание нового общедоступного IP-адреса с помощью IpTag</span><span class="sxs-lookup"><span data-stu-id="e048c-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="e048c-117">Эта команда создает новый ресурс общего IP-адреса. Создается запись DNS для $dnsPrefix. $location. cloudapp.azure.com, указывающая на общедоступный IP-адрес этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="e048c-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="e048c-118">Общедоступный IP-адрес немедленно выделяется этому ресурсу, так как для AllocationMethod задано значение "static".</span><span class="sxs-lookup"><span data-stu-id="e048c-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="e048c-119">Если задано значение Dynamic, общедоступный IP-адрес выделяется только при запуске (или создании) связанного ресурса (например, ВМ или подсистемы балансировки нагрузки).</span><span class="sxs-lookup"><span data-stu-id="e048c-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="e048c-120">Iptag используется для специальных тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="e048c-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="e048c-121">Iptag можно указать с помощью New-AzPublicIpTag и передается в качестве входных данных через-IpTags.</span><span class="sxs-lookup"><span data-stu-id="e048c-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="e048c-122">Пример 4: создание нового общедоступного IP-адреса из префикса</span><span class="sxs-lookup"><span data-stu-id="e048c-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="e048c-123">Эта команда создает новый ресурс общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e048c-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="e048c-124">Создается запись DNS для $dnsPrefix. $location. cloudapp.azure.com, указывающая на общедоступный IP-адрес этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="e048c-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="e048c-125">Общедоступный IP-адрес немедленно выделяется для этого ресурса из указанного publicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="e048c-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="e048c-126">Этот параметр поддерживается только для "Standard" SKU и "static" AllocationMethod.</span><span class="sxs-lookup"><span data-stu-id="e048c-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="e048c-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e048c-127">PARAMETERS</span></span>

### <span data-ttu-id="e048c-128">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="e048c-128">-AllocationMethod</span></span>
<span data-ttu-id="e048c-129">Указывает метод выделения общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e048c-129">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="e048c-130">Допустимые значения этого параметра: Static или Dynamic.</span><span class="sxs-lookup"><span data-stu-id="e048c-130">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="e048c-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e048c-131">-AsJob</span></span>
<span data-ttu-id="e048c-132">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e048c-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e048c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e048c-133">-DefaultProfile</span></span>
<span data-ttu-id="e048c-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e048c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e048c-135">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="e048c-135">-DomainNameLabel</span></span>
<span data-ttu-id="e048c-136">Указывает относительное DNS-имя для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e048c-136">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="e048c-137">-Force</span><span class="sxs-lookup"><span data-stu-id="e048c-137">-Force</span></span>
<span data-ttu-id="e048c-138">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e048c-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e048c-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e048c-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e048c-140">Указывает тайм-фактор простоя (в минутах).</span><span class="sxs-lookup"><span data-stu-id="e048c-140">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="e048c-141">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e048c-141">-IpAddressVersion</span></span>
<span data-ttu-id="e048c-142">Указывает версию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e048c-142">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="e048c-143">-IpTag</span><span class="sxs-lookup"><span data-stu-id="e048c-143">-IpTag</span></span>
<span data-ttu-id="e048c-144">IpTag список.</span><span class="sxs-lookup"><span data-stu-id="e048c-144">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e048c-145">-Location</span><span class="sxs-lookup"><span data-stu-id="e048c-145">-Location</span></span>
<span data-ttu-id="e048c-146">Указывает область, в которой нужно создать общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e048c-146">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="e048c-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e048c-147">-Name</span></span>
<span data-ttu-id="e048c-148">Указывает имя общедоступного IP-адреса, который создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e048c-148">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e048c-149">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e048c-149">-PublicIpPrefix</span></span>
<span data-ttu-id="e048c-150">Указывает PSPublicIpPrefix, из которого будет выделяться общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e048c-150">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e048c-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e048c-151">-ResourceGroupName</span></span>
<span data-ttu-id="e048c-152">Указывает имя группы ресурсов, в которой нужно создать общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e048c-152">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="e048c-153">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="e048c-153">-ReverseFqdn</span></span>
<span data-ttu-id="e048c-154">Задает обратное полное доменное имя (FQDN).</span><span class="sxs-lookup"><span data-stu-id="e048c-154">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="e048c-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="e048c-155">-Sku</span></span>
<span data-ttu-id="e048c-156">Имя общедоступной IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e048c-156">The public IP Sku name.</span></span>

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

### <span data-ttu-id="e048c-157">-Тег</span><span class="sxs-lookup"><span data-stu-id="e048c-157">-Tag</span></span>
<span data-ttu-id="e048c-158">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="e048c-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e048c-159">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="e048c-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e048c-160">-Zone</span><span class="sxs-lookup"><span data-stu-id="e048c-160">-Zone</span></span>
<span data-ttu-id="e048c-161">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="e048c-161">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e048c-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e048c-162">-Confirm</span></span>
<span data-ttu-id="e048c-163">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e048c-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e048c-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e048c-164">-WhatIf</span></span>
<span data-ttu-id="e048c-165">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e048c-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e048c-166">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e048c-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e048c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e048c-167">CommonParameters</span></span>
<span data-ttu-id="e048c-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e048c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e048c-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e048c-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e048c-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e048c-170">INPUTS</span></span>

### <span data-ttu-id="e048c-171">System. String</span><span class="sxs-lookup"><span data-stu-id="e048c-171">System.String</span></span>

### <span data-ttu-id="e048c-172">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag []</span><span class="sxs-lookup"><span data-stu-id="e048c-172">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="e048c-173">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e048c-173">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="e048c-174">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e048c-174">System.Int32</span></span>

### <span data-ttu-id="e048c-175">System. String []</span><span class="sxs-lookup"><span data-stu-id="e048c-175">System.String[]</span></span>

### <span data-ttu-id="e048c-176">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e048c-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e048c-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e048c-177">OUTPUTS</span></span>

### <span data-ttu-id="e048c-178">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e048c-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="e048c-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="e048c-179">NOTES</span></span>

## <span data-ttu-id="e048c-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e048c-180">RELATED LINKS</span></span>

[<span data-ttu-id="e048c-181">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e048c-181">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="e048c-182">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e048c-182">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="e048c-183">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e048c-183">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
