---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: e00b31783554b8ea70760809c36f23a6a62575ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911231"
---
# <span data-ttu-id="cce4a-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="cce4a-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="cce4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cce4a-102">SYNOPSIS</span></span>
<span data-ttu-id="cce4a-103">Удаление записи DNS из локального объекта Set Record.</span><span class="sxs-lookup"><span data-stu-id="cce4a-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="cce4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cce4a-104">SYNTAX</span></span>

### <span data-ttu-id="cce4a-105">Помощью</span><span class="sxs-lookup"><span data-stu-id="cce4a-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="cce4a-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="cce4a-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="cce4a-107">СЛУЖБУ</span><span class="sxs-lookup"><span data-stu-id="cce4a-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="cce4a-108">МХ</span><span class="sxs-lookup"><span data-stu-id="cce4a-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="cce4a-109">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="cce4a-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="cce4a-110">ТХТ</span><span class="sxs-lookup"><span data-stu-id="cce4a-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="cce4a-111">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="cce4a-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="cce4a-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="cce4a-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="cce4a-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cce4a-113">DESCRIPTION</span></span>
<span data-ttu-id="cce4a-114">Командлет **Remove-AzDnsRecordConfig** УДАЛЯЕТ запись DNS (Domain Name System) из множества записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-114">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="cce4a-115">Объект **Recordset** является автономным объектом, и изменения в нем не изменяют ответы DNS, пока не будет запущен командлет Set-AzDnsRecordSet, чтобы сохранить изменения в службе Microsoft Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="cce4a-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="cce4a-116">Для удаления записи все поля для этого типа записей должны точно совпадать.</span><span class="sxs-lookup"><span data-stu-id="cce4a-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="cce4a-117">Вы не можете добавлять и удалять записи SOA.</span><span class="sxs-lookup"><span data-stu-id="cce4a-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="cce4a-118">Записи SOA автоматически создаются при создании зоны DNS и автоматически удаляются при удалении зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="cce4a-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="cce4a-119">Вы можете передать объект **набора записей** в этот командлет как параметр или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="cce4a-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="cce4a-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cce4a-120">EXAMPLES</span></span>

### <span data-ttu-id="cce4a-121">Пример 1: Удаление записи A из множества записей</span><span class="sxs-lookup"><span data-stu-id="cce4a-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="cce4a-122">В этом примере удаляется запись A из существующего набор записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="cce4a-123">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="cce4a-124">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="cce4a-124">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="cce4a-125">Пример 2: Удаление записи AAAA из набор записей</span><span class="sxs-lookup"><span data-stu-id="cce4a-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="cce4a-126">В этом примере удаляется запись AAAA из существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="cce4a-127">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="cce4a-128">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="cce4a-128">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="cce4a-129">Пример 3: Удаление записи CNAME из набор записей</span><span class="sxs-lookup"><span data-stu-id="cce4a-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="cce4a-130">В этом примере запись CNAME удаляется из существующего набор записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="cce4a-131">Так как набор записей CNAME может содержать не более одной записи, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="cce4a-132">Пример 4: Удаление записи MX из набор записей</span><span class="sxs-lookup"><span data-stu-id="cce4a-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="cce4a-133">В этом примере удаляется запись MX из существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="cce4a-134">Имя записи "@" обозначает набор записей на Апексе зоны.</span><span class="sxs-lookup"><span data-stu-id="cce4a-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="cce4a-135">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="cce4a-136">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="cce4a-136">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="cce4a-137">Пример 5: Удаление записи NS из множества записей</span><span class="sxs-lookup"><span data-stu-id="cce4a-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="cce4a-138">В этом примере удаляется запись NS из существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="cce4a-139">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="cce4a-140">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="cce4a-140">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="cce4a-141">Пример 6: Удаление записи PTR из набор записей</span><span class="sxs-lookup"><span data-stu-id="cce4a-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="cce4a-142">В этом примере удаляется запись PTR из существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="cce4a-143">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="cce4a-144">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="cce4a-144">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="cce4a-145">Пример 7: Удаление записи SRV из набор записей</span><span class="sxs-lookup"><span data-stu-id="cce4a-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="cce4a-146">В этом примере удаляется запись SRV из существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="cce4a-147">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="cce4a-148">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="cce4a-148">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="cce4a-149">Пример 8: Удаление записи TXT из множества записей</span><span class="sxs-lookup"><span data-stu-id="cce4a-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="cce4a-150">В этом примере запись TXT удаляется из существующего набор записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="cce4a-151">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="cce4a-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="cce4a-152">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="cce4a-152">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="cce4a-153">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cce4a-153">PARAMETERS</span></span>

