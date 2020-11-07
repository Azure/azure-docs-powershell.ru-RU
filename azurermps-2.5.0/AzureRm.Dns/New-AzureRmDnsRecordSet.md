---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce82a1bae63fafcf0d221d0c2ce6d8e82e8e8e12
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913653"
---
# <span data-ttu-id="ec702-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ec702-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="ec702-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec702-102">SYNOPSIS</span></span>
<span data-ttu-id="ec702-103">Создание набор записей DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec702-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec702-104">SYNTAX</span></span>

### <span data-ttu-id="ec702-105">»</span><span class="sxs-lookup"><span data-stu-id="ec702-105">Fields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec702-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="ec702-106">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec702-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec702-107">DESCRIPTION</span></span>
<span data-ttu-id="ec702-108">Командлет **New-AzureRmDnsRecordSet** создает новый набор записей DNS (Domain Name System) с указанными именем и типом в указанной зоне.</span><span class="sxs-lookup"><span data-stu-id="ec702-108">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="ec702-109">Объект **Recordset** — это набор записей DNS с одинаковыми именами и типами.</span><span class="sxs-lookup"><span data-stu-id="ec702-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="ec702-110">Обратите внимание, что имя задается относительно зоны, а не полного имени.</span><span class="sxs-lookup"><span data-stu-id="ec702-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="ec702-111">Параметр *DnsRecords* указывает записи в заданном множестве записей.</span><span class="sxs-lookup"><span data-stu-id="ec702-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="ec702-112">Этот параметр берет на себя массив DNS-записей, созданный с помощью New-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="ec702-112">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>

<span data-ttu-id="ec702-113">Вы можете использовать оператор Pipeline для передачи объекта **dnsZone** в этот командлет или передать объект **dnsZone** в качестве параметра *зоны* или же можно указать зону по имени.</span><span class="sxs-lookup"><span data-stu-id="ec702-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="ec702-114">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ec702-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="ec702-115">Если соответствующий **набор записей** уже существует (то же имя и тип записи), необходимо указать параметр *перезаписи* , в противном случае командлет не создаст новый **набор записей** .</span><span class="sxs-lookup"><span data-stu-id="ec702-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="ec702-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec702-116">EXAMPLES</span></span>

### <span data-ttu-id="ec702-117">Пример 1: создание набора записей типа A</span><span class="sxs-lookup"><span data-stu-id="ec702-117">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ec702-118">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="ec702-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ec702-119">Набор записей имеет тип A и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="ec702-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ec702-120">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="ec702-121">Пример 2: создание набора записей типа AAAA</span><span class="sxs-lookup"><span data-stu-id="ec702-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ec702-122">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="ec702-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ec702-123">Набор записей имеет тип AAAA и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="ec702-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ec702-124">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-124">It contains a single DNS record.</span></span>

<span data-ttu-id="ec702-125">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="ec702-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ec702-126">Пример 3: создание набора записей с типом CNAME</span><span class="sxs-lookup"><span data-stu-id="ec702-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ec702-127">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="ec702-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ec702-128">Набор записей имеет тип CNAME и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="ec702-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ec702-129">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-129">It contains a single DNS record.</span></span>

<span data-ttu-id="ec702-130">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="ec702-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ec702-131">Пример 4: создание набора записей типа MX</span><span class="sxs-lookup"><span data-stu-id="ec702-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ec702-132">Эта команда создает **набор записей** с именем www в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="ec702-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ec702-133">Набор записей имеет тип MX и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="ec702-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ec702-134">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-134">It contains a single DNS record.</span></span>

<span data-ttu-id="ec702-135">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="ec702-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ec702-136">Пример 5: создание набора записей с типом "NS"</span><span class="sxs-lookup"><span data-stu-id="ec702-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ec702-137">Эта команда создает **набор записей** с именем ns1 в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="ec702-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="ec702-138">Набор записей имеет тип NS и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="ec702-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ec702-139">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-139">It contains a single DNS record.</span></span>

<span data-ttu-id="ec702-140">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="ec702-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ec702-141">Пример 6: создание набора записей типа PTR</span><span class="sxs-lookup"><span data-stu-id="ec702-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="ec702-142">Эта команда создает **набор записей** с именем 4 в зоне 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="ec702-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="ec702-143">Набор записей имеет тип PTR и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="ec702-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ec702-144">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-144">It contains a single DNS record.</span></span>

