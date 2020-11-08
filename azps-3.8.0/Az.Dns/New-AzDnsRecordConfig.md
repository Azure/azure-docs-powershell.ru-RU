---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: cd503905cb36d14b0a0537978f02786da7189c33
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065908"
---
# <span data-ttu-id="01ce7-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="01ce7-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="01ce7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="01ce7-103">Создание нового локального объекта записи DNS.</span><span class="sxs-lookup"><span data-stu-id="01ce7-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="01ce7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01ce7-104">SYNTAX</span></span>

### <span data-ttu-id="01ce7-105">Помощью</span><span class="sxs-lookup"><span data-stu-id="01ce7-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ce7-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="01ce7-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ce7-107">Службу</span><span class="sxs-lookup"><span data-stu-id="01ce7-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ce7-108">МХ</span><span class="sxs-lookup"><span data-stu-id="01ce7-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01ce7-109">Указателя</span><span class="sxs-lookup"><span data-stu-id="01ce7-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ce7-110">ТХТ</span><span class="sxs-lookup"><span data-stu-id="01ce7-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ce7-111">Могла</span><span class="sxs-lookup"><span data-stu-id="01ce7-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ce7-112">CName</span><span class="sxs-lookup"><span data-stu-id="01ce7-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ce7-113">Caa</span><span class="sxs-lookup"><span data-stu-id="01ce7-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01ce7-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01ce7-114">DESCRIPTION</span></span>
<span data-ttu-id="01ce7-115">Командлет **New-AzDnsRecordConfig** создает локальный объект **DnsRecord** .</span><span class="sxs-lookup"><span data-stu-id="01ce7-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="01ce7-116">Массив этих объектов передается в командлет New-AzDnsRecordSet с помощью параметра *DnsRecords* для указания записей для создания в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="01ce7-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="01ce7-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01ce7-117">EXAMPLES</span></span>

### <span data-ttu-id="01ce7-118">Пример 1: создание набора записей типа A</span><span class="sxs-lookup"><span data-stu-id="01ce7-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="01ce7-119">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="01ce7-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="01ce7-120">Набор записей имеет тип A и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="01ce7-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="01ce7-121">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="01ce7-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="01ce7-122">Пример 2: создание набора записей типа AAAA</span><span class="sxs-lookup"><span data-stu-id="01ce7-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="01ce7-123">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="01ce7-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="01ce7-124">Набор записей имеет тип AAAA и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="01ce7-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="01ce7-125">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="01ce7-125">It contains a single DNS record.</span></span>
<span data-ttu-id="01ce7-126">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="01ce7-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="01ce7-127">Пример 3: создание набора записей с типом CNAME</span><span class="sxs-lookup"><span data-stu-id="01ce7-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="01ce7-128">В этом примере в myzone.com зоны создается **набор записей** с именем www.</span><span class="sxs-lookup"><span data-stu-id="01ce7-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="01ce7-129">Набор записей имеет тип CNAME и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="01ce7-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="01ce7-130">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="01ce7-130">It contains a single DNS record.</span></span>
<span data-ttu-id="01ce7-131">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="01ce7-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="01ce7-132">Пример 4: создание набора записей типа MX</span><span class="sxs-lookup"><span data-stu-id="01ce7-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="01ce7-133">Эта команда создает **набор записей** с именем www в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="01ce7-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="01ce7-134">Набор записей имеет тип MX и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="01ce7-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="01ce7-135">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="01ce7-135">It contains a single DNS record.</span></span>
<span data-ttu-id="01ce7-136">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="01ce7-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="01ce7-137">Пример 5: создание набора записей с типом "NS"</span><span class="sxs-lookup"><span data-stu-id="01ce7-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="01ce7-138">Эта команда создает **набор записей** с именем ns1 в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="01ce7-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="01ce7-139">Набор записей имеет тип NS и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="01ce7-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="01ce7-140">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="01ce7-140">It contains a single DNS record.</span></span>
<span data-ttu-id="01ce7-141">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="01ce7-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="01ce7-142">Пример 6: создание набора записей типа PTR</span><span class="sxs-lookup"><span data-stu-id="01ce7-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="01ce7-143">Эта команда создает **набор записей** с именем 4 в зоне 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="01ce7-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="01ce7-144">Набор записей имеет тип PTR и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="01ce7-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="01ce7-145">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="01ce7-145">It contains a single DNS record.</span></span>
<span data-ttu-id="01ce7-146">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="01ce7-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="01ce7-147">Пример 7: создание набора записей типа SRV</span><span class="sxs-lookup"><span data-stu-id="01ce7-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="01ce7-148">Эта команда создает **набор записей** с именем _sip. _tcp в зоне MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="01ce7-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="01ce7-149">Набор записей имеет тип SRV и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="01ce7-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="01ce7-150">Она состоит из одной записи DNS, указывающей на IP-адрес 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="01ce7-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="01ce7-151">Служба SIP и протокол TCP задаются как часть имени набора записей, а не как часть данных записи.</span><span class="sxs-lookup"><span data-stu-id="01ce7-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="01ce7-152">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="01ce7-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="01ce7-153">Пример 8: создание набора записей типа TXT</span><span class="sxs-lookup"><span data-stu-id="01ce7-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="01ce7-154">Эта команда создает **набор записей** с именем, указанным в MyZone.com Zone.</span><span class="sxs-lookup"><span data-stu-id="01ce7-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="01ce7-155">Набор записей имеет тип TXT и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="01ce7-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="01ce7-156">Она состоит из одной записи DNS.</span><span class="sxs-lookup"><span data-stu-id="01ce7-156">It contains a single DNS record.</span></span>
<span data-ttu-id="01ce7-157">Чтобы создать набор **записей** с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="01ce7-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="01ce7-158">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01ce7-158">PARAMETERS</span></span>

