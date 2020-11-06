---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
ms.openlocfilehash: 7f271ee6a946356fe9cbf09379e2e620a240b733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565453"
---
# <span data-ttu-id="f1a2d-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1a2d-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="f1a2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a2d-103">Создание набор записей DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1a2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1a2d-104">SYNTAX</span></span>

### <span data-ttu-id="f1a2d-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f1a2d-105">Fields (Default)</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a2d-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="f1a2d-106">AliasFields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a2d-107">DataObject</span><span class="sxs-lookup"><span data-stu-id="f1a2d-107">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a2d-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="f1a2d-108">AliasObject</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a2d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1a2d-109">DESCRIPTION</span></span>
<span data-ttu-id="f1a2d-110">Командлет **New-AzureRmDnsRecordSet** создает новый набор записей DNS (Domain Name System) с указанными именем и типом в указанной зоне.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-110">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="f1a2d-111">Объект **Recordset** — это набор записей DNS с одинаковыми именами и типами.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="f1a2d-112">Обратите внимание, что имя задается относительно зоны, а не полного имени.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="f1a2d-113">Параметр *DnsRecords* указывает записи в заданном множестве записей.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="f1a2d-114">Этот параметр берет на себя массив DNS-записей, созданный с помощью New-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-114">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>
<span data-ttu-id="f1a2d-115">Вы можете использовать оператор Pipeline для передачи объекта **dnsZone** в этот командлет или передать объект **dnsZone** в качестве параметра *зоны* или же можно указать зону по имени.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="f1a2d-116">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f1a2d-117">Если соответствующий **набор записей** уже существует (то же имя и тип записи), необходимо указать параметр *перезаписи* , в противном случае командлет не создаст новый **набор записей** .</span><span class="sxs-lookup"><span data-stu-id="f1a2d-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="f1a2d-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1a2d-118">EXAMPLES</span></span>

### <span data-ttu-id="f1a2d-119">Пример 1: создание набора записей типа A</span><span class="sxs-lookup"><span data-stu-id="f1a2d-119">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="f1a2d-120">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f1a2d-121">Набор записей имеет тип A и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="f1a2d-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1a2d-122">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="f1a2d-123">Пример 2: создание набора записей типа AAAA</span><span class="sxs-lookup"><span data-stu-id="f1a2d-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1a2d-124">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f1a2d-125">Набор записей имеет тип AAAA и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="f1a2d-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1a2d-126">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-126">It contains a single DNS record.</span></span>
<span data-ttu-id="f1a2d-127">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1a2d-128">Пример 3: создание набора записей с типом CNAME</span><span class="sxs-lookup"><span data-stu-id="f1a2d-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1a2d-129">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f1a2d-130">Набор записей имеет тип CNAME и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="f1a2d-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1a2d-131">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-131">It contains a single DNS record.</span></span>
<span data-ttu-id="f1a2d-132">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1a2d-133">Пример 4: создание набора записей типа MX</span><span class="sxs-lookup"><span data-stu-id="f1a2d-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1a2d-134">Эта команда создает **набор записей** с именем www в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f1a2d-135">Набор записей имеет тип MX и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="f1a2d-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1a2d-136">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-136">It contains a single DNS record.</span></span>
<span data-ttu-id="f1a2d-137">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1a2d-138">Пример 5: создание набора записей с типом "NS"</span><span class="sxs-lookup"><span data-stu-id="f1a2d-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1a2d-139">Эта команда создает **набор записей** с именем ns1 в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="f1a2d-140">Набор записей имеет тип NS и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="f1a2d-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1a2d-141">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-141">It contains a single DNS record.</span></span>
<span data-ttu-id="f1a2d-142">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1a2d-143">Пример 6: создание набора записей типа PTR</span><span class="sxs-lookup"><span data-stu-id="f1a2d-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="f1a2d-144">Эта команда создает **набор записей** с именем 4 в зоне 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="f1a2d-145">Набор записей имеет тип PTR и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="f1a2d-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1a2d-146">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-146">It contains a single DNS record.</span></span>
<span data-ttu-id="f1a2d-147">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1a2d-148">Пример 7: создание набора записей типа SRV</span><span class="sxs-lookup"><span data-stu-id="f1a2d-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1a2d-149">Эта команда создает **набор записей** с именем _sip. _tcp в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="f1a2d-150">Набор записей имеет тип SRV и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="f1a2d-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1a2d-151">Она состоит из одной записи DNS, указывающей на IP-адрес 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="f1a2d-152">Служба SIP и протокол TCP задаются как часть имени набора записей, а не как часть данных записи.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="f1a2d-153">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1a2d-154">Пример 8: создание набора записей типа TXT</span><span class="sxs-lookup"><span data-stu-id="f1a2d-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1a2d-155">Эта команда создает **набор записей** с именем, указанным в MyZone.com Zone.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="f1a2d-156">Набор записей имеет тип TXT и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="f1a2d-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1a2d-157">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-157">It contains a single DNS record.</span></span>
<span data-ttu-id="f1a2d-158">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1a2d-159">Пример 9: создание набора записей на уровне зоны Апекс</span><span class="sxs-lookup"><span data-stu-id="f1a2d-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1a2d-160">Эта команда создает **набор записей** на Апекс (или корне) зоны MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="f1a2d-161">Для этого в качестве имени для записи задано значение @ (в том числе двойные кавычки).</span><span class="sxs-lookup"><span data-stu-id="f1a2d-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="f1a2d-162">Вы не можете создавать записи CNAME на Апекс зоны.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="f1a2d-163">Это ограничение, заданное в DNS-стандартах. Это не ограничение Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="f1a2d-164">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1a2d-165">Пример 10: создание набора записей с подстановочными знаками</span><span class="sxs-lookup"><span data-stu-id="f1a2d-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f1a2d-166">Эта команда создает **набор записей** с именем \* в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="f1a2d-167">Это набор подстановочных записей.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-167">This is a wildcard record set.</span></span>
<span data-ttu-id="f1a2d-168">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f1a2d-169">Пример 11: создание пустого множества записей</span><span class="sxs-lookup"><span data-stu-id="f1a2d-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="f1a2d-170">Эта команда создает **набор записей** с именем www в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f1a2d-171">Набор записей имеет тип A и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="f1a2d-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f1a2d-172">Это пустой набор записей, который выступает в качестве заполнителя, в который позже можно добавлять записи.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="f1a2d-173">Пример 12: создание набор записей и отключение всех подтверждений</span><span class="sxs-lookup"><span data-stu-id="f1a2d-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="f1a2d-174">Эта команда создает **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="f1a2d-175">Параметр *перезаписи* гарантирует, что этот элемент будет перезаписывать все существующие наборы записей с таким же именем и типом (существующие записи из этого множества будут утрачены).</span><span class="sxs-lookup"><span data-stu-id="f1a2d-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="f1a2d-176">Параметр *Confirm* со значением $false подавляет вывод запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="f1a2d-177">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1a2d-177">PARAMETERS</span></span>

