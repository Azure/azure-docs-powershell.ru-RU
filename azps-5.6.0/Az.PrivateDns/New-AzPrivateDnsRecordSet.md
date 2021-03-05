---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7779cf8b357bab9480a9b811303bb19f1f0a6799
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965592"
---
# <span data-ttu-id="83ec0-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="83ec0-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="83ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="83ec0-103">Создает набор записей в частной зоне DNS.</span><span class="sxs-lookup"><span data-stu-id="83ec0-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="83ec0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="83ec0-104">SYNTAX</span></span>

### <span data-ttu-id="83ec0-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="83ec0-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83ec0-106">Объект</span><span class="sxs-lookup"><span data-stu-id="83ec0-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83ec0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="83ec0-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83ec0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83ec0-108">DESCRIPTION</span></span>
<span data-ttu-id="83ec0-109">С New-AzPrivateDnsRecordSet создается новый набор записей DNS с указанным именем и типом в указанной частной зоне.</span><span class="sxs-lookup"><span data-stu-id="83ec0-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="83ec0-110">Объект RecordSet — это набор частных записей DNS с одинаковым именем и типом.</span><span class="sxs-lookup"><span data-stu-id="83ec0-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="83ec0-111">Обратите внимание, что имя является относительно закрытой зоны, а не полного имени.</span><span class="sxs-lookup"><span data-stu-id="83ec0-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="83ec0-112">Параметр PrivateDnsRecord определяет записи в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="83ec0-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="83ec0-113">Этот параметр использует массив частных записей DNS, построенный с использованием New-AzPrivateDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="83ec0-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="83ec0-114">С помощью оператора конвейера можно передать объект PSPrivateDnsZone этому cmdlet или передать объект PSPrivateDnsZone в качестве параметра зоны. Кроме того, вы можете указать зону по ее коду ResourceId или указать ее по имени.</span><span class="sxs-lookup"><span data-stu-id="83ec0-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="83ec0-115">С помощью переменных Confirm и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83ec0-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="83ec0-116">Если совпадающий набор записей уже существует (то же имя и тип записи), необходимо указать параметр Overwrite, иначе командлет не создаст новый Набор записей.</span><span class="sxs-lookup"><span data-stu-id="83ec0-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="83ec0-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="83ec0-117">EXAMPLES</span></span>

### <span data-ttu-id="83ec0-118">Пример 1. Создание наборов записей типа A</span><span class="sxs-lookup"><span data-stu-id="83ec0-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="83ec0-119">В этом примере создается набор записей с именем www в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="83ec0-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="83ec0-120">Набор записей имеет тип A и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="83ec0-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="83ec0-121">Она содержит одну частную запись DNS.</span><span class="sxs-lookup"><span data-stu-id="83ec0-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="83ec0-122">Пример 2. Создание наборов записей типа AAAA</span><span class="sxs-lookup"><span data-stu-id="83ec0-122">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="83ec0-123">В этом примере создается набор записей с именем www в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="83ec0-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="83ec0-124">Набор записей имеет тип AAAA и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="83ec0-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="83ec0-125">Она содержит одну частную запись DNS.</span><span class="sxs-lookup"><span data-stu-id="83ec0-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="83ec0-126">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="83ec0-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="83ec0-127">Пример 3. Создание наборов записей типа CNAME</span><span class="sxs-lookup"><span data-stu-id="83ec0-127">Example 3: Create a RecordSet of type CNAME</span></span>
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

<span data-ttu-id="83ec0-128">В этом примере создается набор записей с именем www в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="83ec0-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="83ec0-129">Набор записей имеет тип CNAME и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="83ec0-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="83ec0-130">Она содержит одну частную запись DNS.</span><span class="sxs-lookup"><span data-stu-id="83ec0-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="83ec0-131">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="83ec0-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="83ec0-132">Пример 4. Создание наборов записей типа MX</span><span class="sxs-lookup"><span data-stu-id="83ec0-132">Example 4: Create a RecordSet of type MX</span></span>
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