<span data-ttu-id="ec702-145">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="ec702-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ec702-146">Пример 7: создание набора записей типа SRV</span><span class="sxs-lookup"><span data-stu-id="ec702-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ec702-147">Эта команда создает **набор записей** с именем _sip. _tcp в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="ec702-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="ec702-148">Набор записей имеет тип SRV и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="ec702-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ec702-149">Она состоит из одной записи DNS, указывающей на IP-адрес 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="ec702-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="ec702-150">Служба SIP и протокол TCP задаются как часть имени набора записей, а не как часть данных записи.</span><span class="sxs-lookup"><span data-stu-id="ec702-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="ec702-151">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="ec702-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ec702-152">Пример 8: создание набора записей типа TXT</span><span class="sxs-lookup"><span data-stu-id="ec702-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ec702-153">Эта команда создает **набор записей** с именем, указанным в MyZone.com Zone.</span><span class="sxs-lookup"><span data-stu-id="ec702-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="ec702-154">Набор записей имеет тип TXT и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="ec702-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ec702-155">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-155">It contains a single DNS record.</span></span>

<span data-ttu-id="ec702-156">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="ec702-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ec702-157">Пример 9: создание набора записей на уровне зоны Апекс</span><span class="sxs-lookup"><span data-stu-id="ec702-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ec702-158">Эта команда создает **набор записей** на Апекс (или корне) зоны MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="ec702-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="ec702-159">Для этого в качестве имени для записи задано значение @ (в том числе двойные кавычки).</span><span class="sxs-lookup"><span data-stu-id="ec702-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="ec702-160">Вы не можете создавать записи CNAME на Апекс зоны.</span><span class="sxs-lookup"><span data-stu-id="ec702-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="ec702-161">Это ограничение, заданное в DNS-стандартах. Это не ограничение Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="ec702-162">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="ec702-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ec702-163">Пример 10: создание набора записей с подстановочными знаками</span><span class="sxs-lookup"><span data-stu-id="ec702-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ec702-164">Эта команда создает **набор записей** с именем \* в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="ec702-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="ec702-165">Это набор подстановочных записей.</span><span class="sxs-lookup"><span data-stu-id="ec702-165">This is a wildcard record set.</span></span>

<span data-ttu-id="ec702-166">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="ec702-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ec702-167">Пример 11: создание пустого множества записей</span><span class="sxs-lookup"><span data-stu-id="ec702-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="ec702-168">Эта команда создает **набор записей** с именем www в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="ec702-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ec702-169">Набор записей имеет тип A и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="ec702-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ec702-170">Это пустой набор записей, который выступает в качестве заполнителя, в который позже можно добавлять записи.</span><span class="sxs-lookup"><span data-stu-id="ec702-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="ec702-171">Пример 12: создание набор записей и отключение всех подтверждений</span><span class="sxs-lookup"><span data-stu-id="ec702-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="ec702-172">Эта команда создает **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="ec702-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="ec702-173">Параметр *перезаписи* гарантирует, что этот элемент будет перезаписывать все существующие наборы записей с таким же именем и типом (существующие записи из этого множества будут утрачены).</span><span class="sxs-lookup"><span data-stu-id="ec702-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="ec702-174">Параметр *Confirm* со значением $false подавляет вывод запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ec702-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="ec702-175">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec702-175">PARAMETERS</span></span>

### <span data-ttu-id="ec702-176">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="ec702-176">-DnsRecords</span></span>
<span data-ttu-id="ec702-177">Указывает массив записей DNS, которые нужно включить в набор записей.</span><span class="sxs-lookup"><span data-stu-id="ec702-177">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="ec702-178">Вы можете использовать командлет New-AzureRmDnsRecordConfig для создания объектов записи DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-178">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="ec702-179">Для получения дополнительных сведений ознакомьтесь с приведенными ниже примерами.</span><span class="sxs-lookup"><span data-stu-id="ec702-179">See the examples for more information.</span></span>

