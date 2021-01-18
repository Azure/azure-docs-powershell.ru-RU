---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506294"
---
# <span data-ttu-id="644ac-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="644ac-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="644ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="644ac-102">SYNOPSIS</span></span>
<span data-ttu-id="644ac-103">Создает набор записей DNS.</span><span class="sxs-lookup"><span data-stu-id="644ac-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="644ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="644ac-104">SYNTAX</span></span>

### <span data-ttu-id="644ac-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="644ac-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="644ac-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="644ac-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="644ac-107">Объект</span><span class="sxs-lookup"><span data-stu-id="644ac-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="644ac-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="644ac-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="644ac-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="644ac-109">DESCRIPTION</span></span>
<span data-ttu-id="644ac-110">С **помощью cmdlet New-AzDnsRecordSet** создается новый набор записей службы доменных имен (DNS) с указанным именем и типом в указанной зоне.</span><span class="sxs-lookup"><span data-stu-id="644ac-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="644ac-111">Объект **RecordSet** — это набор записей DNS с одинаковым именем и типом.</span><span class="sxs-lookup"><span data-stu-id="644ac-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="644ac-112">Обратите внимание, что имя является относительно зоны, а не полного имени.</span><span class="sxs-lookup"><span data-stu-id="644ac-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="644ac-113">Параметр *DnsRecords* определяет записи в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="644ac-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="644ac-114">Этот параметр использует массив записей DNS, построенный с использованием new-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="644ac-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="644ac-115">Вы можете использовать оператор конвейера, чтобы передать объект **DnsZone** этому cmdlet, или передать объект **DnsZone** в качестве параметра *зоны.* Кроме того, вы можете указать зону по имени.</span><span class="sxs-lookup"><span data-stu-id="644ac-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="644ac-116">Параметр Confirm  и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="644ac-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="644ac-117">Если совпадающий **набор записей** уже существует (то же имя и тип записи), необходимо указать параметр *Overwrite,* иначе командлет не создаст новый **Набор записей.**</span><span class="sxs-lookup"><span data-stu-id="644ac-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="644ac-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="644ac-118">EXAMPLES</span></span>

