---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: a5f3871f0ab63d875c2a0389c5585f0871fb0cb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910422"
---
# <span data-ttu-id="31c1b-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="31c1b-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="31c1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="31c1b-103">Добавляет запись DNS в локальный объект локального множества записей.</span><span class="sxs-lookup"><span data-stu-id="31c1b-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="31c1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31c1b-104">SYNTAX</span></span>

### <span data-ttu-id="31c1b-105">Помощью</span><span class="sxs-lookup"><span data-stu-id="31c1b-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="31c1b-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="31c1b-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="31c1b-107">СЛУЖБУ</span><span class="sxs-lookup"><span data-stu-id="31c1b-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="31c1b-108">МХ</span><span class="sxs-lookup"><span data-stu-id="31c1b-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="31c1b-109">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="31c1b-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="31c1b-110">ТХТ</span><span class="sxs-lookup"><span data-stu-id="31c1b-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="31c1b-111">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="31c1b-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="31c1b-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="31c1b-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="31c1b-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31c1b-113">DESCRIPTION</span></span>
<span data-ttu-id="31c1b-114">Командлет **Add-AzDnsRecordConfig** добавляет запись DNS (Domain Name System) в объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="31c1b-114">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="31c1b-115">Объект **Recordset** является автономным объектом, и изменения в нем не изменяют ответы DNS, пока не будет запущен командлет Set-AzDnsRecordSet, чтобы сохранить изменения в службе Microsoft Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="31c1b-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="31c1b-116">Записи SOA создаются при создании зоны DNS и удаляются при удалении зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="31c1b-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="31c1b-117">Вы не можете добавлять и удалять записи SOA, но можете редактировать их.</span><span class="sxs-lookup"><span data-stu-id="31c1b-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="31c1b-118">Вы можете передать объект **набора записей** в этот командлет как параметр или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="31c1b-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="31c1b-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31c1b-119">EXAMPLES</span></span>

### <span data-ttu-id="31c1b-120">Пример 1: Добавление записи A в набор записей</span><span class="sxs-lookup"><span data-stu-id="31c1b-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="31c1b-121">В этом примере к существующему набору записей добавляется запись A.</span><span class="sxs-lookup"><span data-stu-id="31c1b-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="31c1b-122">Пример 2: Добавление записи AAAA в набор записей</span><span class="sxs-lookup"><span data-stu-id="31c1b-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="31c1b-123">В этом примере добавляется запись AAAA в существующий наборы записей.</span><span class="sxs-lookup"><span data-stu-id="31c1b-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="31c1b-124">Пример 3: Добавление записи CNAME в набор записей</span><span class="sxs-lookup"><span data-stu-id="31c1b-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="31c1b-125">В этом примере добавляется запись CNAME к существующему набору записей.</span><span class="sxs-lookup"><span data-stu-id="31c1b-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="31c1b-126">Так как набор записей CNAME может содержать не более одной записи, сначала должна быть пустая набор записей, или существующие записи должны быть удалены с помощью Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="31c1b-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="31c1b-127">Пример 4: Добавление записи MX в набор записей</span><span class="sxs-lookup"><span data-stu-id="31c1b-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="31c1b-128">В этом примере добавляется запись MX в существующий наборы записей.</span><span class="sxs-lookup"><span data-stu-id="31c1b-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="31c1b-129">Имя записи "@" обозначает набор записей на Апексе зоны.</span><span class="sxs-lookup"><span data-stu-id="31c1b-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="31c1b-130">Пример 5: Добавление записи NS в набор записей</span><span class="sxs-lookup"><span data-stu-id="31c1b-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="31c1b-131">В этом примере добавляется запись NS для существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="31c1b-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="31c1b-132">Пример 6: Добавление записи PTR в набор записей</span><span class="sxs-lookup"><span data-stu-id="31c1b-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="31c1b-133">В этом примере к существующему набору записей добавляется запись PTR.</span><span class="sxs-lookup"><span data-stu-id="31c1b-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="31c1b-134">Пример 7: Добавление записи SRV в набор записей</span><span class="sxs-lookup"><span data-stu-id="31c1b-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="31c1b-135">В этом примере добавляется запись SRV для существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="31c1b-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="31c1b-136">Пример 8: Добавление записи TXT в набор записей</span><span class="sxs-lookup"><span data-stu-id="31c1b-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="31c1b-137">В этом примере к существующему набору записей добавляется запись TXT.</span><span class="sxs-lookup"><span data-stu-id="31c1b-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="31c1b-138">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31c1b-138">PARAMETERS</span></span>