<span data-ttu-id="83ec0-133">Эта команда создает набор записей с именем www в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="83ec0-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="83ec0-134">Набор записей имеет тип MX и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="83ec0-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="83ec0-135">Она содержит одну частную запись DNS.</span><span class="sxs-lookup"><span data-stu-id="83ec0-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="83ec0-136">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="83ec0-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="83ec0-137">Пример 5. Создание наборов записей типа PTR</span><span class="sxs-lookup"><span data-stu-id="83ec0-137">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="83ec0-138">Эта команда создает набор записей с именем 4 в частной зоне 3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="83ec0-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="83ec0-139">Набор записей имеет тип PTR и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="83ec0-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="83ec0-140">Она содержит одну частную запись DNS.</span><span class="sxs-lookup"><span data-stu-id="83ec0-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="83ec0-141">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="83ec0-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="83ec0-142">Пример 6. Создание наборов записей типа SRV</span><span class="sxs-lookup"><span data-stu-id="83ec0-142">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="83ec0-143">Эта команда создает набор записей с именем _sip._tcp в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="83ec0-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="83ec0-144">Набор записей имеет тип SRV и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="83ec0-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="83ec0-145">Она содержит одну частную запись DNS, указывав на IP-адрес 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="83ec0-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="83ec0-146">Служба (sip) и протокол (tcp) указаны как часть имени набора записей, а не как часть данных записи.</span><span class="sxs-lookup"><span data-stu-id="83ec0-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="83ec0-147">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="83ec0-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="83ec0-148">Пример 7. Создание наборов записей типа TXT</span><span class="sxs-lookup"><span data-stu-id="83ec0-148">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="83ec0-149">Эта команда создает набор записей с именем текста в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="83ec0-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="83ec0-150">Набор записей имеет тип TXT и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="83ec0-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="83ec0-151">Она содержит одну частную запись DNS.</span><span class="sxs-lookup"><span data-stu-id="83ec0-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="83ec0-152">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="83ec0-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="83ec0-153">Пример 8. Создание наборов записей в апексе зоны</span><span class="sxs-lookup"><span data-stu-id="83ec0-153">Example 8:  Create a RecordSet at the zone apex</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="83ec0-154">Эта команда создает набор записей в апексе (корневом) частного myzone.com.</span><span class="sxs-lookup"><span data-stu-id="83ec0-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="83ec0-155">Для этого имя набора записей задано как @(включая двойные кавычка).</span><span class="sxs-lookup"><span data-stu-id="83ec0-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="83ec0-156">Записи CNAME невозможно создать в апексе зоны.</span><span class="sxs-lookup"><span data-stu-id="83ec0-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="83ec0-157">Это ограничение стандартов DNS. Это не ограничение на частные DNS Azure.</span><span class="sxs-lookup"><span data-stu-id="83ec0-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="83ec0-158">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="83ec0-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="83ec0-159">Пример 9. Создание набора записей с подстройными знаками</span><span class="sxs-lookup"><span data-stu-id="83ec0-159">Example 9:  Create a wildcard Record Set</span></span>

