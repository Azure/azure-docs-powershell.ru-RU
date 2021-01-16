---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: f828c422447768ff59aea413eeca036a60877b09
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424775"
---
# <span data-ttu-id="a4b18-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a4b18-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="a4b18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4b18-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b18-103">Создает локальный объект личной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="a4b18-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="a4b18-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a4b18-104">SYNTAX</span></span>

### <span data-ttu-id="a4b18-105">A (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4b18-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4b18-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="a4b18-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4b18-107">MX</span><span class="sxs-lookup"><span data-stu-id="a4b18-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4b18-108">PTR</span><span class="sxs-lookup"><span data-stu-id="a4b18-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b18-109">TXT</span><span class="sxs-lookup"><span data-stu-id="a4b18-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b18-110">SRV</span><span class="sxs-lookup"><span data-stu-id="a4b18-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b18-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="a4b18-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4b18-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4b18-112">DESCRIPTION</span></span>
<span data-ttu-id="a4b18-113">С New-AzPrivateDnsRecordConfig создается локальный объект PSPrivateDnsRecord.</span><span class="sxs-lookup"><span data-stu-id="a4b18-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="a4b18-114">Массив этих объектов передается в New-AzPrivateDnsRecordSet с помощью параметра PrivateDnsRecord, чтобы указать записи, которые нужно создать в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="a4b18-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="a4b18-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a4b18-115">EXAMPLES</span></span>

### <span data-ttu-id="a4b18-116">Пример 1. Создание наборов записей типа A</span><span class="sxs-lookup"><span data-stu-id="a4b18-116">Example 1: Create a RecordSet of type A</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a4b18-117">В этом примере создается набор записей с именем www в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a4b18-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="a4b18-118">Набор записей имеет тип A и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="a4b18-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a4b18-119">Она содержит одну частную запись DNS.</span><span class="sxs-lookup"><span data-stu-id="a4b18-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="a4b18-120">Пример 2. Создание наборов записей типа AAAA</span><span class="sxs-lookup"><span data-stu-id="a4b18-120">Example 2: Create a RecordSet of type AAAA</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a4b18-121">В этом примере создается набор записей с именем www в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a4b18-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="a4b18-122">Набор записей имеет тип AAAA и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="a4b18-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a4b18-123">Она содержит одну частную запись DNS.</span><span class="sxs-lookup"><span data-stu-id="a4b18-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="a4b18-124">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="a4b18-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a4b18-125">Пример 3. Создание наборов записей типа CNAME</span><span class="sxs-lookup"><span data-stu-id="a4b18-125">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a4b18-126">В этом примере создается набор записей с именем www в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a4b18-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="a4b18-127">Набор записей имеет тип CNAME и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="a4b18-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a4b18-128">Она содержит одну частную запись DNS.</span><span class="sxs-lookup"><span data-stu-id="a4b18-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="a4b18-129">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="a4b18-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a4b18-130">Пример 4. Создание наборов записей типа MX</span><span class="sxs-lookup"><span data-stu-id="a4b18-130">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a4b18-131">Эта команда создает набор записей с именем www в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a4b18-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="a4b18-132">Набор записей имеет тип MX и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="a4b18-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a4b18-133">Она содержит одну частную запись DNS.</span><span class="sxs-lookup"><span data-stu-id="a4b18-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="a4b18-134">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="a4b18-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a4b18-135">Пример 5. Создание наборов записей типа PTR</span><span class="sxs-lookup"><span data-stu-id="a4b18-135">Example 5: Create a RecordSet of type PTR</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a4b18-136">Эта команда создает набор записей с именем 4 в частной зоне 3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="a4b18-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="a4b18-137">Набор записей имеет тип PTR и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="a4b18-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a4b18-138">Она содержит одну частную запись DNS.</span><span class="sxs-lookup"><span data-stu-id="a4b18-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="a4b18-139">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="a4b18-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a4b18-140">Пример 6. Создание recordSet типа SRV</span><span class="sxs-lookup"><span data-stu-id="a4b18-140">Example 6: Create a RecordSet of type SRV</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a4b18-141">Эта команда создает набор записей с именем _sip._tcp в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a4b18-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="a4b18-142">Набор записей имеет тип SRV и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="a4b18-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a4b18-143">Она содержит одну личную запись DNS, указывав на IP-адрес 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="a4b18-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="a4b18-144">Служба (sip) и протокол (tcp) указаны как часть имени набора записей, а не как часть данных записи.</span><span class="sxs-lookup"><span data-stu-id="a4b18-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="a4b18-145">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="a4b18-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="a4b18-146">Пример 7. Создание наборов записей типа TXT</span><span class="sxs-lookup"><span data-stu-id="a4b18-146">Example 7: Create a RecordSet of type TXT</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="a4b18-147">Эта команда создает набор записей с именем текста в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="a4b18-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="a4b18-148">Набор записей имеет тип TXT и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="a4b18-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="a4b18-149">Она содержит одну частную запись DNS.</span><span class="sxs-lookup"><span data-stu-id="a4b18-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="a4b18-150">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="a4b18-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="a4b18-151">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4b18-151">PARAMETERS</span></span>

