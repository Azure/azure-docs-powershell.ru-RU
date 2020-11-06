---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 1e0a7de22b459f5d87c4a79bb91ef4c36f88ad77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566636"
---
# <span data-ttu-id="c5147-101">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c5147-101">Remove-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="c5147-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5147-102">SYNOPSIS</span></span>
<span data-ttu-id="c5147-103">Удаление записи DNS из локального объекта Set Record.</span><span class="sxs-lookup"><span data-stu-id="c5147-103">Removes a DNS record from a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5147-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5147-104">SYNTAX</span></span>

### <span data-ttu-id="c5147-105">Помощью</span><span class="sxs-lookup"><span data-stu-id="c5147-105">A</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5147-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="c5147-106">AAAA</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5147-107">СЛУЖБУ</span><span class="sxs-lookup"><span data-stu-id="c5147-107">NS</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5147-108">МХ</span><span class="sxs-lookup"><span data-stu-id="c5147-108">MX</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5147-109">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="c5147-109">PTR</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5147-110">ТХТ</span><span class="sxs-lookup"><span data-stu-id="c5147-110">TXT</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5147-111">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="c5147-111">SRV</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5147-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="c5147-112">CNAME</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5147-113">Caa</span><span class="sxs-lookup"><span data-stu-id="c5147-113">Caa</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5147-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5147-114">DESCRIPTION</span></span>
<span data-ttu-id="c5147-115">Командлет **Remove-AzureRmDnsRecordConfig** УДАЛЯЕТ запись DNS (Domain Name System) из множества записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-115">The **Remove-AzureRmDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="c5147-116">Объект **Recordset** является автономным объектом, и изменения в нем не изменяют ответы DNS, пока не будет запущен командлет Set-AzureRmDnsRecordSet, чтобы сохранить изменения в службе Microsoft Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="c5147-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="c5147-117">Для удаления записи все поля для этого типа записей должны точно совпадать.</span><span class="sxs-lookup"><span data-stu-id="c5147-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="c5147-118">Вы не можете добавлять и удалять записи SOA.</span><span class="sxs-lookup"><span data-stu-id="c5147-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="c5147-119">Записи SOA автоматически создаются при создании зоны DNS и автоматически удаляются при удалении зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="c5147-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="c5147-120">Вы можете передать объект **набора записей** в этот командлет как параметр или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="c5147-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="c5147-121">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5147-121">EXAMPLES</span></span>

### <span data-ttu-id="c5147-122">Пример 1: Удаление записи A из множества записей</span><span class="sxs-lookup"><span data-stu-id="c5147-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5147-123">В этом примере удаляется запись A из существующего набор записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="c5147-124">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="c5147-125">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5147-125">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="c5147-126">Пример 2: Удаление записи AAAA из набор записей</span><span class="sxs-lookup"><span data-stu-id="c5147-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5147-127">В этом примере удаляется запись AAAA из существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="c5147-128">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="c5147-129">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5147-129">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="c5147-130">Пример 3: Удаление записи CNAME из набор записей</span><span class="sxs-lookup"><span data-stu-id="c5147-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5147-131">В этом примере запись CNAME удаляется из существующего набор записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="c5147-132">Так как набор записей CNAME может содержать не более одной записи, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="c5147-133">Пример 4: Удаление записи MX из набор записей</span><span class="sxs-lookup"><span data-stu-id="c5147-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5147-134">В этом примере удаляется запись MX из существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="c5147-135">Имя записи "@" обозначает набор записей на Апексе зоны.</span><span class="sxs-lookup"><span data-stu-id="c5147-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="c5147-136">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="c5147-137">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5147-137">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="c5147-138">Пример 5: Удаление записи NS из множества записей</span><span class="sxs-lookup"><span data-stu-id="c5147-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5147-139">В этом примере удаляется запись NS из существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="c5147-140">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="c5147-141">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5147-141">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="c5147-142">Пример 6: Удаление записи PTR из набор записей</span><span class="sxs-lookup"><span data-stu-id="c5147-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5147-143">В этом примере удаляется запись PTR из существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="c5147-144">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="c5147-145">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5147-145">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="c5147-146">Пример 7: Удаление записи SRV из набор записей</span><span class="sxs-lookup"><span data-stu-id="c5147-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5147-147">В этом примере удаляется запись SRV из существующего множества записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="c5147-148">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="c5147-149">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5147-149">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="c5147-150">Пример 8: Удаление записи TXT из множества записей</span><span class="sxs-lookup"><span data-stu-id="c5147-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="c5147-151">В этом примере запись TXT удаляется из существующего набор записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="c5147-152">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="c5147-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="c5147-153">Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5147-153">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="c5147-154">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5147-154">PARAMETERS</span></span>

