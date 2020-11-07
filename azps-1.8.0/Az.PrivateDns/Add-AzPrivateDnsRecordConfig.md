---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: af3e2e3494aa7f7f98856db3709d4716f5b04e44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729790"
---
# <span data-ttu-id="80906-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="80906-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="80906-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80906-102">SYNOPSIS</span></span>
<span data-ttu-id="80906-103">Добавляет частную запись DNS в локальный объект локального множества записей.</span><span class="sxs-lookup"><span data-stu-id="80906-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="80906-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80906-104">SYNTAX</span></span>

### <span data-ttu-id="80906-105">A (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80906-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80906-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="80906-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80906-107">МХ</span><span class="sxs-lookup"><span data-stu-id="80906-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80906-108">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="80906-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80906-109">ТХТ</span><span class="sxs-lookup"><span data-stu-id="80906-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80906-110">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="80906-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80906-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="80906-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80906-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80906-112">DESCRIPTION</span></span>
<span data-ttu-id="80906-113">Командлет Add-AzPrivateDnsRecordConfig добавляет частную запись DNS (Domain Name System) в объект набора записей.</span><span class="sxs-lookup"><span data-stu-id="80906-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="80906-114">Объект RecordSet — это автономный объект, и изменения в нем не изменяют частные ответы DNS, пока не будет запущен командлет Set-AzPrivateDnsRecordSet, чтобы сохранить изменения в частной службе DNS Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="80906-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="80906-115">Записи SOA создаются при создании частной зоны DNS и удаляются при удалении частной зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="80906-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="80906-116">Вы не можете добавлять и удалять записи SOA, но можете редактировать их.</span><span class="sxs-lookup"><span data-stu-id="80906-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="80906-117">Вы можете передать объект набора записей в этот командлет как параметр или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="80906-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="80906-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80906-118">EXAMPLES</span></span>

### <span data-ttu-id="80906-119">Пример 1: Добавление записи A в набор записей</span><span class="sxs-lookup"><span data-stu-id="80906-119">Example 1: Add an A record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="80906-120">В этом примере к существующему набору записей добавляется запись A.</span><span class="sxs-lookup"><span data-stu-id="80906-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="80906-121">Пример 2: Добавление записи AAAA в набор записей</span><span class="sxs-lookup"><span data-stu-id="80906-121">Example 2: Add an AAAA record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="80906-122">В этом примере добавляется запись AAAA в существующий наборы записей.</span><span class="sxs-lookup"><span data-stu-id="80906-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="80906-123">Пример 3: Добавление записи CNAME в набор записей</span><span class="sxs-lookup"><span data-stu-id="80906-123">Example 3: Add a CNAME record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="80906-124">В этом примере добавляется запись CNAME к существующему набору записей.</span><span class="sxs-lookup"><span data-stu-id="80906-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="80906-125">Пример 4: Добавление записи MX в набор записей</span><span class="sxs-lookup"><span data-stu-id="80906-125">Example 4: Add a MX record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name @ -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="80906-126">В этом примере добавляется запись MX в существующий набор записей.</span><span class="sxs-lookup"><span data-stu-id="80906-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="80906-127">Пример 5: Добавление записи PTR в набор записей</span><span class="sxs-lookup"><span data-stu-id="80906-127">Example 5: Add a PTR record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="80906-128">В этом примере к существующему набору записей добавляется запись PTR.</span><span class="sxs-lookup"><span data-stu-id="80906-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="80906-129">Пример 6: Добавление записи SRV в набор записей</span><span class="sxs-lookup"><span data-stu-id="80906-129">Example 6: Add a SRV record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup-ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="80906-130">В этом примере добавляется запись SRV к существующему набору записей.</span><span class="sxs-lookup"><span data-stu-id="80906-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="80906-131">Пример 7: Добавление записи TXT в набор записей</span><span class="sxs-lookup"><span data-stu-id="80906-131">Example 7: Add a TXT record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Value "This is a TXT Record" | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="80906-132">В этом примере к существующему набору записей добавляется запись TXT.</span><span class="sxs-lookup"><span data-stu-id="80906-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="80906-133">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80906-133">PARAMETERS</span></span>

