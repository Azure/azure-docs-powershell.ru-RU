---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 98418beaf029b1e1a40ec78fa2a794c2218ab753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568074"
---
# <span data-ttu-id="d7d57-101">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d7d57-101">New-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="d7d57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7d57-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d57-103">Создание нового локального объекта записи DNS.</span><span class="sxs-lookup"><span data-stu-id="d7d57-103">Creates a new DNS record local object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7d57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7d57-104">SYNTAX</span></span>

### <span data-ttu-id="d7d57-105">Помощью</span><span class="sxs-lookup"><span data-stu-id="d7d57-105">A</span></span>
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7d57-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="d7d57-106">Aaaa</span></span>
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7d57-107">Службу</span><span class="sxs-lookup"><span data-stu-id="d7d57-107">Ns</span></span>
```
New-AzureRmDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7d57-108">МХ</span><span class="sxs-lookup"><span data-stu-id="d7d57-108">Mx</span></span>
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7d57-109">Указателя</span><span class="sxs-lookup"><span data-stu-id="d7d57-109">Ptr</span></span>
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7d57-110">ТХТ</span><span class="sxs-lookup"><span data-stu-id="d7d57-110">Txt</span></span>
```
New-AzureRmDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7d57-111">Могла</span><span class="sxs-lookup"><span data-stu-id="d7d57-111">Srv</span></span>
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7d57-112">CName</span><span class="sxs-lookup"><span data-stu-id="d7d57-112">CName</span></span>
```
New-AzureRmDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7d57-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7d57-113">DESCRIPTION</span></span>
<span data-ttu-id="d7d57-114">Командлет **New-AzureRmDnsRecordConfig** создает локальный объект **DnsRecord** .</span><span class="sxs-lookup"><span data-stu-id="d7d57-114">The **New-AzureRmDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="d7d57-115">Массив этих объектов передается в командлет New-AzureRmDnsRecordSet с помощью параметра *DnsRecords* для указания записей для создания в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="d7d57-115">An array of these objects is passed to the New-AzureRmDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="d7d57-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7d57-116">EXAMPLES</span></span>

### <span data-ttu-id="d7d57-117">Пример 1: создание набора записей типа A</span><span class="sxs-lookup"><span data-stu-id="d7d57-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="d7d57-118">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="d7d57-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d7d57-119">Набор записей имеет тип A и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="d7d57-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d7d57-120">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="d7d57-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="d7d57-121">Пример 2: создание набора записей типа AAAA</span><span class="sxs-lookup"><span data-stu-id="d7d57-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d7d57-122">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="d7d57-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d7d57-123">Набор записей имеет тип AAAA и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="d7d57-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d7d57-124">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="d7d57-124">It contains a single DNS record.</span></span>

<span data-ttu-id="d7d57-125">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="d7d57-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7d57-126">Пример 3: создание набора записей с типом CNAME</span><span class="sxs-lookup"><span data-stu-id="d7d57-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d7d57-127">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="d7d57-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d7d57-128">Набор записей имеет тип CNAME и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="d7d57-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d7d57-129">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="d7d57-129">It contains a single DNS record.</span></span>

<span data-ttu-id="d7d57-130">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="d7d57-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7d57-131">Пример 4: создание набора записей типа MX</span><span class="sxs-lookup"><span data-stu-id="d7d57-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d7d57-132">Эта команда создает **набор записей** с именем www в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d7d57-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d7d57-133">Набор записей имеет тип MX и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="d7d57-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d7d57-134">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="d7d57-134">It contains a single DNS record.</span></span>

<span data-ttu-id="d7d57-135">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="d7d57-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7d57-136">Пример 5: создание набора записей с типом "NS"</span><span class="sxs-lookup"><span data-stu-id="d7d57-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d7d57-137">Эта команда создает **набор записей** с именем ns1 в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d7d57-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="d7d57-138">Набор записей имеет тип NS и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="d7d57-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d7d57-139">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="d7d57-139">It contains a single DNS record.</span></span>

<span data-ttu-id="d7d57-140">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="d7d57-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7d57-141">Пример 6: создание набора записей типа PTR</span><span class="sxs-lookup"><span data-stu-id="d7d57-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="d7d57-142">Эта команда создает **набор записей** с именем 4 в зоне 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="d7d57-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="d7d57-143">Набор записей имеет тип PTR и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="d7d57-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d7d57-144">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="d7d57-144">It contains a single DNS record.</span></span>

<span data-ttu-id="d7d57-145">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="d7d57-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7d57-146">Пример 7: создание набора записей типа SRV</span><span class="sxs-lookup"><span data-stu-id="d7d57-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d7d57-147">Эта команда создает **набор записей** с именем _sip. _tcp в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d7d57-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="d7d57-148">Набор записей имеет тип SRV и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="d7d57-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d7d57-149">Она состоит из одной записи DNS, указывающей на IP-адрес 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="d7d57-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="d7d57-150">Служба SIP и протокол TCP задаются как часть имени набора записей, а не как часть данных записи.</span><span class="sxs-lookup"><span data-stu-id="d7d57-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="d7d57-151">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="d7d57-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d7d57-152">Пример 8: создание набора записей типа TXT</span><span class="sxs-lookup"><span data-stu-id="d7d57-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d7d57-153">Эта команда создает **набор записей** с именем, указанным в MyZone.com Zone.</span><span class="sxs-lookup"><span data-stu-id="d7d57-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="d7d57-154">Набор записей имеет тип TXT и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="d7d57-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d7d57-155">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="d7d57-155">It contains a single DNS record.</span></span>

<span data-ttu-id="d7d57-156">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="d7d57-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="d7d57-157">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7d57-157">PARAMETERS</span></span>

### <span data-ttu-id="d7d57-158">-CNAME</span><span class="sxs-lookup"><span data-stu-id="d7d57-158">-Cname</span></span>
<span data-ttu-id="d7d57-159">Задает доменное имя для записи канонического имени (CNAME).</span><span class="sxs-lookup"><span data-stu-id="d7d57-159">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d57-160">-Exchange</span><span class="sxs-lookup"><span data-stu-id="d7d57-160">-Exchange</span></span>
<span data-ttu-id="d7d57-161">Указывает имя почтового сервера для записи почтового обменника (MX).</span><span class="sxs-lookup"><span data-stu-id="d7d57-161">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d57-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="d7d57-162">-Ipv4Address</span></span>
<span data-ttu-id="d7d57-163">Задает IPv4-адрес для записи A.</span><span class="sxs-lookup"><span data-stu-id="d7d57-163">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="d7d57-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="d7d57-164">-Ipv6Address</span></span>
<span data-ttu-id="d7d57-165">Задает IPv6-адрес для записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="d7d57-165">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d57-166">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="d7d57-166">-Nsdname</span></span>
<span data-ttu-id="d7d57-167">Указывает имя сервера доменных имен для записи сервера доменных имен (NS).</span><span class="sxs-lookup"><span data-stu-id="d7d57-167">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d57-168">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="d7d57-168">-Port</span></span>
<span data-ttu-id="d7d57-169">Указывает порт для записи службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="d7d57-169">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d57-170">-Предпочтения</span><span class="sxs-lookup"><span data-stu-id="d7d57-170">-Preference</span></span>
<span data-ttu-id="d7d57-171">Задает приоритет MX-записи.</span><span class="sxs-lookup"><span data-stu-id="d7d57-171">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d57-172">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="d7d57-172">-Priority</span></span>
<span data-ttu-id="d7d57-173">Указывает приоритет записи SRV.</span><span class="sxs-lookup"><span data-stu-id="d7d57-173">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d57-174">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="d7d57-174">-Ptrdname</span></span>
<span data-ttu-id="d7d57-175">Указывает целевое доменное имя записи ресурса указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="d7d57-175">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d57-176">-Target</span><span class="sxs-lookup"><span data-stu-id="d7d57-176">-Target</span></span>
<span data-ttu-id="d7d57-177">Указывает целевой объект для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="d7d57-177">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d57-178">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="d7d57-178">-Value</span></span>
<span data-ttu-id="d7d57-179">Задает значение для записи TXT.</span><span class="sxs-lookup"><span data-stu-id="d7d57-179">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d57-180">-Weight</span><span class="sxs-lookup"><span data-stu-id="d7d57-180">-Weight</span></span>
<span data-ttu-id="d7d57-181">Определяет вес записи SRV.</span><span class="sxs-lookup"><span data-stu-id="d7d57-181">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7d57-182">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d57-182">-DefaultProfile</span></span>
<span data-ttu-id="d7d57-183">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d57-183">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7d57-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d57-184">CommonParameters</span></span>
<span data-ttu-id="d7d57-185">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7d57-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d57-186">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7d57-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d57-187">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7d57-187">INPUTS</span></span>

### <span data-ttu-id="d7d57-188">Ничего.</span><span class="sxs-lookup"><span data-stu-id="d7d57-188">None.</span></span>

## <span data-ttu-id="d7d57-189">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7d57-189">OUTPUTS</span></span>

### <span data-ttu-id="d7d57-190">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="d7d57-190">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="d7d57-191">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7d57-191">NOTES</span></span>

## <span data-ttu-id="d7d57-192">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7d57-192">RELATED LINKS</span></span>

[<span data-ttu-id="d7d57-193">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d7d57-193">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="d7d57-194">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d7d57-194">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="d7d57-195">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d7d57-195">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)
