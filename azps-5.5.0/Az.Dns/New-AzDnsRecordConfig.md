---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: cd503905cb36d14b0a0537978f02786da7189c33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234441"
---
# <span data-ttu-id="c31c8-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c31c8-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="c31c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c31c8-102">SYNOPSIS</span></span>
<span data-ttu-id="c31c8-103">Создает локальный объект DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="c31c8-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="c31c8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c31c8-104">SYNTAX</span></span>

### <span data-ttu-id="c31c8-105">A</span><span class="sxs-lookup"><span data-stu-id="c31c8-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31c8-106">Аааа</span><span class="sxs-lookup"><span data-stu-id="c31c8-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31c8-107">Ns</span><span class="sxs-lookup"><span data-stu-id="c31c8-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31c8-108">Mx</span><span class="sxs-lookup"><span data-stu-id="c31c8-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c31c8-109">Ptr</span><span class="sxs-lookup"><span data-stu-id="c31c8-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31c8-110">Txt</span><span class="sxs-lookup"><span data-stu-id="c31c8-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31c8-111">Srv</span><span class="sxs-lookup"><span data-stu-id="c31c8-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31c8-112">CName</span><span class="sxs-lookup"><span data-stu-id="c31c8-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31c8-113">Caa</span><span class="sxs-lookup"><span data-stu-id="c31c8-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c31c8-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c31c8-114">DESCRIPTION</span></span>
<span data-ttu-id="c31c8-115">Для создания локального объекта DnsRecordConfig будет создаваться новый объект **New-AzDnsRecordConfig.** </span><span class="sxs-lookup"><span data-stu-id="c31c8-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="c31c8-116">Массив этих объектов передается в New-AzDnsRecordSet с помощью параметра *DnsRecords,* чтобы указать записи, которые нужно создать в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="c31c8-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="c31c8-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c31c8-117">EXAMPLES</span></span>

### <span data-ttu-id="c31c8-118">Пример 1. Создание наборов записей типа A</span><span class="sxs-lookup"><span data-stu-id="c31c8-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="c31c8-119">В этом примере создается **набор записей с** именем www в зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c31c8-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c31c8-120">Набор записей имеет тип A и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="c31c8-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c31c8-121">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="c31c8-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="c31c8-122">Пример 2. Создание наборов записей типа AAAA</span><span class="sxs-lookup"><span data-stu-id="c31c8-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c31c8-123">В этом примере создается **набор записей с** именем www в зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c31c8-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c31c8-124">Набор записей имеет тип AAAA и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="c31c8-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c31c8-125">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="c31c8-125">It contains a single DNS record.</span></span>
<span data-ttu-id="c31c8-126">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="c31c8-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c31c8-127">Пример 3. Создание наборов записей типа CNAME</span><span class="sxs-lookup"><span data-stu-id="c31c8-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c31c8-128">В этом примере создается **набор записей с** именем www в зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c31c8-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c31c8-129">Набор записей имеет тип CNAME и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="c31c8-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c31c8-130">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="c31c8-130">It contains a single DNS record.</span></span>
<span data-ttu-id="c31c8-131">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="c31c8-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c31c8-132">Пример 4. Создание наборов записей типа MX</span><span class="sxs-lookup"><span data-stu-id="c31c8-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c31c8-133">Эта команда создает набор **записей с** именем www в зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c31c8-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c31c8-134">Набор записей имеет тип MX и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="c31c8-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c31c8-135">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="c31c8-135">It contains a single DNS record.</span></span>
<span data-ttu-id="c31c8-136">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="c31c8-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c31c8-137">Пример 5. Создание наборов записей типа NS</span><span class="sxs-lookup"><span data-stu-id="c31c8-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c31c8-138">Эта команда создает набор **записей с** именем ns1 в зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c31c8-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="c31c8-139">Набор записей имеет тип NS и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="c31c8-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c31c8-140">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="c31c8-140">It contains a single DNS record.</span></span>
<span data-ttu-id="c31c8-141">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="c31c8-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c31c8-142">Пример 6. Создание наборов записей типа PTR</span><span class="sxs-lookup"><span data-stu-id="c31c8-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="c31c8-143">Эта команда создает набор **записей с** именем 4 в зоне 3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="c31c8-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="c31c8-144">Набор записей имеет тип PTR и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="c31c8-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c31c8-145">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="c31c8-145">It contains a single DNS record.</span></span>
<span data-ttu-id="c31c8-146">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="c31c8-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c31c8-147">Пример 7. Создание наборов записей типа SRV</span><span class="sxs-lookup"><span data-stu-id="c31c8-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c31c8-148">Эта команда создает набор **записей с** именем _sip._tcp в myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c31c8-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="c31c8-149">Набор записей имеет тип SRV и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="c31c8-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c31c8-150">Она содержит одну запись DNS, указывав на IP-адрес 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="c31c8-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="c31c8-151">Служба (sip) и протокол (tcp) указаны как часть имени набора записей, а не как часть данных записи.</span><span class="sxs-lookup"><span data-stu-id="c31c8-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="c31c8-152">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="c31c8-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c31c8-153">Пример 8. Создание наборов записей типа TXT</span><span class="sxs-lookup"><span data-stu-id="c31c8-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c31c8-154">Эта команда создает **именуемую** команду RecordSet в myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c31c8-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="c31c8-155">Набор записей имеет тип TXT и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="c31c8-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c31c8-156">Она содержит одну запись DNS.</span><span class="sxs-lookup"><span data-stu-id="c31c8-156">It contains a single DNS record.</span></span>
<span data-ttu-id="c31c8-157">Чтобы создать набор **записей,** используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="c31c8-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="c31c8-158">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c31c8-158">PARAMETERS</span></span>

