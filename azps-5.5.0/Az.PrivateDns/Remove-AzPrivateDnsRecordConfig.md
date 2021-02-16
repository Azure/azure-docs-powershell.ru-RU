---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 1e3362850880f02c648fb3318db226515fc95eef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225449"
---
# <span data-ttu-id="52e2f-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="52e2f-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="52e2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="52e2f-103">Удаляет личную запись DNS из локального объекта набора записей.</span><span class="sxs-lookup"><span data-stu-id="52e2f-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="52e2f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="52e2f-104">SYNTAX</span></span>

### <span data-ttu-id="52e2f-105">A (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52e2f-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52e2f-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="52e2f-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52e2f-107">MX</span><span class="sxs-lookup"><span data-stu-id="52e2f-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52e2f-108">PTR</span><span class="sxs-lookup"><span data-stu-id="52e2f-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52e2f-109">TXT</span><span class="sxs-lookup"><span data-stu-id="52e2f-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52e2f-110">SRV</span><span class="sxs-lookup"><span data-stu-id="52e2f-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52e2f-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="52e2f-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52e2f-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52e2f-112">DESCRIPTION</span></span>
<span data-ttu-id="52e2f-113">С Remove-AzPrivateDnsRecordConfig- и DNS-записи из набора записей удаляются.</span><span class="sxs-lookup"><span data-stu-id="52e2f-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="52e2f-114">Объект RecordSet является автономным объектом, и изменения в нем не изменяют ответы на частные DNS до тех пор, пока вы не запустите Set-AzPrivateDnsRecordSet, чтобы сохранить изменение в частной службе DNS Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="52e2f-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="52e2f-115">Чтобы удалить запись, все поля для этого типа записи должны в точности соответствовать.</span><span class="sxs-lookup"><span data-stu-id="52e2f-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="52e2f-116">Записи SOA добавлять и удалять нельзя.</span><span class="sxs-lookup"><span data-stu-id="52e2f-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="52e2f-117">Записи SOA создаются автоматически при создания частной зоны DNS и автоматическом удалении при ее удалении.</span><span class="sxs-lookup"><span data-stu-id="52e2f-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="52e2f-118">Объект RecordSet можно передать этому cmdlet в качестве параметра или с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="52e2f-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="52e2f-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="52e2f-119">EXAMPLES</span></span>

### <span data-ttu-id="52e2f-120">Пример 1. Удаление записи A из набора записей</span><span class="sxs-lookup"><span data-stu-id="52e2f-120">Example 1: Remove an A record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="52e2f-121">В этом примере запись A удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="52e2f-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="52e2f-122">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="52e2f-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="52e2f-123">Чтобы полностью удалить набор записей, см. видео Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="52e2f-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="52e2f-124">Пример 2. Удаление записи AAAA из набора записей</span><span class="sxs-lookup"><span data-stu-id="52e2f-124">Example 2: Remove an AAAA record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="52e2f-125">В этом примере запись AAAA удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="52e2f-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="52e2f-126">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="52e2f-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="52e2f-127">Чтобы полностью удалить набор записей, см. видео Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="52e2f-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="52e2f-128">Пример 3. Удаление записи CNAME из набора записей</span><span class="sxs-lookup"><span data-stu-id="52e2f-128">Example 3: Remove a CNAME record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="52e2f-129">В этом примере запись CNAME удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="52e2f-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="52e2f-130">Так как набор записей CNAME может содержать не более одной записи, результатом является пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="52e2f-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="52e2f-131">Пример 4. Удаление записи MX из набора записей</span><span class="sxs-lookup"><span data-stu-id="52e2f-131">Example 4: Remove a MX record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="52e2f-132">В этом примере запись MX удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="52e2f-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="52e2f-133">Имя записи "@" означает набор записей на апексе зоны.</span><span class="sxs-lookup"><span data-stu-id="52e2f-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="52e2f-134">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="52e2f-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="52e2f-135">Чтобы полностью удалить набор записей, см. видео Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="52e2f-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="52e2f-136">Пример 5. Удаление записи PTR из набора записей</span><span class="sxs-lookup"><span data-stu-id="52e2f-136">Example 5: Remove a PTR record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="52e2f-137">В этом примере запись PTR удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="52e2f-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="52e2f-138">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="52e2f-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="52e2f-139">Чтобы полностью удалить набор записей, см. видео Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="52e2f-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="52e2f-140">Пример 6. Удаление записи SRV из набора записей</span><span class="sxs-lookup"><span data-stu-id="52e2f-140">Example 6: Remove a SRV record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="52e2f-141">В этом примере запись SRV удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="52e2f-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="52e2f-142">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="52e2f-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="52e2f-143">Чтобы полностью удалить набор записей, см. видео Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="52e2f-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="52e2f-144">Пример 7. Удаление записи TXT из набора записей</span><span class="sxs-lookup"><span data-stu-id="52e2f-144">Example 7: Remove a TXT record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="52e2f-145">В этом примере запись TXT удаляется из существующего набора.</span><span class="sxs-lookup"><span data-stu-id="52e2f-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="52e2f-146">Если это единственная запись в наборе записей, результатом будет пустой набор записей.</span><span class="sxs-lookup"><span data-stu-id="52e2f-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="52e2f-147">Чтобы полностью удалить набор записей, см. видео Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="52e2f-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="52e2f-148">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52e2f-148">PARAMETERS</span></span>

