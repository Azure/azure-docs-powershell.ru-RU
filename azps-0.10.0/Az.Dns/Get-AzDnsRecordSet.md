---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 7e1ea1213759e9c4edf9524a36637aff1ef1c12b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911243"
---
# <span data-ttu-id="7aa1b-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7aa1b-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="7aa1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7aa1b-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa1b-103">Получает набор записей DNS.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="7aa1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7aa1b-104">SYNTAX</span></span>

### <span data-ttu-id="7aa1b-105">»</span><span class="sxs-lookup"><span data-stu-id="7aa1b-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### <span data-ttu-id="7aa1b-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="7aa1b-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
```

## <span data-ttu-id="7aa1b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7aa1b-107">DESCRIPTION</span></span>
<span data-ttu-id="7aa1b-108">Командлет **Get-AzDnsRecordSet** получает набор записей DNS (Domain Name System) с указанными именем и типом в указанной зоне.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="7aa1b-109">Если не указать параметры *Name* или *RecordType* , этот командлет возвращает все наборы записей указанного типа в зоне.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="7aa1b-110">Если указать параметр *RecordType* , но не параметр *Name* , этот командлет возвращает все наборы записей с указанным типом записи.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="7aa1b-111">Вы можете использовать оператор конвейера для передачи объекта **dnsZone** в этот командлет или передавать объект **dnsZone** в качестве параметра *зоны* или можно указать зону и группу ресурсов по имени.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="7aa1b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7aa1b-112">EXAMPLES</span></span>

### <span data-ttu-id="7aa1b-113">Пример 1: получение наборов записей с указанным именем и типом</span><span class="sxs-lookup"><span data-stu-id="7aa1b-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="7aa1b-114">Эта команда получает набор записей с именем www в заданной группе ресурсов и зоне, а затем сохраняет его в переменной $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="7aa1b-115">Так как указаны параметры *Name* и *RecordType* , возвращается только один объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="7aa1b-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="7aa1b-116">Пример 2: получение наборов записей указанного типа</span><span class="sxs-lookup"><span data-stu-id="7aa1b-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="7aa1b-117">Эта команда получает массив всех наборов записей типа A в зоне с именем myzone.com в группе ресурсов с именем MyResourceGroup и сохраняет их в переменной $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="7aa1b-118">Пример 3: получение всех наборов записей в зоне</span><span class="sxs-lookup"><span data-stu-id="7aa1b-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="7aa1b-119">Эта команда получает массив всех наборов записей в зоне с именем myzone.com в группе ресурсов с именем MyResourceGroup, а затем сохраняет их в переменной $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="7aa1b-120">Пример 4: получение всех наборов записей в зоне с помощью объекта DnsZone</span><span class="sxs-lookup"><span data-stu-id="7aa1b-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="7aa1b-121">Этот пример эквивалентен примеру 3 выше.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="7aa1b-122">На этот раз зона задается с помощью объекта Zone.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="7aa1b-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7aa1b-123">PARAMETERS</span></span>

### <span data-ttu-id="7aa1b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7aa1b-124">-Name</span></span>
<span data-ttu-id="7aa1b-125">Указывает имя **набора записей** для получения.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-125">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="7aa1b-126">Если параметр *Name* не указан, возвращаются все наборы записей указанного типа.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-126">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa1b-127">-RecordType</span><span class="sxs-lookup"><span data-stu-id="7aa1b-127">-RecordType</span></span>
<span data-ttu-id="7aa1b-128">Указывает тип DNS-записи, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-128">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="7aa1b-129">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="7aa1b-129">Valid values are:</span></span> 

- <span data-ttu-id="7aa1b-130">Помощью</span><span class="sxs-lookup"><span data-stu-id="7aa1b-130">A</span></span>
- <span data-ttu-id="7aa1b-131">AAAA</span><span class="sxs-lookup"><span data-stu-id="7aa1b-131">AAAA</span></span>
- <span data-ttu-id="7aa1b-132">CNAME</span><span class="sxs-lookup"><span data-stu-id="7aa1b-132">CNAME</span></span>
- <span data-ttu-id="7aa1b-133">МХ</span><span class="sxs-lookup"><span data-stu-id="7aa1b-133">MX</span></span>
- <span data-ttu-id="7aa1b-134">СЛУЖБУ</span><span class="sxs-lookup"><span data-stu-id="7aa1b-134">NS</span></span>
- <span data-ttu-id="7aa1b-135">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="7aa1b-135">PTR</span></span>
- <span data-ttu-id="7aa1b-136">ЗОНЫ</span><span class="sxs-lookup"><span data-stu-id="7aa1b-136">SOA</span></span>
- <span data-ttu-id="7aa1b-137">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="7aa1b-137">SRV</span></span>
- <span data-ttu-id="7aa1b-138">ТХТ</span><span class="sxs-lookup"><span data-stu-id="7aa1b-138">TXT</span></span>

<span data-ttu-id="7aa1b-139">Если параметр *RecordType* не указан, необходимо также опустить параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="7aa1b-139">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="7aa1b-140">Затем этот командлет возвращает все наборы записей в зоне (для всех имен и типов).</span><span class="sxs-lookup"><span data-stu-id="7aa1b-140">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa1b-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aa1b-141">-ResourceGroupName</span></span>
<span data-ttu-id="7aa1b-142">Указывает группу ресурсов, которая содержит зону DNS.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-142">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="7aa1b-143">Имя зоны также должно быть указано с помощью параметра *zonename* .</span><span class="sxs-lookup"><span data-stu-id="7aa1b-143">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="7aa1b-144">Кроме того, вы можете указать зону и группу ресурсов, передав объект **dnsZone** с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="7aa1b-144">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa1b-145">-Zone</span><span class="sxs-lookup"><span data-stu-id="7aa1b-145">-Zone</span></span>
<span data-ttu-id="7aa1b-146">Указывает зону DNS, которая содержит набор записей, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-146">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="7aa1b-147">Кроме того, вы можете указать зону с помощью параметров *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="7aa1b-147">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa1b-148">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="7aa1b-148">-ZoneName</span></span>
<span data-ttu-id="7aa1b-149">Указывает имя зоны DNS, которая содержит набор записей, для которого требуется получить доступ.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-149">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="7aa1b-150">Группа ресурсов, содержащая зону, также должна быть указана с помощью параметра *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="7aa1b-150">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="7aa1b-151">Кроме того, вы можете указать зону и группу ресурсов, передав объект зоны DNS с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="7aa1b-151">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa1b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa1b-152">CommonParameters</span></span>
<span data-ttu-id="7aa1b-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa1b-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aa1b-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa1b-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7aa1b-155">INPUTS</span></span>

### <span data-ttu-id="7aa1b-156">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="7aa1b-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="7aa1b-157">Вы можете передать на этот командлет объект **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="7aa1b-157">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="7aa1b-158">Объект **dnsZone** представляет зону, в которой следует искать объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="7aa1b-158">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="7aa1b-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7aa1b-159">OUTPUTS</span></span>

### <span data-ttu-id="7aa1b-160">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7aa1b-160">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="7aa1b-161">Этот командлет возвращает один или несколько объектов, представляющих найденные наборы записей.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-161">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="7aa1b-162">Если указаны параметры *Name* и *RecordType* , возвращается не более одного **набора записей** , в противном случае несколько объектов **набора записей** возвращаются в виде массива.</span><span class="sxs-lookup"><span data-stu-id="7aa1b-162">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="7aa1b-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="7aa1b-163">NOTES</span></span>

## <span data-ttu-id="7aa1b-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7aa1b-164">RELATED LINKS</span></span>

[<span data-ttu-id="7aa1b-165">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7aa1b-165">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="7aa1b-166">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7aa1b-166">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="7aa1b-167">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="7aa1b-167">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