### <span data-ttu-id="c31c8-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="c31c8-159">-CaaFlags</span></span>
<span data-ttu-id="c31c8-160">Флаги для добавляемой записи CAA.</span><span class="sxs-lookup"><span data-stu-id="c31c8-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="c31c8-161">Должен быть числом от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="c31c8-161">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="c31c8-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="c31c8-162">-CaaTag</span></span>
<span data-ttu-id="c31c8-163">Поле тега добавляемой записи CAA.</span><span class="sxs-lookup"><span data-stu-id="c31c8-163">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="c31c8-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="c31c8-164">-CaaValue</span></span>
<span data-ttu-id="c31c8-165">Поле значения для добавляемой записи CAA.</span><span class="sxs-lookup"><span data-stu-id="c31c8-165">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="c31c8-166">-Cname</span><span class="sxs-lookup"><span data-stu-id="c31c8-166">-Cname</span></span>
<span data-ttu-id="c31c8-167">Указывает доменное имя для канонической записи (CNAME).</span><span class="sxs-lookup"><span data-stu-id="c31c8-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="c31c8-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c31c8-168">-DefaultProfile</span></span>
<span data-ttu-id="c31c8-169">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c31c8-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c31c8-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="c31c8-170">-Exchange</span></span>
<span data-ttu-id="c31c8-171">Имя сервера обмена электронной почтой для записи обмена электронной почтой (MX).</span><span class="sxs-lookup"><span data-stu-id="c31c8-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="c31c8-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="c31c8-172">-Ipv4Address</span></span>
<span data-ttu-id="c31c8-173">Определяет IPv4-адрес для записи A.</span><span class="sxs-lookup"><span data-stu-id="c31c8-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="c31c8-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="c31c8-174">-Ipv6Address</span></span>
<span data-ttu-id="c31c8-175">Определяет IPv6-адрес для записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="c31c8-175">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="c31c8-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="c31c8-176">-Nsdname</span></span>
<span data-ttu-id="c31c8-177">Указывает имя сервера доменных имен для записи сервера доменных имен.</span><span class="sxs-lookup"><span data-stu-id="c31c8-177">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="c31c8-178">-Port</span><span class="sxs-lookup"><span data-stu-id="c31c8-178">-Port</span></span>
<span data-ttu-id="c31c8-179">Порт для записи службы (SRV).</span><span class="sxs-lookup"><span data-stu-id="c31c8-179">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="c31c8-180">-Preference</span><span class="sxs-lookup"><span data-stu-id="c31c8-180">-Preference</span></span>
<span data-ttu-id="c31c8-181">Указывает параметр для записи MX.</span><span class="sxs-lookup"><span data-stu-id="c31c8-181">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="c31c8-182">-Priority</span><span class="sxs-lookup"><span data-stu-id="c31c8-182">-Priority</span></span>
<span data-ttu-id="c31c8-183">Определяет приоритет для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="c31c8-183">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="c31c8-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="c31c8-184">-Ptrdname</span></span>
<span data-ttu-id="c31c8-185">Указывает целевое доменное имя записи ресурса указателя (PTR).</span><span class="sxs-lookup"><span data-stu-id="c31c8-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="c31c8-186">-Target</span><span class="sxs-lookup"><span data-stu-id="c31c8-186">-Target</span></span>
<span data-ttu-id="c31c8-187">Указывает целевой объект для записи SRV.</span><span class="sxs-lookup"><span data-stu-id="c31c8-187">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="c31c8-188">-Value</span><span class="sxs-lookup"><span data-stu-id="c31c8-188">-Value</span></span>
<span data-ttu-id="c31c8-189">Определяет значение для записи TXT.</span><span class="sxs-lookup"><span data-stu-id="c31c8-189">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="c31c8-190">-Weight</span><span class="sxs-lookup"><span data-stu-id="c31c8-190">-Weight</span></span>
<span data-ttu-id="c31c8-191">Определяет вес записи SRV.</span><span class="sxs-lookup"><span data-stu-id="c31c8-191">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="c31c8-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c31c8-192">CommonParameters</span></span>
<span data-ttu-id="c31c8-193">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c31c8-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c31c8-194">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c31c8-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c31c8-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c31c8-195">INPUTS</span></span>

### <span data-ttu-id="c31c8-196">System.String</span><span class="sxs-lookup"><span data-stu-id="c31c8-196">System.String</span></span>

### <span data-ttu-id="c31c8-197">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="c31c8-197">System.UInt16</span></span>

### <span data-ttu-id="c31c8-198">System.Byte</span><span class="sxs-lookup"><span data-stu-id="c31c8-198">System.Byte</span></span>

## <span data-ttu-id="c31c8-199">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c31c8-199">OUTPUTS</span></span>

### <span data-ttu-id="c31c8-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="c31c8-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="c31c8-201">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c31c8-201">NOTES</span></span>

## <span data-ttu-id="c31c8-202">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c31c8-202">RELATED LINKS</span></span>

[<span data-ttu-id="c31c8-203">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c31c8-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="c31c8-204">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c31c8-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="c31c8-205">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c31c8-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
