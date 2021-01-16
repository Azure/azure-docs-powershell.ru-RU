---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 8c48c7ec1f651348309c012275287bd88dd42bcc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391572"
---
# <span data-ttu-id="c8615-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c8615-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="c8615-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8615-102">SYNOPSIS</span></span>
<span data-ttu-id="c8615-103">Создается общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="c8615-103">Creates a public IP address.</span></span>

## <span data-ttu-id="c8615-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8615-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8615-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8615-105">DESCRIPTION</span></span>
<span data-ttu-id="c8615-106">Для **создания общего IP-адреса создается новый ip-адрес AzPublicIpAddress.**</span><span class="sxs-lookup"><span data-stu-id="c8615-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="c8615-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8615-107">EXAMPLES</span></span>

### <span data-ttu-id="c8615-108">Пример 1. Создание нового общего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="c8615-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="c8615-109">Эта команда создает общедоступный IP-адресный ресурс. DNS-запись создается для $dnsPrefix.$location.cloudapp.azure.com, указывав на общедоступный IP-адрес этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c8615-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="c8615-110">Общедоступный IP-адрес сразу же выделяется этому ресурсу, так как для -AllocationMethod задано "Статическое".</span><span class="sxs-lookup"><span data-stu-id="c8615-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="c8615-111">Если этот адрес указан как динамический, то общедоступный IP-адрес выделяется только при запуске (или создании) связанного ресурса (например, VM или балансиров нагрузки).</span><span class="sxs-lookup"><span data-stu-id="c8615-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="c8615-112">Пример 2. Создание общего IP-адреса с обратным FQDN</span><span class="sxs-lookup"><span data-stu-id="c8615-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="c8615-113">Эта команда создает общедоступный IP-адресный ресурс.</span><span class="sxs-lookup"><span data-stu-id="c8615-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="c8615-114">С помощью параметра -ReverseFqdn Azure создает запись DNS PTR (обратный просмотр) для обще доступного IP-адреса, выделенного для ресурса, указывая на $customFqdn, указанное в команде.</span><span class="sxs-lookup"><span data-stu-id="c8615-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="c8615-115">В качестве предварительного требования у $customFqdn (например, webapp.contoso.com) должна быть запись CNAME DNS (forward-lookup), указывка на $dnsPrefix.$location.cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="c8615-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="c8615-116">Пример 3. Создание нового общего IP-адреса с помощью IpTag</span><span class="sxs-lookup"><span data-stu-id="c8615-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="c8615-117">Эта команда создает общедоступный IP-адресный ресурс. DNS-запись создается для $dnsPrefix.$location.cloudapp.azure.com, указывав на общедоступный IP-адрес этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c8615-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="c8615-118">Общедоступный IP-адрес сразу же выделяется этому ресурсу, так как для -AllocationMethod задано "Статическое".</span><span class="sxs-lookup"><span data-stu-id="c8615-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="c8615-119">Если этот адрес указан как динамический, то общедоступный IP-адрес выделяется только при запуске (или создании) связанного ресурса (например, VM или балансиров нагрузки).</span><span class="sxs-lookup"><span data-stu-id="c8615-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="c8615-120">Iptag используется для конкретных тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="c8615-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="c8615-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IPTags.</span><span class="sxs-lookup"><span data-stu-id="c8615-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="c8615-122">Пример 4. Создание нового общего IP-адреса с префикса</span><span class="sxs-lookup"><span data-stu-id="c8615-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="c8615-123">Эта команда создает общедоступный IP-адресный ресурс.</span><span class="sxs-lookup"><span data-stu-id="c8615-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="c8615-124">DNS-запись создается для $dnsPrefix.$location.cloudapp.azure.com, указывав на общедоступный IP-адрес этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c8615-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="c8615-125">Общедоступный IP-адрес сразу же выделяется этому ресурсу из указанной publicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="c8615-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="c8615-126">Этот параметр поддерживается только для SKU стандартных и статических средств размещенияMethod.</span><span class="sxs-lookup"><span data-stu-id="c8615-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

### <span data-ttu-id="c8615-127">Пример 5. Создание глобального общего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="c8615-127">Example 5: Create a new global public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

<span data-ttu-id="c8615-128">Эта команда создает новый глобальный общедоступный IP-адресный ресурс. DNS-запись создается для $dnsPrefix.$location.cloudapp.azure.com, указывав на общедоступный IP-адрес этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c8615-128">This command creates a new global public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="c8615-129">Этому ресурсу сразу же выделяется глобальный общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="c8615-129">A global public IP address is immediately allocated to this resource.</span></span>
<span data-ttu-id="c8615-130">Этот параметр поддерживается только для стандартных SKU и статического параметра AllocationMethod.</span><span class="sxs-lookup"><span data-stu-id="c8615-130">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="c8615-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8615-131">PARAMETERS</span></span>