### <span data-ttu-id="cce4a-154">-CNAME</span><span class="sxs-lookup"><span data-stu-id="cce4a-154">-Cname</span></span>
<span data-ttu-id="cce4a-155">Задает доменное имя для записи канонического имени (CNAME).</span><span class="sxs-lookup"><span data-stu-id="cce4a-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="cce4a-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="cce4a-156">-Exchange</span></span>
<span data-ttu-id="cce4a-157">Указывает имя почтового сервера для записи почтового обменника (MX).</span><span class="sxs-lookup"><span data-stu-id="cce4a-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="cce4a-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="cce4a-158">-Ipv4Address</span></span>
<span data-ttu-id="cce4a-159">Задает IPv4-адрес для записи A.</span><span class="sxs-lookup"><span data-stu-id="cce4a-159">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="cce4a-160">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="cce4a-160">-Ipv6Address</span></span>
<span data-ttu-id="cce4a-161">Задает IPv6-адрес для записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="cce4a-161">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="cce4a-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="cce4a-162">-Nsdname</span></span>
<span data-ttu-id="cce4a-163">Указывает сервер доменных имен для записи сервера доменных имен (NS).</span><span class="sxs-lookup"><span data-stu-id="cce4a-163">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="cce4a-164">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="cce4a-164">-Port</span></span>
<span data-ttu-id="cce4a-165">Указывает порт для записи службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="cce4a-165">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="cce4a-166">-Предпочтения</span><span class="sxs-lookup"><span data-stu-id="cce4a-166">-Preference</span></span>
<span data-ttu-id="cce4a-167">Задает приоритет MX-записи.</span><span class="sxs-lookup"><span data-stu-id="cce4a-167">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="cce4a-168">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="cce4a-168">-Priority</span></span>
<span data-ttu-id="cce4a-169">Указывает приоритет записи SRV.</span><span class="sxs-lookup"><span data-stu-id="cce4a-169">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="cce4a-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="cce4a-170">-Ptrdname</span></span>
<span data-ttu-id="cce4a-171">Указывает целевое доменное имя записи указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="cce4a-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="cce4a-172">-Набор записей</span><span class="sxs-lookup"><span data-stu-id="cce4a-172">-RecordSet</span></span>
<span data-ttu-id="cce4a-173">Указывает объект **набора записей** , содержащий удаляемую запись.</span><span class="sxs-lookup"><span data-stu-id="cce4a-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="cce4a-174">-Target</span><span class="sxs-lookup"><span data-stu-id="cce4a-174">-Target</span></span>
<span data-ttu-id="cce4a-175">Указывает целевой объект для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="cce4a-175">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="cce4a-176">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="cce4a-176">-Value</span></span>
<span data-ttu-id="cce4a-177">Задает значение для записи TXT.</span><span class="sxs-lookup"><span data-stu-id="cce4a-177">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="cce4a-178">-Weight</span><span class="sxs-lookup"><span data-stu-id="cce4a-178">-Weight</span></span>
<span data-ttu-id="cce4a-179">Определяет вес записи SRV.</span><span class="sxs-lookup"><span data-stu-id="cce4a-179">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="cce4a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce4a-180">CommonParameters</span></span>
<span data-ttu-id="cce4a-181">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cce4a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce4a-182">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cce4a-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce4a-183">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cce4a-183">INPUTS</span></span>

### <span data-ttu-id="cce4a-184">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cce4a-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="cce4a-185">Вы можете передать на этот командлет объект **DnsRecordSet** .</span><span class="sxs-lookup"><span data-stu-id="cce4a-185">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="cce4a-186">Это автономное представление набора записей и его обновления не изменяют ответы DNS, пока не будет запущен параметр SET-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="cce4a-186">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzDnsRecordSet.</span></span>

## <span data-ttu-id="cce4a-187">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cce4a-187">OUTPUTS</span></span>

### <span data-ttu-id="cce4a-188">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cce4a-188">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="cce4a-189">Этот командлет возвращает измененный объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="cce4a-189">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="cce4a-190">Пуск</span><span class="sxs-lookup"><span data-stu-id="cce4a-190">NOTES</span></span>

## <span data-ttu-id="cce4a-191">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cce4a-191">RELATED LINKS</span></span>

[<span data-ttu-id="cce4a-192">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="cce4a-192">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="cce4a-193">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cce4a-193">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="cce4a-194">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="cce4a-194">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
