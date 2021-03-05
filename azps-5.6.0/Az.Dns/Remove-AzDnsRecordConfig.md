---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: 07af143e1a1582670d15a15c356f673fef1f7590
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984780"
---
# <span data-ttu-id="6ead3-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6ead3-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="6ead3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ead3-102">SYNOPSIS</span></span>
<span data-ttu-id="6ead3-103">Удаляет DNS-запись из локального объекта набора записей.</span><span class="sxs-lookup"><span data-stu-id="6ead3-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="6ead3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6ead3-104">SYNTAX</span></span>

### <span data-ttu-id="6ead3-105">A</span><span class="sxs-lookup"><span data-stu-id="6ead3-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ead3-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="6ead3-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ead3-107">NS</span><span class="sxs-lookup"><span data-stu-id="6ead3-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ead3-108">MX</span><span class="sxs-lookup"><span data-stu-id="6ead3-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ead3-109">PTR</span><span class="sxs-lookup"><span data-stu-id="6ead3-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ead3-110">TXT</span><span class="sxs-lookup"><span data-stu-id="6ead3-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ead3-111">SRV</span><span class="sxs-lookup"><span data-stu-id="6ead3-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ead3-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="6ead3-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ead3-113">Caa</span><span class="sxs-lookup"><span data-stu-id="6ead3-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ead3-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ead3-114">DESCRIPTION</span></span>
<span data-ttu-id="6ead3-115">При этом из набора записей удаляется запись DNS системы доменных имен **(AzDnsRecordConfig).**</span><span class="sxs-lookup"><span data-stu-id="6ead3-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="6ead3-116">Объект **RecordSet** является автономным объектом, и его изменения не изменяют ответы DNS до запуска Set-AzDnsRecordSet, чтобы сохранить изменение службы DNS Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6ead3-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="6ead3-117">Чтобы удалить запись, все поля для этого типа записи должны в точности соответствовать.</span><span class="sxs-lookup"><span data-stu-id="6ead3-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="6ead3-118">Записи SOA добавлять и удалять нельзя.</span><span class="sxs-lookup"><span data-stu-id="6ead3-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="6ead3-119">Записи SOA создаются автоматически при создания зоны DNS и автоматическом удалении при удалении зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="6ead3-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="6ead3-120">Объект **RecordSet** можно передать этому cmdlet в качестве параметра или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="6ead3-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="6ead3-121">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6ead3-121">EXAMPLES</span></span>

### <span data-ttu-id="6ead3-122">Пример 1. Удаление записи A из набора записей</span><span class="sxs-lookup"><span data-stu-id="6ead3-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="6ead3-123">В этом примере запись A удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="6ead3-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="6ead3-124">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="6ead3-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="6ead3-125">Чтобы полностью удалить набор записей, см. видео Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6ead3-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6ead3-126">Пример 2. Удаление записи AAAA из набора записей</span><span class="sxs-lookup"><span data-stu-id="6ead3-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="6ead3-127">В этом примере запись AAAA удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="6ead3-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="6ead3-128">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="6ead3-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="6ead3-129">Чтобы полностью удалить набор записей, см. видео Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6ead3-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6ead3-130">Пример 3. Удаление записи CNAME из набора записей</span><span class="sxs-lookup"><span data-stu-id="6ead3-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="6ead3-131">В этом примере запись CNAME удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="6ead3-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="6ead3-132">Так как набор записей CNAME может содержать не более одной записи, результатом является пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="6ead3-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="6ead3-133">Пример 4. Удаление записи MX из набора записей</span><span class="sxs-lookup"><span data-stu-id="6ead3-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="6ead3-134">В этом примере запись MX удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="6ead3-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="6ead3-135">Имя записи "@" означает набор записей на апексе зоны.</span><span class="sxs-lookup"><span data-stu-id="6ead3-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="6ead3-136">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="6ead3-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6ead3-137">Чтобы полностью удалить набор записей, см. видео Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6ead3-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6ead3-138">Пример 5. Удаление записи NS из набора записей</span><span class="sxs-lookup"><span data-stu-id="6ead3-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="6ead3-139">В этом примере NS-запись удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="6ead3-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="6ead3-140">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="6ead3-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6ead3-141">Чтобы полностью удалить набор записей, см. видео Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6ead3-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6ead3-142">Пример 6. Удаление записи PTR из набора записей</span><span class="sxs-lookup"><span data-stu-id="6ead3-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="6ead3-143">В этом примере запись PTR удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="6ead3-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="6ead3-144">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="6ead3-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6ead3-145">Чтобы полностью удалить набор записей, см. видео Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6ead3-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6ead3-146">Пример 7. Удаление записи SRV из набора записей</span><span class="sxs-lookup"><span data-stu-id="6ead3-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="6ead3-147">В этом примере запись SRV удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="6ead3-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="6ead3-148">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="6ead3-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6ead3-149">Чтобы полностью удалить набор записей, см. видео Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6ead3-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6ead3-150">Пример 8. Удаление записи TXT из набора записей</span><span class="sxs-lookup"><span data-stu-id="6ead3-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="6ead3-151">В этом примере запись TXT удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="6ead3-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="6ead3-152">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="6ead3-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6ead3-153">Чтобы полностью удалить набор записей, см. видео Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6ead3-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="6ead3-154">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ead3-154">PARAMETERS</span></span>