### <span data-ttu-id="31c1b-139">-CNAME</span><span class="sxs-lookup"><span data-stu-id="31c1b-139">-Cname</span></span>
<span data-ttu-id="31c1b-140">Задает доменное имя для записи канонического имени (CNAME).</span><span class="sxs-lookup"><span data-stu-id="31c1b-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="31c1b-141">-Exchange</span></span>
<span data-ttu-id="31c1b-142">Указывает имя почтового сервера для записи почтового обменника (MX).</span><span class="sxs-lookup"><span data-stu-id="31c1b-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="31c1b-143">-Ipv4Address</span></span>
<span data-ttu-id="31c1b-144">Задает IPv4-адрес для записи A.</span><span class="sxs-lookup"><span data-stu-id="31c1b-144">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-145">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="31c1b-145">-Ipv6Address</span></span>
<span data-ttu-id="31c1b-146">Задает IPv6-адрес для записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="31c1b-146">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="31c1b-147">-Nsdname</span></span>
<span data-ttu-id="31c1b-148">Указывает имя сервера доменных имен для записи сервера доменных имен (NS).</span><span class="sxs-lookup"><span data-stu-id="31c1b-148">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-149">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="31c1b-149">-Port</span></span>
<span data-ttu-id="31c1b-150">Указывает порт для записи службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="31c1b-150">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-151">-Предпочтения</span><span class="sxs-lookup"><span data-stu-id="31c1b-151">-Preference</span></span>
<span data-ttu-id="31c1b-152">Задает приоритет MX-записи.</span><span class="sxs-lookup"><span data-stu-id="31c1b-152">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-153">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="31c1b-153">-Priority</span></span>
<span data-ttu-id="31c1b-154">Указывает приоритет записи SRV.</span><span class="sxs-lookup"><span data-stu-id="31c1b-154">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="31c1b-155">-Ptrdname</span></span>
<span data-ttu-id="31c1b-156">Указывает целевое доменное имя записи ресурса указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="31c1b-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-157">-Набор записей</span><span class="sxs-lookup"><span data-stu-id="31c1b-157">-RecordSet</span></span>
<span data-ttu-id="31c1b-158">Указывает объект **набора записей** , который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="31c1b-158">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-159">-Target</span><span class="sxs-lookup"><span data-stu-id="31c1b-159">-Target</span></span>
<span data-ttu-id="31c1b-160">Указывает целевой объект для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="31c1b-160">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-161">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="31c1b-161">-Value</span></span>
<span data-ttu-id="31c1b-162">Задает значение для записи TXT.</span><span class="sxs-lookup"><span data-stu-id="31c1b-162">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-163">-Weight</span><span class="sxs-lookup"><span data-stu-id="31c1b-163">-Weight</span></span>
<span data-ttu-id="31c1b-164">Определяет вес записи SRV.</span><span class="sxs-lookup"><span data-stu-id="31c1b-164">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c1b-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c1b-165">CommonParameters</span></span>
<span data-ttu-id="31c1b-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31c1b-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c1b-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31c1b-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c1b-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31c1b-168">INPUTS</span></span>

### <span data-ttu-id="31c1b-169">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="31c1b-169">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="31c1b-170">Вы можете передать в этот командлет объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="31c1b-170">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="31c1b-171">Это автономное представление **набора записей** , и изменения в нем не изменяют ответы DNS до тех пор, пока вы не запустили командлет Set-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="31c1b-171">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="31c1b-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31c1b-172">OUTPUTS</span></span>

### <span data-ttu-id="31c1b-173">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="31c1b-173">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="31c1b-174">Этот командлет возвращает измененный объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="31c1b-174">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="31c1b-175">Кроме того, переданный объект изменяется напрямую.</span><span class="sxs-lookup"><span data-stu-id="31c1b-175">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="31c1b-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="31c1b-176">NOTES</span></span>

## <span data-ttu-id="31c1b-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31c1b-177">RELATED LINKS</span></span>

[<span data-ttu-id="31c1b-178">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="31c1b-178">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="31c1b-179">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="31c1b-179">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="31c1b-180">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="31c1b-180">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