### <span data-ttu-id="80906-134">-CNAME</span><span class="sxs-lookup"><span data-stu-id="80906-134">-Cname</span></span>
<span data-ttu-id="80906-135">Каноническое имя для добавляемой записи CNAME.</span><span class="sxs-lookup"><span data-stu-id="80906-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="80906-136">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="80906-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="80906-137">Точка не должна быть завершающей</span><span class="sxs-lookup"><span data-stu-id="80906-137">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="80906-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80906-138">-DefaultProfile</span></span>
<span data-ttu-id="80906-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80906-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80906-140">-Exchange</span><span class="sxs-lookup"><span data-stu-id="80906-140">-Exchange</span></span>
<span data-ttu-id="80906-141">Узел почтового обмена для добавляемой записи MX.</span><span class="sxs-lookup"><span data-stu-id="80906-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="80906-142">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="80906-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="80906-143">Точка не должна быть завершающей</span><span class="sxs-lookup"><span data-stu-id="80906-143">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="80906-144">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="80906-144">-Ipv4Address</span></span>
<span data-ttu-id="80906-145">IPv4-адрес для записи A, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="80906-145">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="80906-146">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="80906-146">-Ipv6Address</span></span>
<span data-ttu-id="80906-147">Адрес IPv6 добавляемой записи AAAA.</span><span class="sxs-lookup"><span data-stu-id="80906-147">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="80906-148">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="80906-148">-Port</span></span>
<span data-ttu-id="80906-149">Номер порта для добавляемой записи SRV.</span><span class="sxs-lookup"><span data-stu-id="80906-149">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="80906-150">-Предпочтения</span><span class="sxs-lookup"><span data-stu-id="80906-150">-Preference</span></span>
<span data-ttu-id="80906-151">Значение предпочтения для добавляемой записи MX.</span><span class="sxs-lookup"><span data-stu-id="80906-151">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="80906-152">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="80906-152">-Priority</span></span>
<span data-ttu-id="80906-153">Значение приоритета SRV-записи, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="80906-153">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="80906-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="80906-154">-Ptrdname</span></span>
<span data-ttu-id="80906-155">Целевой узел для добавляемой записи PTR.</span><span class="sxs-lookup"><span data-stu-id="80906-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="80906-156">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="80906-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="80906-157">Точка не должна быть завершающей</span><span class="sxs-lookup"><span data-stu-id="80906-157">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="80906-158">-Набор записей</span><span class="sxs-lookup"><span data-stu-id="80906-158">-RecordSet</span></span>
<span data-ttu-id="80906-159">Настройка записи, в которую нужно добавить запись.</span><span class="sxs-lookup"><span data-stu-id="80906-159">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80906-160">-Target</span><span class="sxs-lookup"><span data-stu-id="80906-160">-Target</span></span>
<span data-ttu-id="80906-161">Целевой узел для добавляемой записи SRV.</span><span class="sxs-lookup"><span data-stu-id="80906-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="80906-162">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="80906-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="80906-163">Точка не должна быть завершающей</span><span class="sxs-lookup"><span data-stu-id="80906-163">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="80906-164">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="80906-164">-Value</span></span>
<span data-ttu-id="80906-165">Текстовое значение добавляемой записи TXT.</span><span class="sxs-lookup"><span data-stu-id="80906-165">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="80906-166">-Weight</span><span class="sxs-lookup"><span data-stu-id="80906-166">-Weight</span></span>
<span data-ttu-id="80906-167">Значение веса для добавляемой записи SRV.</span><span class="sxs-lookup"><span data-stu-id="80906-167">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="80906-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80906-168">CommonParameters</span></span>
<span data-ttu-id="80906-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80906-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80906-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80906-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80906-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80906-171">INPUTS</span></span>

### <span data-ttu-id="80906-172">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="80906-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="80906-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80906-173">OUTPUTS</span></span>

### <span data-ttu-id="80906-174">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="80906-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="80906-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="80906-175">NOTES</span></span>

## <span data-ttu-id="80906-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80906-176">RELATED LINKS</span></span>
