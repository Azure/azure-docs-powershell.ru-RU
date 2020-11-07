---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6368cffa168772a384deb99f5a8388aef84f85b2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914481"
---
# <span data-ttu-id="fe4f0-101">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="fe4f0-101">New-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="fe4f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe4f0-102">SYNOPSIS</span></span>
<span data-ttu-id="fe4f0-103">Создание нового локального объекта записи DNS.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-103">Creates a new DNS record local object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe4f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe4f0-104">SYNTAX</span></span>

### <span data-ttu-id="fe4f0-105">Помощью</span><span class="sxs-lookup"><span data-stu-id="fe4f0-105">A</span></span>
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="fe4f0-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="fe4f0-106">Aaaa</span></span>
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="fe4f0-107">Службу</span><span class="sxs-lookup"><span data-stu-id="fe4f0-107">Ns</span></span>
```
New-AzureRmDnsRecordConfig -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="fe4f0-108">МХ</span><span class="sxs-lookup"><span data-stu-id="fe4f0-108">Mx</span></span>
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="fe4f0-109">Указателя</span><span class="sxs-lookup"><span data-stu-id="fe4f0-109">Ptr</span></span>
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="fe4f0-110">ТХТ</span><span class="sxs-lookup"><span data-stu-id="fe4f0-110">Txt</span></span>
```
New-AzureRmDnsRecordConfig -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="fe4f0-111">Могла</span><span class="sxs-lookup"><span data-stu-id="fe4f0-111">Srv</span></span>
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="fe4f0-112">CName</span><span class="sxs-lookup"><span data-stu-id="fe4f0-112">CName</span></span>
```
New-AzureRmDnsRecordConfig -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="fe4f0-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe4f0-113">DESCRIPTION</span></span>
<span data-ttu-id="fe4f0-114">Командлет **New-AzureRmDnsRecordConfig** создает локальный объект **DnsRecord** .</span><span class="sxs-lookup"><span data-stu-id="fe4f0-114">The **New-AzureRmDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="fe4f0-115">Массив этих объектов передается в командлет New-AzureRmDnsRecordSet с помощью параметра *DnsRecords* для указания записей для создания в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-115">An array of these objects is passed to the New-AzureRmDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="fe4f0-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe4f0-116">EXAMPLES</span></span>

### <span data-ttu-id="fe4f0-117">Пример 1: создание набора записей типа A</span><span class="sxs-lookup"><span data-stu-id="fe4f0-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="fe4f0-118">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="fe4f0-119">Набор записей имеет тип A и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="fe4f0-120">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="fe4f0-121">Пример 2: создание набора записей типа AAAA</span><span class="sxs-lookup"><span data-stu-id="fe4f0-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="fe4f0-122">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="fe4f0-123">Набор записей имеет тип AAAA и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="fe4f0-124">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-124">It contains a single DNS record.</span></span>

<span data-ttu-id="fe4f0-125">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="fe4f0-126">Пример 3: создание набора записей с типом CNAME</span><span class="sxs-lookup"><span data-stu-id="fe4f0-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="fe4f0-127">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="fe4f0-128">Набор записей имеет тип CNAME и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="fe4f0-129">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-129">It contains a single DNS record.</span></span>

<span data-ttu-id="fe4f0-130">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="fe4f0-131">Пример 4: создание набора записей типа MX</span><span class="sxs-lookup"><span data-stu-id="fe4f0-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="fe4f0-132">Эта команда создает **набор записей** с именем www в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="fe4f0-133">Набор записей имеет тип MX и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="fe4f0-134">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-134">It contains a single DNS record.</span></span>

<span data-ttu-id="fe4f0-135">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="fe4f0-136">Пример 5: создание набора записей с типом "NS"</span><span class="sxs-lookup"><span data-stu-id="fe4f0-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="fe4f0-137">Эта команда создает **набор записей** с именем ns1 в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="fe4f0-138">Набор записей имеет тип NS и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="fe4f0-139">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-139">It contains a single DNS record.</span></span>

<span data-ttu-id="fe4f0-140">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="fe4f0-141">Пример 6: создание набора записей типа PTR</span><span class="sxs-lookup"><span data-stu-id="fe4f0-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="fe4f0-142">Эта команда создает **набор записей** с именем 4 в зоне 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="fe4f0-143">Набор записей имеет тип PTR и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="fe4f0-144">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-144">It contains a single DNS record.</span></span>

<span data-ttu-id="fe4f0-145">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="fe4f0-146">Пример 7: создание набора записей типа SRV</span><span class="sxs-lookup"><span data-stu-id="fe4f0-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="fe4f0-147">Эта команда создает **набор записей** с именем _sip. _tcp в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="fe4f0-148">Набор записей имеет тип SRV и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="fe4f0-149">Она состоит из одной записи DNS, указывающей на IP-адрес 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="fe4f0-150">Служба SIP и протокол TCP задаются как часть имени набора записей, а не как часть данных записи.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="fe4f0-151">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="fe4f0-152">Пример 8: создание набора записей типа TXT</span><span class="sxs-lookup"><span data-stu-id="fe4f0-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="fe4f0-153">Эта команда создает **набор записей** с именем, указанным в MyZone.com Zone.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="fe4f0-154">Набор записей имеет тип TXT и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="fe4f0-155">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-155">It contains a single DNS record.</span></span>

<span data-ttu-id="fe4f0-156">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="fe4f0-157">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe4f0-157">PARAMETERS</span></span>

### <span data-ttu-id="fe4f0-158">-CNAME</span><span class="sxs-lookup"><span data-stu-id="fe4f0-158">-Cname</span></span>
<span data-ttu-id="fe4f0-159">Задает доменное имя для записи канонического имени (CNAME).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-159">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4f0-160">-Exchange</span><span class="sxs-lookup"><span data-stu-id="fe4f0-160">-Exchange</span></span>
<span data-ttu-id="fe4f0-161">Указывает имя почтового сервера для записи почтового обменника (MX).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-161">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4f0-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="fe4f0-162">-Ipv4Address</span></span>
<span data-ttu-id="fe4f0-163">Задает IPv4-адрес для записи A.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-163">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="fe4f0-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="fe4f0-164">-Ipv6Address</span></span>
<span data-ttu-id="fe4f0-165">Задает IPv6-адрес для записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-165">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4f0-166">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="fe4f0-166">-Nsdname</span></span>
<span data-ttu-id="fe4f0-167">Указывает имя сервера доменных имен для записи сервера доменных имен (NS).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-167">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4f0-168">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="fe4f0-168">-Port</span></span>
<span data-ttu-id="fe4f0-169">Указывает порт для записи службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-169">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4f0-170">-Предпочтения</span><span class="sxs-lookup"><span data-stu-id="fe4f0-170">-Preference</span></span>
<span data-ttu-id="fe4f0-171">Задает приоритет MX-записи.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-171">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4f0-172">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="fe4f0-172">-Priority</span></span>
<span data-ttu-id="fe4f0-173">Указывает приоритет записи SRV.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-173">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4f0-174">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="fe4f0-174">-Ptrdname</span></span>
<span data-ttu-id="fe4f0-175">Указывает целевое доменное имя записи ресурса указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="fe4f0-175">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4f0-176">-Target</span><span class="sxs-lookup"><span data-stu-id="fe4f0-176">-Target</span></span>
<span data-ttu-id="fe4f0-177">Указывает целевой объект для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-177">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4f0-178">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="fe4f0-178">-Value</span></span>
<span data-ttu-id="fe4f0-179">Задает значение для записи TXT.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-179">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4f0-180">-Weight</span><span class="sxs-lookup"><span data-stu-id="fe4f0-180">-Weight</span></span>
<span data-ttu-id="fe4f0-181">Определяет вес записи SRV.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-181">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4f0-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4f0-182">CommonParameters</span></span>
<span data-ttu-id="fe4f0-183">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4f0-184">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe4f0-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4f0-185">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe4f0-185">INPUTS</span></span>

### <span data-ttu-id="fe4f0-186">Ничего.</span><span class="sxs-lookup"><span data-stu-id="fe4f0-186">None.</span></span>

## <span data-ttu-id="fe4f0-187">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe4f0-187">OUTPUTS</span></span>

### <span data-ttu-id="fe4f0-188">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="fe4f0-188">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="fe4f0-189">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe4f0-189">NOTES</span></span>

## <span data-ttu-id="fe4f0-190">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe4f0-190">RELATED LINKS</span></span>

[<span data-ttu-id="fe4f0-191">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="fe4f0-191">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="fe4f0-192">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fe4f0-192">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="fe4f0-193">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="fe4f0-193">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)
