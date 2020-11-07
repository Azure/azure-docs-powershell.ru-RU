---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: fc5686e22167613550b236bd234c649317ba8cca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905082"
---
# <span data-ttu-id="fc110-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="fc110-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="fc110-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc110-102">SYNOPSIS</span></span>
<span data-ttu-id="fc110-103">Создание нового локального объекта записи DNS.</span><span class="sxs-lookup"><span data-stu-id="fc110-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="fc110-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc110-104">SYNTAX</span></span>

### <span data-ttu-id="fc110-105">A (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc110-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc110-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="fc110-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc110-107">МХ</span><span class="sxs-lookup"><span data-stu-id="fc110-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc110-108">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="fc110-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc110-109">ТХТ</span><span class="sxs-lookup"><span data-stu-id="fc110-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc110-110">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="fc110-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc110-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="fc110-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc110-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc110-112">DESCRIPTION</span></span>
<span data-ttu-id="fc110-113">Командлет New-AzPrivateDnsRecordConfig создает локальный объект PSPrivateDnsRecord.</span><span class="sxs-lookup"><span data-stu-id="fc110-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="fc110-114">Массив этих объектов передается в командлет New-AzPrivateDnsRecordSet с помощью параметра PrivateDnsRecord для указания записей для создания в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="fc110-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="fc110-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc110-115">EXAMPLES</span></span>

### <span data-ttu-id="fc110-116">Пример 1: создание набора записей типа A</span><span class="sxs-lookup"><span data-stu-id="fc110-116">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="fc110-117">В этом примере в частной зоне myzone.com создается набор записей с именем www.</span><span class="sxs-lookup"><span data-stu-id="fc110-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="fc110-118">Набор записей имеет тип A и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fc110-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="fc110-119">Она состоит из одной частной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="fc110-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="fc110-120">Пример 2: создание набора записей типа AAAA</span><span class="sxs-lookup"><span data-stu-id="fc110-120">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="fc110-121">В этом примере в частной зоне myzone.com создается набор записей с именем www.</span><span class="sxs-lookup"><span data-stu-id="fc110-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="fc110-122">Набор записей имеет тип AAAA и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fc110-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="fc110-123">Она состоит из одной частной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="fc110-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="fc110-124">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fc110-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="fc110-125">Пример 3: создание набора записей с типом CNAME</span><span class="sxs-lookup"><span data-stu-id="fc110-125">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="fc110-126">В этом примере в частной зоне myzone.com создается набор записей с именем www.</span><span class="sxs-lookup"><span data-stu-id="fc110-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="fc110-127">Набор записей имеет тип CNAME и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fc110-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="fc110-128">Она состоит из одной частной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="fc110-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="fc110-129">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fc110-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="fc110-130">Пример 4: создание набора записей типа MX</span><span class="sxs-lookup"><span data-stu-id="fc110-130">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="fc110-131">Эта команда создает набор записей с именем www в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="fc110-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="fc110-132">Набор записей имеет тип MX и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fc110-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="fc110-133">Она состоит из одной частной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="fc110-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="fc110-134">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fc110-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="fc110-135">Пример 5: создание набора записей типа PTR</span><span class="sxs-lookup"><span data-stu-id="fc110-135">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="fc110-136">Эта команда создает набор записей с именем 4 в частной зоне 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="fc110-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="fc110-137">Набор записей имеет тип PTR и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fc110-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="fc110-138">Она состоит из одной частной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="fc110-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="fc110-139">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fc110-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="fc110-140">Пример 6: создание набора записей типа SRV</span><span class="sxs-lookup"><span data-stu-id="fc110-140">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="fc110-141">Эта команда создает набор записей с именем _sip. _tcp в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="fc110-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="fc110-142">Набор записей имеет тип SRV и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fc110-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="fc110-143">Она состоит из одной частной DNS-записи, указывающей на IP-адрес 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="fc110-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="fc110-144">Служба SIP и протокол TCP задаются как часть имени набора записей, а не как часть данных записи.</span><span class="sxs-lookup"><span data-stu-id="fc110-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="fc110-145">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fc110-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="fc110-146">Пример 7: создание набора записей типа TXT</span><span class="sxs-lookup"><span data-stu-id="fc110-146">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="fc110-147">Эта команда создает набор записей с именем в частной зоне myzone.com.</span><span class="sxs-lookup"><span data-stu-id="fc110-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="fc110-148">Набор записей имеет тип TXT и имеет значение TTL, равное 1 часу (3600 секунд).</span><span class="sxs-lookup"><span data-stu-id="fc110-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="fc110-149">Она состоит из одной частной DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="fc110-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="fc110-150">Чтобы создать набор записей с использованием одной строки pn_PowerShell_short или создать набор записей с несколькими записями, ознакомьтесь с примером 1.</span><span class="sxs-lookup"><span data-stu-id="fc110-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="fc110-151">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc110-151">PARAMETERS</span></span>