### <span data-ttu-id="01ce7-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="01ce7-159">-CaaFlags</span></span>
<span data-ttu-id="01ce7-160">Флаги для записи CAA, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="01ce7-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="01ce7-161">Должно быть числом от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="01ce7-161">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="01ce7-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="01ce7-162">-CaaTag</span></span>
<span data-ttu-id="01ce7-163">Поле тега записи CAA, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="01ce7-163">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="01ce7-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="01ce7-164">-CaaValue</span></span>
<span data-ttu-id="01ce7-165">Поле значения для записи CAA, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="01ce7-165">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="01ce7-166">-CNAME</span><span class="sxs-lookup"><span data-stu-id="01ce7-166">-Cname</span></span>
<span data-ttu-id="01ce7-167">Задает доменное имя для записи канонического имени (CNAME).</span><span class="sxs-lookup"><span data-stu-id="01ce7-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="01ce7-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ce7-168">-DefaultProfile</span></span>
<span data-ttu-id="01ce7-169">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="01ce7-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01ce7-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="01ce7-170">-Exchange</span></span>
<span data-ttu-id="01ce7-171">Указывает имя почтового сервера для записи почтового обменника (MX).</span><span class="sxs-lookup"><span data-stu-id="01ce7-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="01ce7-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="01ce7-172">-Ipv4Address</span></span>
<span data-ttu-id="01ce7-173">Задает IPv4-адрес для записи A.</span><span class="sxs-lookup"><span data-stu-id="01ce7-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="01ce7-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="01ce7-174">-Ipv6Address</span></span>
<span data-ttu-id="01ce7-175">Задает IPv6-адрес для записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="01ce7-175">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="01ce7-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="01ce7-176">-Nsdname</span></span>
<span data-ttu-id="01ce7-177">Указывает имя сервера доменных имен для записи сервера доменных имен (NS).</span><span class="sxs-lookup"><span data-stu-id="01ce7-177">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="01ce7-178">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="01ce7-178">-Port</span></span>
<span data-ttu-id="01ce7-179">Указывает порт для записи службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="01ce7-179">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="01ce7-180">-Предпочтения</span><span class="sxs-lookup"><span data-stu-id="01ce7-180">-Preference</span></span>
<span data-ttu-id="01ce7-181">Задает приоритет MX-записи.</span><span class="sxs-lookup"><span data-stu-id="01ce7-181">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="01ce7-182">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="01ce7-182">-Priority</span></span>
<span data-ttu-id="01ce7-183">Указывает приоритет записи SRV.</span><span class="sxs-lookup"><span data-stu-id="01ce7-183">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="01ce7-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="01ce7-184">-Ptrdname</span></span>
<span data-ttu-id="01ce7-185">Указывает целевое доменное имя записи ресурса указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="01ce7-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="01ce7-186">-Target</span><span class="sxs-lookup"><span data-stu-id="01ce7-186">-Target</span></span>
<span data-ttu-id="01ce7-187">Указывает целевой объект для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="01ce7-187">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="01ce7-188">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="01ce7-188">-Value</span></span>
<span data-ttu-id="01ce7-189">Задает значение для записи TXT.</span><span class="sxs-lookup"><span data-stu-id="01ce7-189">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="01ce7-190">-Weight</span><span class="sxs-lookup"><span data-stu-id="01ce7-190">-Weight</span></span>
<span data-ttu-id="01ce7-191">Определяет вес записи SRV.</span><span class="sxs-lookup"><span data-stu-id="01ce7-191">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="01ce7-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ce7-192">CommonParameters</span></span>
<span data-ttu-id="01ce7-193">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01ce7-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ce7-194">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01ce7-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ce7-195">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01ce7-195">INPUTS</span></span>

### <span data-ttu-id="01ce7-196">System. String</span><span class="sxs-lookup"><span data-stu-id="01ce7-196">System.String</span></span>

### <span data-ttu-id="01ce7-197">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="01ce7-197">System.UInt16</span></span>

### <span data-ttu-id="01ce7-198">System. Byte</span><span class="sxs-lookup"><span data-stu-id="01ce7-198">System.Byte</span></span>

## <span data-ttu-id="01ce7-199">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01ce7-199">OUTPUTS</span></span>

### <span data-ttu-id="01ce7-200">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="01ce7-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="01ce7-201">Пуск</span><span class="sxs-lookup"><span data-stu-id="01ce7-201">NOTES</span></span>

## <span data-ttu-id="01ce7-202">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01ce7-202">RELATED LINKS</span></span>

[<span data-ttu-id="01ce7-203">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="01ce7-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="01ce7-204">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="01ce7-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="01ce7-205">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="01ce7-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