```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="83ec0-160">Эта команда создает набор записей с именем \* в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="83ec0-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="83ec0-161">Это набор записей с поддиавными знаками.</span><span class="sxs-lookup"><span data-stu-id="83ec0-161">This is a wildcard record set.</span></span> <span data-ttu-id="83ec0-162">Чтобы создать набор записей, используя только одну строку pn_PowerShell_short или создать набор записей с несколькими записями, см. пример 1.</span><span class="sxs-lookup"><span data-stu-id="83ec0-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="83ec0-163">Пример 10. Создание пустого набора записей</span><span class="sxs-lookup"><span data-stu-id="83ec0-163">Example 10:  Create an empty Record Set</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords @()

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="83ec0-164">Эта команда создает набор записей с именем \* в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="83ec0-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="83ec0-165">Набор записей имеет тип A и имеет срок жизни 1 час (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="83ec0-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="83ec0-166">Это пустой набор записей, который выступать в качестве места для добавления записей.</span><span class="sxs-lookup"><span data-stu-id="83ec0-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="83ec0-167">Пример 11. Создание набора записей и подавления всего подтверждения</span><span class="sxs-lookup"><span data-stu-id="83ec0-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="83ec0-168">Эта команда создает набор записей.</span><span class="sxs-lookup"><span data-stu-id="83ec0-168">This command creates a RecordSet.</span></span> <span data-ttu-id="83ec0-169">Параметр "Перезаписать" гарантирует, что этот набор записей перезаписает все существующие записи с одинаковыми именами и типами (существующие записи в этом наборе будут потеряны).</span><span class="sxs-lookup"><span data-stu-id="83ec0-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="83ec0-170">Параметр Confirm со значением $False подавляет запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="83ec0-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="83ec0-171">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83ec0-171">PARAMETERS</span></span>

### <span data-ttu-id="83ec0-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ec0-172">-DefaultProfile</span></span>
<span data-ttu-id="83ec0-173">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83ec0-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83ec0-174">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="83ec0-174">-Metadata</span></span>
<span data-ttu-id="83ec0-175">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="83ec0-175">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ec0-176">-Name</span><span class="sxs-lookup"><span data-stu-id="83ec0-176">-Name</span></span>
<span data-ttu-id="83ec0-177">Имена записей в этом наборе записей (относительно имени зоны и без конечной точки).</span><span class="sxs-lookup"><span data-stu-id="83ec0-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ec0-178">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="83ec0-178">-Overwrite</span></span>
<span data-ttu-id="83ec0-179">Не сделайте сбой, если набор записей уже существует.</span><span class="sxs-lookup"><span data-stu-id="83ec0-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="83ec0-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="83ec0-180">-ParentResourceId</span></span>
<span data-ttu-id="83ec0-181">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="83ec0-181">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83ec0-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="83ec0-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="83ec0-183">Личные записи DNS, которые являются частью этого набора.</span><span class="sxs-lookup"><span data-stu-id="83ec0-183">The private dns records that are part of this record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordBase[]
Parameter Sets: (All)
Aliases: PrivateDnsRecords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ec0-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="83ec0-184">-RecordType</span></span>
<span data-ttu-id="83ec0-185">Тип личных записей DNS в этом наборе.</span><span class="sxs-lookup"><span data-stu-id="83ec0-185">The type of Private DNS records in this record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ec0-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83ec0-186">-ResourceGroupName</span></span>
<span data-ttu-id="83ec0-187">Группа ресурсов, к которой относится зона.</span><span class="sxs-lookup"><span data-stu-id="83ec0-187">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ec0-188">-Ttl</span><span class="sxs-lookup"><span data-stu-id="83ec0-188">-Ttl</span></span>
<span data-ttu-id="83ec0-189">Значение TTL для всех записей в этом наборе записей.</span><span class="sxs-lookup"><span data-stu-id="83ec0-189">The TTL value of all the records in this record set.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ec0-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="83ec0-190">-Zone</span></span>
<span data-ttu-id="83ec0-191">Объект PrivateDnsZone, представляющий зону, в которой создается набор записей.</span><span class="sxs-lookup"><span data-stu-id="83ec0-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83ec0-192">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="83ec0-192">-ZoneName</span></span>
<span data-ttu-id="83ec0-193">Зона, в которой создается набор записей (без завершающих точек).</span><span class="sxs-lookup"><span data-stu-id="83ec0-193">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ec0-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83ec0-194">-Confirm</span></span>
<span data-ttu-id="83ec0-195">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="83ec0-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ec0-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83ec0-196">-WhatIf</span></span>
<span data-ttu-id="83ec0-197">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83ec0-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83ec0-198">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="83ec0-198">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83ec0-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ec0-199">CommonParameters</span></span>
<span data-ttu-id="83ec0-200">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ec0-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ec0-201">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83ec0-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ec0-202">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83ec0-202">INPUTS</span></span>

### <span data-ttu-id="83ec0-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="83ec0-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="83ec0-204">System.String</span><span class="sxs-lookup"><span data-stu-id="83ec0-204">System.String</span></span>

## <span data-ttu-id="83ec0-205">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="83ec0-205">OUTPUTS</span></span>

### <span data-ttu-id="83ec0-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="83ec0-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="83ec0-207">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="83ec0-207">NOTES</span></span>

## <span data-ttu-id="83ec0-208">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83ec0-208">RELATED LINKS</span></span>