### <span data-ttu-id="644ac-119">Пример 1. Создание наборов записей типа A</span><span class="sxs-lookup"><span data-stu-id="644ac-119">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="644ac-120">В этом примере создается **набор записей с** именем www в зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="644ac-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="644ac-121">Набор записей имеет тип A и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="644ac-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="644ac-122">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="644ac-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="644ac-123">Пример 2. Создание наборов записей типа AAAA</span><span class="sxs-lookup"><span data-stu-id="644ac-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="644ac-124">В этом примере создается **набор записей с** именем www в зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="644ac-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="644ac-125">Набор записей имеет тип AAAA и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="644ac-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="644ac-126">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="644ac-126">It contains a single DNS record.</span></span>
<span data-ttu-id="644ac-127">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="644ac-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="644ac-128">Пример 3. Создание наборов записей типа CNAME</span><span class="sxs-lookup"><span data-stu-id="644ac-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="644ac-129">В этом примере создается **набор записей с** именем www в зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="644ac-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="644ac-130">Набор записей имеет тип CNAME и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="644ac-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="644ac-131">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="644ac-131">It contains a single DNS record.</span></span>
<span data-ttu-id="644ac-132">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="644ac-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="644ac-133">Пример 4. Создание наборов записей типа MX</span><span class="sxs-lookup"><span data-stu-id="644ac-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="644ac-134">Эта команда создает набор **записей с именем** www в зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="644ac-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="644ac-135">Набор записей имеет тип MX и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="644ac-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="644ac-136">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="644ac-136">It contains a single DNS record.</span></span>
<span data-ttu-id="644ac-137">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="644ac-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="644ac-138">Пример 5. Создание наборов записей типа NS</span><span class="sxs-lookup"><span data-stu-id="644ac-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="644ac-139">Эта команда создает набор **записей с** именем ns1 в зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="644ac-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="644ac-140">Набор записей имеет тип NS и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="644ac-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="644ac-141">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="644ac-141">It contains a single DNS record.</span></span>
<span data-ttu-id="644ac-142">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="644ac-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="644ac-143">Пример 6. Создание наборов записей типа PTR</span><span class="sxs-lookup"><span data-stu-id="644ac-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="644ac-144">Эта команда создает набор **записей с** именем 4 в зоне 3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="644ac-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="644ac-145">Набор записей имеет тип PTR и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="644ac-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="644ac-146">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="644ac-146">It contains a single DNS record.</span></span>
<span data-ttu-id="644ac-147">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="644ac-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="644ac-148">Пример 7. Создание recordSet типа SRV</span><span class="sxs-lookup"><span data-stu-id="644ac-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="644ac-149">Эта команда создает набор **записей с** именем _sip._tcp в myzone.com.</span><span class="sxs-lookup"><span data-stu-id="644ac-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="644ac-150">Набор записей имеет тип SRV и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="644ac-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="644ac-151">Она содержит одну запись DNS, указывав на IP-адрес 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="644ac-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="644ac-152">Служба (sip) и протокол (tcp) указаны как часть имени набора записей, а не как часть данных записи.</span><span class="sxs-lookup"><span data-stu-id="644ac-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="644ac-153">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="644ac-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="644ac-154">Пример 8. Создание наборов записей типа TXT</span><span class="sxs-lookup"><span data-stu-id="644ac-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="644ac-155">Эта команда создает **именуемую** команду RecordSet в myzone.com.</span><span class="sxs-lookup"><span data-stu-id="644ac-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="644ac-156">Набор записей имеет тип TXT и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="644ac-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="644ac-157">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="644ac-157">It contains a single DNS record.</span></span>
<span data-ttu-id="644ac-158">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="644ac-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="644ac-159">Пример 9. Создание наборов записей в апексе зоны</span><span class="sxs-lookup"><span data-stu-id="644ac-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="644ac-160">Эта команда создает **набор записей** в апексе (корневом) точках зоны myzone.com.</span><span class="sxs-lookup"><span data-stu-id="644ac-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="644ac-161">Для этого имя набора записей задано как @(включая двойные кавычка).</span><span class="sxs-lookup"><span data-stu-id="644ac-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="644ac-162">Записи CNAME невозможно создать в апексе зоны.</span><span class="sxs-lookup"><span data-stu-id="644ac-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="644ac-163">Это ограничение стандартов DNS. это не ограничение службы Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="644ac-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="644ac-164">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="644ac-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="644ac-165">Пример 10. Создание набора записей с поддиавными знаками</span><span class="sxs-lookup"><span data-stu-id="644ac-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="644ac-166">Эта команда создает набор **записей с именем** \* в myzone.com.</span><span class="sxs-lookup"><span data-stu-id="644ac-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="644ac-167">Это набор записей с поддиавными знаками.</span><span class="sxs-lookup"><span data-stu-id="644ac-167">This is a wildcard record set.</span></span>
<span data-ttu-id="644ac-168">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="644ac-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="644ac-169">Пример 11. Создание пустого набора записей</span><span class="sxs-lookup"><span data-stu-id="644ac-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="644ac-170">Эта команда создает набор **записей с именем** www в зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="644ac-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="644ac-171">Набор записей имеет тип A и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="644ac-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="644ac-172">Это пустой набор записей, который выступать в качестве места для добавления записей.</span><span class="sxs-lookup"><span data-stu-id="644ac-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="644ac-173">Пример 12. Создание набора записей и подавления всего подтверждения</span><span class="sxs-lookup"><span data-stu-id="644ac-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="644ac-174">Эта команда создает **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="644ac-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="644ac-175">Параметр *"Перезаписать"* гарантирует, что этот набор записей перезаписает все существующие записи с одинаковыми именами и типами (существующие записи в этом наборе будут потеряны).</span><span class="sxs-lookup"><span data-stu-id="644ac-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="644ac-176">Параметр *Confirm* со значением $False подавляет запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="644ac-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="644ac-177">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="644ac-177">PARAMETERS</span></span>

### <span data-ttu-id="644ac-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="644ac-178">-DefaultProfile</span></span>
<span data-ttu-id="644ac-179">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="644ac-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="644ac-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="644ac-180">-DnsRecords</span></span>
<span data-ttu-id="644ac-181">Определяет массив DNS-записей, которые нужно включить в набор.</span><span class="sxs-lookup"><span data-stu-id="644ac-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="644ac-182">С помощью New-AzDnsRecordConfig DNS можно создавать объекты записей DNS.</span><span class="sxs-lookup"><span data-stu-id="644ac-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="644ac-183">Дополнительные сведения см. в примерах.</span><span class="sxs-lookup"><span data-stu-id="644ac-183">See the examples for more information.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="644ac-184">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="644ac-184">-Metadata</span></span>
<span data-ttu-id="644ac-185">Указывает массив метаданных, который нужно связать с RecordSet.</span><span class="sxs-lookup"><span data-stu-id="644ac-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="644ac-186">Метаданные заданы с помощью пар имен и значений, представленных в виде hash tables, например @{"dept"="shopping";" env"="production"}.</span><span class="sxs-lookup"><span data-stu-id="644ac-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

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

