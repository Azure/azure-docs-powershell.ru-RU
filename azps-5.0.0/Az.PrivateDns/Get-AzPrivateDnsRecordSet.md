---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: ade9d95b6388a667f55df24db107a2326fa001ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248057"
---
# <span data-ttu-id="f3a61-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f3a61-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f3a61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3a61-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a61-103">Получает набор записей из частной зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="f3a61-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="f3a61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3a61-104">SYNTAX</span></span>

### <span data-ttu-id="f3a61-105">FieldsWithNoName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f3a61-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3a61-106">»</span><span class="sxs-lookup"><span data-stu-id="f3a61-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3a61-107">DataObject</span><span class="sxs-lookup"><span data-stu-id="f3a61-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3a61-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="f3a61-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3a61-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3a61-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3a61-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="f3a61-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3a61-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3a61-111">DESCRIPTION</span></span>
<span data-ttu-id="f3a61-112">Командлет Get-AzPrivateDnsRecordSet получает набор записей частной системы доменных имен (DNS) с указанными именем и типом в указанной частной зоне.</span><span class="sxs-lookup"><span data-stu-id="f3a61-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="f3a61-113">Если не указать параметры Name или RecordType, этот командлет возвращает все наборы записей указанного типа в частной зоне.</span><span class="sxs-lookup"><span data-stu-id="f3a61-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="f3a61-114">Если указать параметр RecordType, но не параметр name, этот командлет возвращает все наборы записей с указанным типом записи.</span><span class="sxs-lookup"><span data-stu-id="f3a61-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="f3a61-115">Вы можете использовать оператор конвейера для передачи объекта PSPrivateDnsZone в этот командлет или передавать объект PSPrivateDnsZone в качестве параметра зоны или можно указать зону и группу ресурсов по имени.</span><span class="sxs-lookup"><span data-stu-id="f3a61-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="f3a61-116">Вы также можете указать частную зону, используя идентификатор ресурса частной зоны.</span><span class="sxs-lookup"><span data-stu-id="f3a61-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="f3a61-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3a61-117">EXAMPLES</span></span>

### <span data-ttu-id="f3a61-118">Пример 1: получение наборов записей с указанным именем и типом</span><span class="sxs-lookup"><span data-stu-id="f3a61-118">Example 1: Get record sets with a specified name and type</span></span>
```powershell
PS C:\>$RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
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

<span data-ttu-id="f3a61-119">Эта команда возвращает набор записей с именем "www" в указанной группе ресурсов и частной зоне, а затем сохраняет его в переменной $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="f3a61-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="f3a61-120">Так как указаны параметры Name и RecordType, возвращается только один объект RecordSet.</span><span class="sxs-lookup"><span data-stu-id="f3a61-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="f3a61-121">Пример 2: получение наборов записей указанного типа</span><span class="sxs-lookup"><span data-stu-id="f3a61-121">Example 2: Get record sets of a specified type</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www2
Name              : www2
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {2.3.4.5}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f3a61-122">Эта команда получает массив всех наборов записей типа Record в частной зоне с именем myzone.com в группе ресурсов с именем MyResourceGroup и сохраняет их в переменной $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="f3a61-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="f3a61-123">Пример 3: получение всех наборов записей в частной зоне</span><span class="sxs-lookup"><span data-stu-id="f3a61-123">Example 3: Get all record sets in a private zone</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f3a61-124">Эта команда получает массив всех наборов записей в частной зоне с именем myzone.com в группе ресурсов с именем MyResourceGroup и сохраняет их в переменной $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="f3a61-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="f3a61-125">Пример 4: получение всех наборов записей в частной зоне с помощью объекта PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f3a61-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
```powershell
PS C:\> $Zone = Get-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzPrivateDnsRecordSet -Zone $Zone

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f3a61-126">Этот пример эквивалентен примеру 3 выше.</span><span class="sxs-lookup"><span data-stu-id="f3a61-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="f3a61-127">На этот раз закрытая зона задается с помощью объекта частной зоны.</span><span class="sxs-lookup"><span data-stu-id="f3a61-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="f3a61-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3a61-128">PARAMETERS</span></span>

### <span data-ttu-id="f3a61-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a61-129">-DefaultProfile</span></span>
<span data-ttu-id="f3a61-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3a61-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3a61-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3a61-131">-Name</span></span>
<span data-ttu-id="f3a61-132">Имена записей в наборе записей (относительно имени зоны и без точки).</span><span class="sxs-lookup"><span data-stu-id="f3a61-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Object, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a61-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f3a61-133">-ParentResourceId</span></span>
<span data-ttu-id="f3a61-134">Частный секретный ИД зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="f3a61-134">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId, ResourceIdWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a61-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="f3a61-135">-RecordType</span></span>
<span data-ttu-id="f3a61-136">Тип DNS-записей в этом наборе записей.</span><span class="sxs-lookup"><span data-stu-id="f3a61-136">The type of DNS records in this record set.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: FieldsWithNoName, ObjectWithNoName, ResourceIdWithNoName
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: Fields, Object, ResourceId
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a61-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3a61-137">-ResourceGroupName</span></span>
<span data-ttu-id="f3a61-138">Группа ресурсов, к которой принадлежит зона.</span><span class="sxs-lookup"><span data-stu-id="f3a61-138">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a61-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="f3a61-139">-Zone</span></span>
<span data-ttu-id="f3a61-140">Объект DnsZone, представляющий зону, в которой нужно создать набор записей.</span><span class="sxs-lookup"><span data-stu-id="f3a61-140">The DnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object, ObjectWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a61-141">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="f3a61-141">-ZoneName</span></span>
<span data-ttu-id="f3a61-142">Зона, в которой нужно создать набор записей (без точки завершения).</span><span class="sxs-lookup"><span data-stu-id="f3a61-142">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a61-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a61-143">CommonParameters</span></span>
<span data-ttu-id="f3a61-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3a61-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a61-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3a61-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a61-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3a61-146">INPUTS</span></span>

### <span data-ttu-id="f3a61-147">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f3a61-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="f3a61-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f3a61-148">System.String</span></span>

## <span data-ttu-id="f3a61-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3a61-149">OUTPUTS</span></span>

### <span data-ttu-id="f3a61-150">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f3a61-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f3a61-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3a61-151">NOTES</span></span>

## <span data-ttu-id="f3a61-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3a61-152">RELATED LINKS</span></span>