### <span data-ttu-id="f1a2d-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a2d-178">-DefaultProfile</span></span>
<span data-ttu-id="f1a2d-179">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f1a2d-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1a2d-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="f1a2d-180">-DnsRecords</span></span>
<span data-ttu-id="f1a2d-181">Указывает массив записей DNS, которые нужно включить в набор записей.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="f1a2d-182">Вы можете использовать командлет New-AzureRmDnsRecordConfig для создания объектов записи DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-182">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="f1a2d-183">Для получения дополнительных сведений ознакомьтесь с приведенными ниже примерами.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-183">See the examples for more information.</span></span>

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

### <span data-ttu-id="f1a2d-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f1a2d-184">-Metadata</span></span>
<span data-ttu-id="f1a2d-185">Задает массив метаданных, которые нужно связать с набором записей.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="f1a2d-186">Метаданные задаются с помощью пар "имя-значение", которые представлены в виде хэш-таблиц, например @ (@ {"Name" = "Отдел"; "Value" = "покупки"}, @ {"Name" = "пер"; "Значение" = "производство"}).</span><span class="sxs-lookup"><span data-stu-id="f1a2d-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

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

### <span data-ttu-id="f1a2d-187">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1a2d-187">-Name</span></span>
<span data-ttu-id="f1a2d-188">Указывает имя создаваемого **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="f1a2d-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="f1a2d-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f1a2d-189">-Overwrite</span></span>
<span data-ttu-id="f1a2d-190">Указывает на то, что этот командлет перезаписывает указанный **набор записей** , если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="f1a2d-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="f1a2d-191">-RecordType</span></span>
<span data-ttu-id="f1a2d-192">Указывает тип создаваемой записи DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="f1a2d-193">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f1a2d-193">Valid values are:</span></span>
- <span data-ttu-id="f1a2d-194">Помощью</span><span class="sxs-lookup"><span data-stu-id="f1a2d-194">A</span></span>
- <span data-ttu-id="f1a2d-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="f1a2d-195">AAAA</span></span>
- <span data-ttu-id="f1a2d-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="f1a2d-196">CNAME</span></span>
- <span data-ttu-id="f1a2d-197">МХ</span><span class="sxs-lookup"><span data-stu-id="f1a2d-197">MX</span></span>
- <span data-ttu-id="f1a2d-198">СЛУЖБУ</span><span class="sxs-lookup"><span data-stu-id="f1a2d-198">NS</span></span>
- <span data-ttu-id="f1a2d-199">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="f1a2d-199">PTR</span></span>
- <span data-ttu-id="f1a2d-200">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="f1a2d-200">SRV</span></span>
- <span data-ttu-id="f1a2d-201">Записи SOA будут создаваться автоматически при создании зоны и не могут быть созданы вручную.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="f1a2d-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a2d-202">-ResourceGroupName</span></span>
<span data-ttu-id="f1a2d-203">Указывает группу ресурсов, которая содержит зону DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="f1a2d-204">Кроме того, необходимо указать параметр *zonename* , чтобы указать имя зоны.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="f1a2d-205">Кроме того, вы можете указать зону и группу ресурсов, передав объект зоны DNS с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="f1a2d-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="f1a2d-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a2d-206">-TargetResourceId</span></span>
<span data-ttu-id="f1a2d-207">Идентификатор целевого ресурса псевдонима.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-207">Alias Target Resource Id.</span></span>

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