### <span data-ttu-id="c5147-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="c5147-155">-CaaFlags</span></span>
<span data-ttu-id="c5147-156">Флаги для записи CAA, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="c5147-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="c5147-157">Должно быть числом от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="c5147-157">Must be a number between 0 and 255.</span></span>

```yaml
Type: Byte
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5147-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="c5147-158">-CaaTag</span></span>
<span data-ttu-id="c5147-159">Поле тега записи CAA, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="c5147-159">The tag field of the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5147-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="c5147-160">-CaaValue</span></span>
<span data-ttu-id="c5147-161">Поле значения для записи CAA, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="c5147-161">The value field for the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5147-162">-CNAME</span><span class="sxs-lookup"><span data-stu-id="c5147-162">-Cname</span></span>
<span data-ttu-id="c5147-163">Задает доменное имя для записи канонического имени (CNAME).</span><span class="sxs-lookup"><span data-stu-id="c5147-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="c5147-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5147-164">-DefaultProfile</span></span>
<span data-ttu-id="c5147-165">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c5147-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5147-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="c5147-166">-Exchange</span></span>
<span data-ttu-id="c5147-167">Указывает имя почтового сервера для записи почтового обменника (MX).</span><span class="sxs-lookup"><span data-stu-id="c5147-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="c5147-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="c5147-168">-Ipv4Address</span></span>
<span data-ttu-id="c5147-169">Задает IPv4-адрес для записи A.</span><span class="sxs-lookup"><span data-stu-id="c5147-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="c5147-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="c5147-170">-Ipv6Address</span></span>
<span data-ttu-id="c5147-171">Задает IPv6-адрес для записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="c5147-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="c5147-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="c5147-172">-Nsdname</span></span>
<span data-ttu-id="c5147-173">Указывает сервер доменных имен для записи сервера доменных имен (NS).</span><span class="sxs-lookup"><span data-stu-id="c5147-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="c5147-174">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="c5147-174">-Port</span></span>
<span data-ttu-id="c5147-175">Указывает порт для записи службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="c5147-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="c5147-176">-Предпочтения</span><span class="sxs-lookup"><span data-stu-id="c5147-176">-Preference</span></span>
<span data-ttu-id="c5147-177">Задает приоритет MX-записи.</span><span class="sxs-lookup"><span data-stu-id="c5147-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="c5147-178">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="c5147-178">-Priority</span></span>
<span data-ttu-id="c5147-179">Указывает приоритет записи SRV.</span><span class="sxs-lookup"><span data-stu-id="c5147-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="c5147-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="c5147-180">-Ptrdname</span></span>
<span data-ttu-id="c5147-181">Указывает целевое доменное имя записи указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="c5147-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="c5147-182">-Набор записей</span><span class="sxs-lookup"><span data-stu-id="c5147-182">-RecordSet</span></span>
<span data-ttu-id="c5147-183">Указывает объект **набора записей** , содержащий удаляемую запись.</span><span class="sxs-lookup"><span data-stu-id="c5147-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="c5147-184">-Target</span><span class="sxs-lookup"><span data-stu-id="c5147-184">-Target</span></span>
<span data-ttu-id="c5147-185">Указывает целевой объект для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="c5147-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="c5147-186">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="c5147-186">-Value</span></span>
<span data-ttu-id="c5147-187">Задает значение для записи TXT.</span><span class="sxs-lookup"><span data-stu-id="c5147-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="c5147-188">-Weight</span><span class="sxs-lookup"><span data-stu-id="c5147-188">-Weight</span></span>
<span data-ttu-id="c5147-189">Определяет вес записи SRV.</span><span class="sxs-lookup"><span data-stu-id="c5147-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="c5147-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5147-190">CommonParameters</span></span>
<span data-ttu-id="c5147-191">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5147-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5147-192">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5147-192">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5147-193">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5147-193">INPUTS</span></span>

### <span data-ttu-id="c5147-194">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c5147-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="c5147-195">Вы можете передать на этот командлет объект **DnsRecordSet** .</span><span class="sxs-lookup"><span data-stu-id="c5147-195">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="c5147-196">Это автономное представление набора записей и его обновления не изменяют ответы DNS, пока не будет запущен параметр SET-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="c5147-196">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="c5147-197">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5147-197">OUTPUTS</span></span>

### <span data-ttu-id="c5147-198">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c5147-198">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="c5147-199">Этот командлет возвращает измененный объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="c5147-199">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="c5147-200">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5147-200">NOTES</span></span>

## <span data-ttu-id="c5147-201">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5147-201">RELATED LINKS</span></span>

[<span data-ttu-id="c5147-202">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c5147-202">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="c5147-203">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c5147-203">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="c5147-204">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c5147-204">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
