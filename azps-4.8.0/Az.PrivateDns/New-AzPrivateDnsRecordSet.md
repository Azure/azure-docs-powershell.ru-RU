---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 1a7042c94457f23302aa8d2899475d7b117e65b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236673"
---
# <span data-ttu-id="847b6-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="847b6-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="847b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="847b6-102">SYNOPSIS</span></span>
<span data-ttu-id="847b6-103">Создает набор записей в частной зоне DNS.</span><span class="sxs-lookup"><span data-stu-id="847b6-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="847b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="847b6-104">SYNTAX</span></span>

### <span data-ttu-id="847b6-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="847b6-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="847b6-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="847b6-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="847b6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="847b6-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="847b6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="847b6-108">DESCRIPTION</span></span>
<span data-ttu-id="847b6-109">Командлет New-AzPrivateDnsRecordSet создает новый набор записей в частной системе доменных имен (DNS) с указанным именем и типом в указанной частной зоне.</span><span class="sxs-lookup"><span data-stu-id="847b6-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="847b6-110">Объект RecordSet — это набор частных DNS-записей с одинаковыми именами и типами.</span><span class="sxs-lookup"><span data-stu-id="847b6-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="847b6-111">Обратите внимание, что имя задается относительно частной зоны, а не полного имени.</span><span class="sxs-lookup"><span data-stu-id="847b6-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="847b6-112">Параметр PrivateDnsRecord указывает записи в заданном множестве записей.</span><span class="sxs-lookup"><span data-stu-id="847b6-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="847b6-113">Этот параметр берет на себя массив частных DNS-записей, созданный с помощью New-AzPrivateDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="847b6-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="847b6-114">Вы можете использовать оператор конвейера для передачи объекта PSPrivateDnsZone в этот командлет или передать объект PSPrivateDnsZone в качестве параметра зоны или задать зону по ее ResourceId, либо можно указать зону по имени.</span><span class="sxs-lookup"><span data-stu-id="847b6-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="847b6-115">Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="847b6-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="847b6-116">Если соответствующий набор записей уже существует (то же имя и тип записи), необходимо указать параметр перезаписи, в противном случае командлет не создаст новый набор записей.</span><span class="sxs-lookup"><span data-stu-id="847b6-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="847b6-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="847b6-117">EXAMPLES</span></span>

### <span data-ttu-id="847b6-118">Пример 1: создание набора записей типа A</span><span class="sxs-lookup"><span data-stu-id="847b6-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="847b6-119">В этом примере в частной зоне myzone.com создается набор записей с именем www.</span><span class="sxs-lookup"><span data-stu-id="847b6-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="847b6-120">Набор записей имеет тип A и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="847b6-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="847b6-121">Она состоит из одной частной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="847b6-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="847b6-122">Пример 2: создание набора записей типа AAAA</span><span class="sxs-lookup"><span data-stu-id="847b6-122">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="847b6-123">В этом примере в частной зоне myzone.com создается набор записей с именем www.</span><span class="sxs-lookup"><span data-stu-id="847b6-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="847b6-124">Набор записей имеет тип AAAA и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="847b6-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="847b6-125">Она состоит из одной частной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="847b6-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="847b6-126">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="847b6-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="847b6-127">Пример 3: создание набора записей с типом CNAME</span><span class="sxs-lookup"><span data-stu-id="847b6-127">Example 3: Create a RecordSet of type CNAME</span></span>
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

<span data-ttu-id="847b6-128">В этом примере в частной зоне myzone.com создается набор записей с именем www.</span><span class="sxs-lookup"><span data-stu-id="847b6-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="847b6-129">Набор записей имеет тип CNAME и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="847b6-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="847b6-130">Она состоит из одной частной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="847b6-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="847b6-131">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="847b6-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="847b6-132">Пример 4: создание набора записей типа MX</span><span class="sxs-lookup"><span data-stu-id="847b6-132">Example 4: Create a RecordSet of type MX</span></span>
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