### <span data-ttu-id="52e2f-149">-Cname</span><span class="sxs-lookup"><span data-stu-id="52e2f-149">-Cname</span></span>
<span data-ttu-id="52e2f-150">Каноническое имя записи CNAME, удаляемой.</span><span class="sxs-lookup"><span data-stu-id="52e2f-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="52e2f-151">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="52e2f-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="52e2f-152">Не должно быть точки, заканчиваемой точкой</span><span class="sxs-lookup"><span data-stu-id="52e2f-152">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="52e2f-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52e2f-153">-DefaultProfile</span></span>
<span data-ttu-id="52e2f-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52e2f-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52e2f-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="52e2f-155">-Exchange</span></span>
<span data-ttu-id="52e2f-156">Сервер обмена электронной почтой записи MX, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="52e2f-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="52e2f-157">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="52e2f-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="52e2f-158">Не должно быть точки, заканчиваемой точкой</span><span class="sxs-lookup"><span data-stu-id="52e2f-158">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="52e2f-159">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="52e2f-159">-Ipv4Address</span></span>
<span data-ttu-id="52e2f-160">IPv4-адрес записи A, удаляемой.</span><span class="sxs-lookup"><span data-stu-id="52e2f-160">The IPv4 address of the A record to remove.</span></span>

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

### <span data-ttu-id="52e2f-161">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="52e2f-161">-Ipv6Address</span></span>
<span data-ttu-id="52e2f-162">IPv6-адрес записи AAAA, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="52e2f-162">The IPv6 address of the AAAA record to remove.</span></span>

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

### <span data-ttu-id="52e2f-163">-Port</span><span class="sxs-lookup"><span data-stu-id="52e2f-163">-Port</span></span>
<span data-ttu-id="52e2f-164">Номер порта записи SRV, удаляемой.</span><span class="sxs-lookup"><span data-stu-id="52e2f-164">The port number of the SRV record to remove.</span></span>

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

### <span data-ttu-id="52e2f-165">-Preference</span><span class="sxs-lookup"><span data-stu-id="52e2f-165">-Preference</span></span>
<span data-ttu-id="52e2f-166">Значение параметра записи MX, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="52e2f-166">The preference value of the MX record to remove.</span></span>

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

### <span data-ttu-id="52e2f-167">-Priority</span><span class="sxs-lookup"><span data-stu-id="52e2f-167">-Priority</span></span>
<span data-ttu-id="52e2f-168">Значение приоритета записи SRV, которая нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="52e2f-168">The priority value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="52e2f-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="52e2f-169">-Ptrdname</span></span>
<span data-ttu-id="52e2f-170">Целевой хост записи PTR, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="52e2f-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="52e2f-171">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="52e2f-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="52e2f-172">Не должно быть точки, заканчиваемой точкой</span><span class="sxs-lookup"><span data-stu-id="52e2f-172">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="52e2f-173">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="52e2f-173">-RecordSet</span></span>
<span data-ttu-id="52e2f-174">Набор записей, из которого нужно удалить запись.</span><span class="sxs-lookup"><span data-stu-id="52e2f-174">The record set from which to remove the record.</span></span>

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

### <span data-ttu-id="52e2f-175">-Target</span><span class="sxs-lookup"><span data-stu-id="52e2f-175">-Target</span></span>
<span data-ttu-id="52e2f-176">Целевой хост записи SRV, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="52e2f-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="52e2f-177">Не должно быть относительно имени зоны.</span><span class="sxs-lookup"><span data-stu-id="52e2f-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="52e2f-178">Не должно быть точки, заканчиваемой точкой</span><span class="sxs-lookup"><span data-stu-id="52e2f-178">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="52e2f-179">-Value</span><span class="sxs-lookup"><span data-stu-id="52e2f-179">-Value</span></span>
<span data-ttu-id="52e2f-180">Текстовое значение записи TXT, которая нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="52e2f-180">The text value of the TXT record to remove.</span></span>

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

### <span data-ttu-id="52e2f-181">-Weight</span><span class="sxs-lookup"><span data-stu-id="52e2f-181">-Weight</span></span>
<span data-ttu-id="52e2f-182">Значение веса записи SRV, которая нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="52e2f-182">The weight value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="52e2f-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e2f-183">CommonParameters</span></span>
<span data-ttu-id="52e2f-184">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52e2f-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e2f-185">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52e2f-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e2f-186">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52e2f-186">INPUTS</span></span>

### <span data-ttu-id="52e2f-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="52e2f-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="52e2f-188">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="52e2f-188">OUTPUTS</span></span>

### <span data-ttu-id="52e2f-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="52e2f-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="52e2f-190">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="52e2f-190">NOTES</span></span>

## <span data-ttu-id="52e2f-191">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52e2f-191">RELATED LINKS</span></span>