### <span data-ttu-id="6ead3-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="6ead3-155">-CaaFlags</span></span>
<span data-ttu-id="6ead3-156">Флаги для добавляемой записи CAA.</span><span class="sxs-lookup"><span data-stu-id="6ead3-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="6ead3-157">Должен быть числом от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="6ead3-157">Must be a number between 0 and 255.</span></span>

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="6ead3-158">-CaaTag</span></span>
<span data-ttu-id="6ead3-159">Поле тега добавляемой записи CAA.</span><span class="sxs-lookup"><span data-stu-id="6ead3-159">The tag field of the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="6ead3-160">-CaaValue</span></span>
<span data-ttu-id="6ead3-161">Поле значения для добавляемой записи CAA.</span><span class="sxs-lookup"><span data-stu-id="6ead3-161">The value field for the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-162">-Cname</span><span class="sxs-lookup"><span data-stu-id="6ead3-162">-Cname</span></span>
<span data-ttu-id="6ead3-163">Указывает доменное имя для канонической записи (CNAME).</span><span class="sxs-lookup"><span data-stu-id="6ead3-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ead3-164">-DefaultProfile</span></span>
<span data-ttu-id="6ead3-165">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6ead3-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ead3-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="6ead3-166">-Exchange</span></span>
<span data-ttu-id="6ead3-167">Имя сервера обмена электронной почтой для записи обмена электронной почтой (MX).</span><span class="sxs-lookup"><span data-stu-id="6ead3-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="6ead3-168">-Ipv4Address</span></span>
<span data-ttu-id="6ead3-169">Определяет IPv4-адрес для записи A.</span><span class="sxs-lookup"><span data-stu-id="6ead3-169">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="6ead3-170">-Ipv6Address</span></span>
<span data-ttu-id="6ead3-171">Определяет IPv6-адрес для записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="6ead3-171">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="6ead3-172">-Nsdname</span></span>
<span data-ttu-id="6ead3-173">Сервер доменных имен для записи сервера доменных имен.</span><span class="sxs-lookup"><span data-stu-id="6ead3-173">Specifies the name server for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-174">-Port</span><span class="sxs-lookup"><span data-stu-id="6ead3-174">-Port</span></span>
<span data-ttu-id="6ead3-175">Порт для записи службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="6ead3-175">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-176">-Preference</span><span class="sxs-lookup"><span data-stu-id="6ead3-176">-Preference</span></span>
<span data-ttu-id="6ead3-177">Указывает параметр для записи MX.</span><span class="sxs-lookup"><span data-stu-id="6ead3-177">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-178">-Priority</span><span class="sxs-lookup"><span data-stu-id="6ead3-178">-Priority</span></span>
<span data-ttu-id="6ead3-179">Определяет приоритет для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="6ead3-179">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="6ead3-180">-Ptrdname</span></span>
<span data-ttu-id="6ead3-181">Указывает целевое доменное имя для записи указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="6ead3-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="6ead3-182">-RecordSet</span></span>
<span data-ttu-id="6ead3-183">Определяет объект **RecordSet,** содержащий удаляемую запись.</span><span class="sxs-lookup"><span data-stu-id="6ead3-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-184">-Target</span><span class="sxs-lookup"><span data-stu-id="6ead3-184">-Target</span></span>
<span data-ttu-id="6ead3-185">Указывает целевой объект для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="6ead3-185">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-186">-Value</span><span class="sxs-lookup"><span data-stu-id="6ead3-186">-Value</span></span>
<span data-ttu-id="6ead3-187">Определяет значение для записи TXT.</span><span class="sxs-lookup"><span data-stu-id="6ead3-187">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-188">-Weight</span><span class="sxs-lookup"><span data-stu-id="6ead3-188">-Weight</span></span>
<span data-ttu-id="6ead3-189">Определяет вес записи SRV.</span><span class="sxs-lookup"><span data-stu-id="6ead3-189">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ead3-190">CommonParameters</span></span>
<span data-ttu-id="6ead3-191">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ead3-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ead3-192">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ead3-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ead3-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ead3-193">INPUTS</span></span>

### <span data-ttu-id="6ead3-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6ead3-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="6ead3-195">System.String</span><span class="sxs-lookup"><span data-stu-id="6ead3-195">System.String</span></span>

### <span data-ttu-id="6ead3-196">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="6ead3-196">System.UInt16</span></span>

### <span data-ttu-id="6ead3-197">System.Byte</span><span class="sxs-lookup"><span data-stu-id="6ead3-197">System.Byte</span></span>

## <span data-ttu-id="6ead3-198">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6ead3-198">OUTPUTS</span></span>

### <span data-ttu-id="6ead3-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6ead3-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="6ead3-200">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6ead3-200">NOTES</span></span>

## <span data-ttu-id="6ead3-201">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ead3-201">RELATED LINKS</span></span>

[<span data-ttu-id="6ead3-202">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6ead3-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="6ead3-203">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6ead3-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="6ead3-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6ead3-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