### <span data-ttu-id="c8615-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="c8615-132">-AllocationMethod</span></span>
<span data-ttu-id="c8615-133">Метод выделения общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="c8615-133">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="c8615-134">Допустимыми значениями для этого параметра являются статические или динамические.</span><span class="sxs-lookup"><span data-stu-id="c8615-134">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="c8615-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8615-135">-AsJob</span></span>
<span data-ttu-id="c8615-136">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c8615-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8615-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8615-137">-DefaultProfile</span></span>
<span data-ttu-id="c8615-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8615-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8615-139">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="c8615-139">-DomainNameLabel</span></span>
<span data-ttu-id="c8615-140">Указывает относительное имя DNS для общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="c8615-140">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="c8615-141">-Force</span><span class="sxs-lookup"><span data-stu-id="c8615-141">-Force</span></span>
<span data-ttu-id="c8615-142">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c8615-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c8615-143">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c8615-143">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c8615-144">Указывает, что время ожидания неа установлено в минутах.</span><span class="sxs-lookup"><span data-stu-id="c8615-144">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="c8615-145">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="c8615-145">-IpAddressVersion</span></span>
<span data-ttu-id="c8615-146">Определяет версию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="c8615-146">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="c8615-147">-IpTag</span><span class="sxs-lookup"><span data-stu-id="c8615-147">-IpTag</span></span>
<span data-ttu-id="c8615-148">Список IPTag.</span><span class="sxs-lookup"><span data-stu-id="c8615-148">IpTag List.</span></span>

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

### <span data-ttu-id="c8615-149">-Location</span><span class="sxs-lookup"><span data-stu-id="c8615-149">-Location</span></span>
<span data-ttu-id="c8615-150">Определяет регион, в котором нужно создать общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="c8615-150">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="c8615-151">-Name</span><span class="sxs-lookup"><span data-stu-id="c8615-151">-Name</span></span>
<span data-ttu-id="c8615-152">Указывает имя общего IP-адреса, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8615-152">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c8615-153">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8615-153">-PublicIpPrefix</span></span>
<span data-ttu-id="c8615-154">Определяет PSPublicIpPrefix, с которого нужно выделить общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="c8615-154">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="c8615-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8615-155">-ResourceGroupName</span></span>
<span data-ttu-id="c8615-156">Имя группы ресурсов, в которой нужно создать общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="c8615-156">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="c8615-157">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="c8615-157">-ReverseFqdn</span></span>
<span data-ttu-id="c8615-158">Указывает обратное полное доменное имя.</span><span class="sxs-lookup"><span data-stu-id="c8615-158">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="c8615-159">-SKU</span><span class="sxs-lookup"><span data-stu-id="c8615-159">-Sku</span></span>
<span data-ttu-id="c8615-160">Имя SKU общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="c8615-160">The public IP Sku name.</span></span>

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

### <span data-ttu-id="c8615-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="c8615-161">-Tag</span></span>
<span data-ttu-id="c8615-162">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="c8615-162">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c8615-163">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c8615-163">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c8615-164">-Tier</span><span class="sxs-lookup"><span data-stu-id="c8615-164">-Tier</span></span>
<span data-ttu-id="c8615-165">Уровень SKU для общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="c8615-165">The public IP Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8615-166">-Zone</span><span class="sxs-lookup"><span data-stu-id="c8615-166">-Zone</span></span>
<span data-ttu-id="c8615-167">Список зон доступности, обозначающий IP-адрес, выделенный для ресурса.</span><span class="sxs-lookup"><span data-stu-id="c8615-167">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="c8615-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8615-168">-Confirm</span></span>
<span data-ttu-id="c8615-169">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8615-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8615-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8615-170">-WhatIf</span></span>
<span data-ttu-id="c8615-171">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8615-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8615-172">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c8615-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8615-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8615-173">CommonParameters</span></span>
<span data-ttu-id="c8615-174">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8615-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8615-175">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8615-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8615-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8615-176">INPUTS</span></span>

### <span data-ttu-id="c8615-177">System.String</span><span class="sxs-lookup"><span data-stu-id="c8615-177">System.String</span></span>

### <span data-ttu-id="c8615-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span><span class="sxs-lookup"><span data-stu-id="c8615-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="c8615-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c8615-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="c8615-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c8615-180">System.Int32</span></span>

### <span data-ttu-id="c8615-181">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c8615-181">System.String[]</span></span>

### <span data-ttu-id="c8615-182">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c8615-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c8615-183">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8615-183">OUTPUTS</span></span>

### <span data-ttu-id="c8615-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c8615-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="c8615-185">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8615-185">NOTES</span></span>

## <span data-ttu-id="c8615-186">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8615-186">RELATED LINKS</span></span>

[<span data-ttu-id="c8615-187">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c8615-187">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="c8615-188">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c8615-188">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="c8615-189">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c8615-189">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