### <span data-ttu-id="644ac-187">-Name</span><span class="sxs-lookup"><span data-stu-id="644ac-187">-Name</span></span>
<span data-ttu-id="644ac-188">Имя создаемого **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="644ac-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="644ac-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="644ac-189">-Overwrite</span></span>
<span data-ttu-id="644ac-190">Указывает на то, что этот cmdlet переописает указанный **набор записей,** если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="644ac-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="644ac-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="644ac-191">-RecordType</span></span>
<span data-ttu-id="644ac-192">Тип записи DNS, которая будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="644ac-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="644ac-193">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="644ac-193">Valid values are:</span></span>
- <span data-ttu-id="644ac-194">A</span><span class="sxs-lookup"><span data-stu-id="644ac-194">A</span></span>
- <span data-ttu-id="644ac-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="644ac-195">AAAA</span></span>
- <span data-ttu-id="644ac-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="644ac-196">CNAME</span></span>
- <span data-ttu-id="644ac-197">MX</span><span class="sxs-lookup"><span data-stu-id="644ac-197">MX</span></span>
- <span data-ttu-id="644ac-198">NS</span><span class="sxs-lookup"><span data-stu-id="644ac-198">NS</span></span>
- <span data-ttu-id="644ac-199">PTR</span><span class="sxs-lookup"><span data-stu-id="644ac-199">PTR</span></span>
- <span data-ttu-id="644ac-200">SRV</span><span class="sxs-lookup"><span data-stu-id="644ac-200">SRV</span></span>
- <span data-ttu-id="644ac-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span><span class="sxs-lookup"><span data-stu-id="644ac-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="644ac-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="644ac-202">-ResourceGroupName</span></span>
<span data-ttu-id="644ac-203">Определяет группу ресурсов, которая содержит зону DNS.</span><span class="sxs-lookup"><span data-stu-id="644ac-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="644ac-204">Чтобы указать имя зоны, необходимо также указать параметр *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="644ac-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="644ac-205">Вы также можете указать зону и группу ресурсов, указав объект зоны DNS с помощью *параметра Zone (Зона).*</span><span class="sxs-lookup"><span data-stu-id="644ac-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="644ac-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="644ac-206">-TargetResourceId</span></span>
<span data-ttu-id="644ac-207">Alias Target Resource Id (Псевдоним целевого ресурса).</span><span class="sxs-lookup"><span data-stu-id="644ac-207">Alias Target Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="644ac-208">-Ttl</span><span class="sxs-lookup"><span data-stu-id="644ac-208">-Ttl</span></span>
<span data-ttu-id="644ac-209">Время жизни (TTL) для DNS RecordSet.</span><span class="sxs-lookup"><span data-stu-id="644ac-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="644ac-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="644ac-210">-Zone</span></span>
<span data-ttu-id="644ac-211">Определяет DnsZone, в котором нужно создать **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="644ac-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="644ac-212">Вы также можете указать зону с помощью параметров *ZoneName* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="644ac-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="644ac-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="644ac-213">-ZoneName</span></span>
<span data-ttu-id="644ac-214">Указывает имя зоны, в которой нужно создать **Набор записей.**</span><span class="sxs-lookup"><span data-stu-id="644ac-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="644ac-215">Кроме того, с помощью параметра *ResourceGroupName* необходимо указать группу ресурсов, содержащую зону.</span><span class="sxs-lookup"><span data-stu-id="644ac-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="644ac-216">Вы также можете указать зону и группу ресурсов, указав объект зоны DNS с помощью *параметра Zone (Зона).*</span><span class="sxs-lookup"><span data-stu-id="644ac-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="644ac-217">-Confirm</span><span class="sxs-lookup"><span data-stu-id="644ac-217">-Confirm</span></span>
<span data-ttu-id="644ac-218">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="644ac-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="644ac-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="644ac-219">-WhatIf</span></span>
<span data-ttu-id="644ac-220">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="644ac-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="644ac-221">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="644ac-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="644ac-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="644ac-222">CommonParameters</span></span>
<span data-ttu-id="644ac-223">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="644ac-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="644ac-224">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="644ac-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="644ac-225">INPUTS</span><span class="sxs-lookup"><span data-stu-id="644ac-225">INPUTS</span></span>

### <span data-ttu-id="644ac-226">System.String</span><span class="sxs-lookup"><span data-stu-id="644ac-226">System.String</span></span>

### <span data-ttu-id="644ac-227">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="644ac-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="644ac-228">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="644ac-228">System.UInt32</span></span>

### <span data-ttu-id="644ac-229">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="644ac-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="644ac-230">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="644ac-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="644ac-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span><span class="sxs-lookup"><span data-stu-id="644ac-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="644ac-232">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="644ac-232">OUTPUTS</span></span>

### <span data-ttu-id="644ac-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="644ac-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="644ac-234">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="644ac-234">NOTES</span></span>
<span data-ttu-id="644ac-235">С помощью параметра *Confirm* (Подтвердить) можно управлять запросом на подтверждение с помощью этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="644ac-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="644ac-236">По умолчанию с помощью cmdlet вы можете получить подтверждение, если переменная $ConfirmPreference Windows PowerShell имеет значение "Средний" или "Ниже".</span><span class="sxs-lookup"><span data-stu-id="644ac-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="644ac-237">Если указать *"Подтвердить"* или *"$True:$True",* этот cmdlet запросит подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="644ac-237">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="644ac-238">Если *указать confirm:$False,* то при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="644ac-238">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="644ac-239">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="644ac-239">RELATED LINKS</span></span>

[<span data-ttu-id="644ac-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="644ac-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="644ac-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="644ac-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="644ac-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="644ac-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="644ac-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="644ac-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="644ac-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="644ac-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