```yaml
Type: DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec702-180">-Force</span><span class="sxs-lookup"><span data-stu-id="ec702-180">-Force</span></span>
<span data-ttu-id="ec702-181">Этот параметр устарел для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="ec702-181">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="ec702-182">Оно будет удалено в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="ec702-182">It will be removed in a future release.</span></span>

<span data-ttu-id="ec702-183">Чтобы указать, будет ли этот командлет запрашивать comfirmation, используйте параметр *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="ec702-183">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="ec702-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ec702-184">-Metadata</span></span>
<span data-ttu-id="ec702-185">Задает массив метаданных, которые нужно связать с набором записей.</span><span class="sxs-lookup"><span data-stu-id="ec702-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="ec702-186">Метаданные задаются с помощью пар "имя-значение", которые представлены в виде хэш-таблиц, например @ (@ {"Name" = "Отдел"; "Value" = "покупки"}, @ {"Name" = "пер"; "Значение" = "производство"}).</span><span class="sxs-lookup"><span data-stu-id="ec702-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

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

### <span data-ttu-id="ec702-187">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ec702-187">-Name</span></span>
<span data-ttu-id="ec702-188">Указывает имя создаваемого **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ec702-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="ec702-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ec702-189">-Overwrite</span></span>
<span data-ttu-id="ec702-190">Указывает на то, что этот командлет перезаписывает указанный **набор записей** , если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="ec702-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="ec702-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="ec702-191">-RecordType</span></span>
<span data-ttu-id="ec702-192">Указывает тип создаваемой записи DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-192">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="ec702-193">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="ec702-193">Valid values are:</span></span>

- <span data-ttu-id="ec702-194">Помощью</span><span class="sxs-lookup"><span data-stu-id="ec702-194">A</span></span>
- <span data-ttu-id="ec702-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="ec702-195">AAAA</span></span>
- <span data-ttu-id="ec702-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="ec702-196">CNAME</span></span>
- <span data-ttu-id="ec702-197">МХ</span><span class="sxs-lookup"><span data-stu-id="ec702-197">MX</span></span>
- <span data-ttu-id="ec702-198">СЛУЖБУ</span><span class="sxs-lookup"><span data-stu-id="ec702-198">NS</span></span>
- <span data-ttu-id="ec702-199">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="ec702-199">PTR</span></span>
- <span data-ttu-id="ec702-200">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="ec702-200">SRV</span></span>
- <span data-ttu-id="ec702-201">ТХТ</span><span class="sxs-lookup"><span data-stu-id="ec702-201">TXT</span></span>

<span data-ttu-id="ec702-202">Записи SOA создаются автоматически при создании зоны и не могут быть созданы вручную.</span><span class="sxs-lookup"><span data-stu-id="ec702-202">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec702-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec702-203">-ResourceGroupName</span></span>
<span data-ttu-id="ec702-204">Указывает группу ресурсов, которая содержит зону DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-204">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="ec702-205">Кроме того, необходимо указать параметр *zonename* , чтобы указать имя зоны.</span><span class="sxs-lookup"><span data-stu-id="ec702-205">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="ec702-206">Кроме того, вы можете указать зону и группу ресурсов, передав объект зоны DNS с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="ec702-206">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec702-207">-TTL</span><span class="sxs-lookup"><span data-stu-id="ec702-207">-Ttl</span></span>
<span data-ttu-id="ec702-208">Указывает срок жизни (TTL) для набора записей DNS.</span><span class="sxs-lookup"><span data-stu-id="ec702-208">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec702-209">-Zone</span><span class="sxs-lookup"><span data-stu-id="ec702-209">-Zone</span></span>
<span data-ttu-id="ec702-210">Указывает DnsZone, в котором нужно создать **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="ec702-210">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="ec702-211">Кроме того, вы можете указать зону с помощью параметров *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ec702-211">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec702-212">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="ec702-212">-ZoneName</span></span>
<span data-ttu-id="ec702-213">Указывает имя зоны, в которой нужно создать **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="ec702-213">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="ec702-214">Кроме того, необходимо указать группу ресурсов, содержащую зону, с помощью параметра *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ec702-214">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="ec702-215">Кроме того, вы можете указать зону и группу ресурсов, передав объект зоны DNS с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="ec702-215">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec702-216">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec702-216">-Confirm</span></span>
<span data-ttu-id="ec702-217">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ec702-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec702-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec702-218">-WhatIf</span></span>
<span data-ttu-id="ec702-219">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ec702-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec702-220">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ec702-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec702-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec702-221">CommonParameters</span></span>
<span data-ttu-id="ec702-222">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec702-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec702-223">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec702-223">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec702-224">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec702-224">INPUTS</span></span>

### <span data-ttu-id="ec702-225">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="ec702-225">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="ec702-226">Вы можете передать на этот командлет объект DnsZone.</span><span class="sxs-lookup"><span data-stu-id="ec702-226">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="ec702-227">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec702-227">OUTPUTS</span></span>

### <span data-ttu-id="ec702-228">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ec702-228">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="ec702-229">Этот командлет возвращает объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ec702-229">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="ec702-230">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec702-230">NOTES</span></span>
<span data-ttu-id="ec702-231">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ec702-231">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ec702-232">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="ec702-232">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="ec702-233">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="ec702-233">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="ec702-234">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ec702-234">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ec702-235">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec702-235">RELATED LINKS</span></span>

[<span data-ttu-id="ec702-236">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ec702-236">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="ec702-237">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ec702-237">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ec702-238">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ec702-238">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="ec702-239">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ec702-239">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ec702-240">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ec702-240">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