<span data-ttu-id="847b6-133">Эта команда создает набор записей с именем www в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="847b6-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="847b6-134">Набор записей имеет тип MX и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="847b6-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="847b6-135">Она состоит из одной частной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="847b6-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="847b6-136">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="847b6-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="847b6-137">Пример 5: создание набора записей типа PTR</span><span class="sxs-lookup"><span data-stu-id="847b6-137">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="847b6-138">Эта команда создает набор записей с именем 4 в частной зоне 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="847b6-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="847b6-139">Набор записей имеет тип PTR и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="847b6-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="847b6-140">Она состоит из одной частной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="847b6-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="847b6-141">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="847b6-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="847b6-142">Пример 6: создание набора записей типа SRV</span><span class="sxs-lookup"><span data-stu-id="847b6-142">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="847b6-143">Эта команда создает набор записей с именем _sip. _tcp в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="847b6-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="847b6-144">Набор записей имеет тип SRV и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="847b6-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="847b6-145">Она состоит из одной частной DNS-записи, указывающей на IP-адрес 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="847b6-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="847b6-146">Служба SIP и протокол TCP задаются как часть имени набора записей, а не как часть данных записи.</span><span class="sxs-lookup"><span data-stu-id="847b6-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="847b6-147">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="847b6-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="847b6-148">Пример 7: создание набора записей типа TXT</span><span class="sxs-lookup"><span data-stu-id="847b6-148">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="847b6-149">Эта команда создает набор записей с именем в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="847b6-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="847b6-150">Набор записей имеет тип TXT и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="847b6-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="847b6-151">Она состоит из одной частной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="847b6-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="847b6-152">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="847b6-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="847b6-153">Пример 8: создание набора записей на уровне зоны Апекс</span><span class="sxs-lookup"><span data-stu-id="847b6-153">Example 8:  Create a RecordSet at the zone apex</span></span>
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

<span data-ttu-id="847b6-154">Эта команда создает набор записей на Апекс (или корневом уровне) частной зоны myzone.com.</span><span class="sxs-lookup"><span data-stu-id="847b6-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="847b6-155">Для этого в качестве имени для записи задано значение @ (в том числе двойные кавычки).</span><span class="sxs-lookup"><span data-stu-id="847b6-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="847b6-156">Вы не можете создавать записи CNAME на Апекс зоны.</span><span class="sxs-lookup"><span data-stu-id="847b6-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="847b6-157">Это ограничение, заданное в DNS-стандартах. Это не является ограничением службы Azure Private DNS.</span><span class="sxs-lookup"><span data-stu-id="847b6-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="847b6-158">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="847b6-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="847b6-159">Пример 9: создание набора записей с подстановочными знаками</span><span class="sxs-lookup"><span data-stu-id="847b6-159">Example 9:  Create a wildcard Record Set</span></span>

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

<span data-ttu-id="847b6-160">Эта команда создает набор записей с именем \* в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="847b6-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="847b6-161">Это набор подстановочных записей.</span><span class="sxs-lookup"><span data-stu-id="847b6-161">This is a wildcard record set.</span></span> <span data-ttu-id="847b6-162">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="847b6-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="847b6-163">Пример 10: создание пустого множества записей</span><span class="sxs-lookup"><span data-stu-id="847b6-163">Example 10:  Create an empty Record Set</span></span>

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

<span data-ttu-id="847b6-164">Эта команда создает набор записей с именем \* в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="847b6-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="847b6-165">Набор записей имеет тип A и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="847b6-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="847b6-166">Это пустой набор записей, который выступает в качестве заполнителя, в который позже можно добавлять записи.</span><span class="sxs-lookup"><span data-stu-id="847b6-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="847b6-167">Пример 11: создание набор записей и отключение всех подтверждений</span><span class="sxs-lookup"><span data-stu-id="847b6-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="847b6-168">Эта команда создает набор записей.</span><span class="sxs-lookup"><span data-stu-id="847b6-168">This command creates a RecordSet.</span></span> <span data-ttu-id="847b6-169">Параметр перезаписи гарантирует, что этот элемент будет перезаписывать все существующие наборы записей с таким же именем и типом (существующие записи из этого множества будут утрачены).</span><span class="sxs-lookup"><span data-stu-id="847b6-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="847b6-170">Параметр Confirm со значением $False подавляет вывод запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="847b6-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="847b6-171">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="847b6-171">PARAMETERS</span></span>