### <span data-ttu-id="f1a2d-208">-TTL</span><span class="sxs-lookup"><span data-stu-id="f1a2d-208">-Ttl</span></span>
<span data-ttu-id="f1a2d-209">Указывает срок жизни (TTL) для набора записей DNS.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="f1a2d-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="f1a2d-210">-Zone</span></span>
<span data-ttu-id="f1a2d-211">Указывает DnsZone, в котором нужно создать **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="f1a2d-212">Кроме того, вы можете указать зону с помощью параметров *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f1a2d-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="f1a2d-213">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="f1a2d-213">-ZoneName</span></span>
<span data-ttu-id="f1a2d-214">Указывает имя зоны, в которой нужно создать **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="f1a2d-215">Кроме того, необходимо указать группу ресурсов, содержащую зону, с помощью параметра *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f1a2d-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="f1a2d-216">Кроме того, вы можете указать зону и группу ресурсов, передав объект зоны DNS с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="f1a2d-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="f1a2d-217">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1a2d-217">-Confirm</span></span>
<span data-ttu-id="f1a2d-218">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a2d-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a2d-219">-WhatIf</span></span>
<span data-ttu-id="f1a2d-220">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a2d-221">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a2d-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a2d-222">CommonParameters</span></span>
<span data-ttu-id="f1a2d-223">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a2d-224">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1a2d-224">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a2d-225">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1a2d-225">INPUTS</span></span>

### <span data-ttu-id="f1a2d-226">System. String</span><span class="sxs-lookup"><span data-stu-id="f1a2d-226">System.String</span></span>

### <span data-ttu-id="f1a2d-227">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="f1a2d-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="f1a2d-228">Параметры: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f1a2d-228">Parameters: Zone (ByValue)</span></span>

### <span data-ttu-id="f1a2d-229">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="f1a2d-229">System.UInt32</span></span>

### <span data-ttu-id="f1a2d-230">Microsoft. Azure. Management. DNS. Models. RecordType</span><span class="sxs-lookup"><span data-stu-id="f1a2d-230">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="f1a2d-231">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1a2d-231">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f1a2d-232">Microsoft. Azure. Commands. DNS. DnsRecordBase []</span><span class="sxs-lookup"><span data-stu-id="f1a2d-232">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>
<span data-ttu-id="f1a2d-233">Параметры: DnsRecords (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f1a2d-233">Parameters: DnsRecords (ByValue)</span></span>

## <span data-ttu-id="f1a2d-234">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1a2d-234">OUTPUTS</span></span>

### <span data-ttu-id="f1a2d-235">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1a2d-235">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="f1a2d-236">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1a2d-236">NOTES</span></span>
<span data-ttu-id="f1a2d-237">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-237">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f1a2d-238">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-238">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="f1a2d-239">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-239">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="f1a2d-240">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f1a2d-240">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f1a2d-241">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1a2d-241">RELATED LINKS</span></span>

[<span data-ttu-id="f1a2d-242">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f1a2d-242">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="f1a2d-243">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1a2d-243">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="f1a2d-244">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f1a2d-244">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="f1a2d-245">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1a2d-245">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="f1a2d-246">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1a2d-246">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