### <span data-ttu-id="a4b18-152">-Cname</span><span class="sxs-lookup"><span data-stu-id="a4b18-152">-Cname</span></span>
<span data-ttu-id="a4b18-153">Каноническое имя добавляемой записи CNAME.</span><span class="sxs-lookup"><span data-stu-id="a4b18-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="a4b18-154">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="a4b18-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="a4b18-155">Не должно быть точки, заканчиваемой точкой</span><span class="sxs-lookup"><span data-stu-id="a4b18-155">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b18-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b18-156">-DefaultProfile</span></span>
<span data-ttu-id="a4b18-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b18-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4b18-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="a4b18-158">-Exchange</span></span>
<span data-ttu-id="a4b18-159">Хост обмена электронной почтой для добавляемой записи MX.</span><span class="sxs-lookup"><span data-stu-id="a4b18-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="a4b18-160">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="a4b18-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="a4b18-161">Не должно быть точки, заканчиваемой точкой</span><span class="sxs-lookup"><span data-stu-id="a4b18-161">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b18-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="a4b18-162">-Ipv4Address</span></span>
<span data-ttu-id="a4b18-163">IPv4-адрес добавляемой записи A.</span><span class="sxs-lookup"><span data-stu-id="a4b18-163">The IPv4 address for the A record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b18-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="a4b18-164">-Ipv6Address</span></span>
<span data-ttu-id="a4b18-165">IPv6-адрес добавляемой записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="a4b18-165">The IPv6 address for the AAAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b18-166">-Port</span><span class="sxs-lookup"><span data-stu-id="a4b18-166">-Port</span></span>
<span data-ttu-id="a4b18-167">Номер порта для добавляемой записи SRV.</span><span class="sxs-lookup"><span data-stu-id="a4b18-167">The port number for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b18-168">-Preference</span><span class="sxs-lookup"><span data-stu-id="a4b18-168">-Preference</span></span>
<span data-ttu-id="a4b18-169">Значение параметра для добавляемой записи MX.</span><span class="sxs-lookup"><span data-stu-id="a4b18-169">The preference value for the MX record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b18-170">-Priority</span><span class="sxs-lookup"><span data-stu-id="a4b18-170">-Priority</span></span>
<span data-ttu-id="a4b18-171">SRV-запись приоритета, которая нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="a4b18-171">The priority value SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b18-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="a4b18-172">-Ptrdname</span></span>
<span data-ttu-id="a4b18-173">Целевой хост для добавляемой записи PTR.</span><span class="sxs-lookup"><span data-stu-id="a4b18-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="a4b18-174">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="a4b18-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="a4b18-175">Не должно быть точки, заканчиваемой точкой</span><span class="sxs-lookup"><span data-stu-id="a4b18-175">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b18-176">-Target</span><span class="sxs-lookup"><span data-stu-id="a4b18-176">-Target</span></span>
<span data-ttu-id="a4b18-177">Целевой хост для добавляемой записи SRV.</span><span class="sxs-lookup"><span data-stu-id="a4b18-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="a4b18-178">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="a4b18-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="a4b18-179">Не должно быть точки, заканчиваемой точкой</span><span class="sxs-lookup"><span data-stu-id="a4b18-179">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b18-180">-Value</span><span class="sxs-lookup"><span data-stu-id="a4b18-180">-Value</span></span>
<span data-ttu-id="a4b18-181">Текстовое значение добавляемой записи TXT.</span><span class="sxs-lookup"><span data-stu-id="a4b18-181">The text value for the TXT record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b18-182">-Weight</span><span class="sxs-lookup"><span data-stu-id="a4b18-182">-Weight</span></span>
<span data-ttu-id="a4b18-183">Значение веса для добавляемой записи SRV.</span><span class="sxs-lookup"><span data-stu-id="a4b18-183">The weight value for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b18-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b18-184">CommonParameters</span></span>
<span data-ttu-id="a4b18-185">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b18-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b18-186">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4b18-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b18-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4b18-187">INPUTS</span></span>

### <span data-ttu-id="a4b18-188">Нет</span><span class="sxs-lookup"><span data-stu-id="a4b18-188">None</span></span>

## <span data-ttu-id="a4b18-189">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4b18-189">OUTPUTS</span></span>

### <span data-ttu-id="a4b18-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a4b18-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="a4b18-191">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a4b18-191">NOTES</span></span>

## <span data-ttu-id="a4b18-192">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4b18-192">RELATED LINKS</span></span>