### <span data-ttu-id="847b6-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="847b6-172">-DefaultProfile</span></span>
<span data-ttu-id="847b6-173">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="847b6-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="847b6-174">-Metadata</span><span class="sxs-lookup"><span data-stu-id="847b6-174">-Metadata</span></span>
<span data-ttu-id="847b6-175">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="847b6-175">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="847b6-176">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="847b6-176">-Name</span></span>
<span data-ttu-id="847b6-177">Имена записей в наборе записей (относительно имени зоны и без точки).</span><span class="sxs-lookup"><span data-stu-id="847b6-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="847b6-178">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="847b6-178">-Overwrite</span></span>
<span data-ttu-id="847b6-179">Не завершать ошибку, если такой наборы записей уже есть.</span><span class="sxs-lookup"><span data-stu-id="847b6-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="847b6-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="847b6-180">-ParentResourceId</span></span>
<span data-ttu-id="847b6-181">Частный секретный ИД зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="847b6-181">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="847b6-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="847b6-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="847b6-183">Закрытые записи DNS, являющиеся частью этого набора записей.</span><span class="sxs-lookup"><span data-stu-id="847b6-183">The private dns records that are part of this record set.</span></span>

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

### <span data-ttu-id="847b6-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="847b6-184">-RecordType</span></span>
<span data-ttu-id="847b6-185">Тип частных DNS-записей в этом наборе записей.</span><span class="sxs-lookup"><span data-stu-id="847b6-185">The type of Private DNS records in this record set.</span></span>

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

### <span data-ttu-id="847b6-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="847b6-186">-ResourceGroupName</span></span>
<span data-ttu-id="847b6-187">Группа ресурсов, к которой принадлежит зона.</span><span class="sxs-lookup"><span data-stu-id="847b6-187">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="847b6-188">-TTL</span><span class="sxs-lookup"><span data-stu-id="847b6-188">-Ttl</span></span>
<span data-ttu-id="847b6-189">Значение TTL для всех записей в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="847b6-189">The TTL value of all the records in this record set.</span></span>

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

### <span data-ttu-id="847b6-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="847b6-190">-Zone</span></span>
<span data-ttu-id="847b6-191">Объект PrivateDnsZone, представляющий зону, в которой нужно создать набор записей.</span><span class="sxs-lookup"><span data-stu-id="847b6-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="847b6-192">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="847b6-192">-ZoneName</span></span>
<span data-ttu-id="847b6-193">Зона, в которой нужно создать набор записей (без точки завершения).</span><span class="sxs-lookup"><span data-stu-id="847b6-193">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="847b6-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="847b6-194">-Confirm</span></span>
<span data-ttu-id="847b6-195">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="847b6-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="847b6-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="847b6-196">-WhatIf</span></span>
<span data-ttu-id="847b6-197">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="847b6-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="847b6-198">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="847b6-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="847b6-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="847b6-199">CommonParameters</span></span>
<span data-ttu-id="847b6-200">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="847b6-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="847b6-201">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="847b6-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="847b6-202">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="847b6-202">INPUTS</span></span>

### <span data-ttu-id="847b6-203">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="847b6-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="847b6-204">System. String</span><span class="sxs-lookup"><span data-stu-id="847b6-204">System.String</span></span>

## <span data-ttu-id="847b6-205">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="847b6-205">OUTPUTS</span></span>

### <span data-ttu-id="847b6-206">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="847b6-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="847b6-207">Пуск</span><span class="sxs-lookup"><span data-stu-id="847b6-207">NOTES</span></span>

## <span data-ttu-id="847b6-208">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="847b6-208">RELATED LINKS</span></span>