### <span data-ttu-id="fc110-152">-CNAME</span><span class="sxs-lookup"><span data-stu-id="fc110-152">-Cname</span></span>
<span data-ttu-id="fc110-153">Каноническое имя для добавляемой записи CNAME.</span><span class="sxs-lookup"><span data-stu-id="fc110-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="fc110-154">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="fc110-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="fc110-155">Точка не должна быть завершающей</span><span class="sxs-lookup"><span data-stu-id="fc110-155">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="fc110-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc110-156">-DefaultProfile</span></span>
<span data-ttu-id="fc110-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc110-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc110-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="fc110-158">-Exchange</span></span>
<span data-ttu-id="fc110-159">Узел почтового обмена для добавляемой записи MX.</span><span class="sxs-lookup"><span data-stu-id="fc110-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="fc110-160">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="fc110-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="fc110-161">Точка не должна быть завершающей</span><span class="sxs-lookup"><span data-stu-id="fc110-161">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="fc110-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="fc110-162">-Ipv4Address</span></span>
<span data-ttu-id="fc110-163">IPv4-адрес для записи A, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="fc110-163">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="fc110-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="fc110-164">-Ipv6Address</span></span>
<span data-ttu-id="fc110-165">Адрес IPv6 добавляемой записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="fc110-165">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="fc110-166">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="fc110-166">-Port</span></span>
<span data-ttu-id="fc110-167">Номер порта для добавляемой записи SRV.</span><span class="sxs-lookup"><span data-stu-id="fc110-167">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="fc110-168">-Предпочтения</span><span class="sxs-lookup"><span data-stu-id="fc110-168">-Preference</span></span>
<span data-ttu-id="fc110-169">Значение предпочтения для добавляемой записи MX.</span><span class="sxs-lookup"><span data-stu-id="fc110-169">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="fc110-170">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="fc110-170">-Priority</span></span>
<span data-ttu-id="fc110-171">Значение приоритета SRV-записи, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="fc110-171">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="fc110-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="fc110-172">-Ptrdname</span></span>
<span data-ttu-id="fc110-173">Целевой узел для добавляемой записи PTR.</span><span class="sxs-lookup"><span data-stu-id="fc110-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="fc110-174">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="fc110-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="fc110-175">Точка не должна быть завершающей</span><span class="sxs-lookup"><span data-stu-id="fc110-175">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="fc110-176">-Target</span><span class="sxs-lookup"><span data-stu-id="fc110-176">-Target</span></span>
<span data-ttu-id="fc110-177">Целевой узел для добавляемой записи SRV.</span><span class="sxs-lookup"><span data-stu-id="fc110-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="fc110-178">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="fc110-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="fc110-179">Точка не должна быть завершающей</span><span class="sxs-lookup"><span data-stu-id="fc110-179">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="fc110-180">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="fc110-180">-Value</span></span>
<span data-ttu-id="fc110-181">Текстовое значение добавляемой записи TXT.</span><span class="sxs-lookup"><span data-stu-id="fc110-181">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="fc110-182">-Weight</span><span class="sxs-lookup"><span data-stu-id="fc110-182">-Weight</span></span>
<span data-ttu-id="fc110-183">Значение веса для добавляемой записи SRV.</span><span class="sxs-lookup"><span data-stu-id="fc110-183">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="fc110-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc110-184">CommonParameters</span></span>
<span data-ttu-id="fc110-185">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc110-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc110-186">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc110-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc110-187">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc110-187">INPUTS</span></span>

### <span data-ttu-id="fc110-188">Ничего</span><span class="sxs-lookup"><span data-stu-id="fc110-188">None</span></span>

## <span data-ttu-id="fc110-189">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc110-189">OUTPUTS</span></span>

### <span data-ttu-id="fc110-190">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fc110-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="fc110-191">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc110-191">NOTES</span></span>

## <span data-ttu-id="fc110-192">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc110-192">RELATED LINKS</span></span>
