---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: c45fc33ec45ce0843fe7ef832a70ec622b14af8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566818"
---
# <span data-ttu-id="77ec2-101">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="77ec2-101">Get-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="77ec2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="77ec2-103">Получает набор записей DNS.</span><span class="sxs-lookup"><span data-stu-id="77ec2-103">Gets a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77ec2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77ec2-104">SYNTAX</span></span>

### <span data-ttu-id="77ec2-105">»</span><span class="sxs-lookup"><span data-stu-id="77ec2-105">Fields</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77ec2-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="77ec2-106">Object</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77ec2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77ec2-107">DESCRIPTION</span></span>
<span data-ttu-id="77ec2-108">Командлет **Get-AzureRmDnsRecordSet** получает набор записей DNS (Domain Name System) с указанными именем и типом в указанной зоне.</span><span class="sxs-lookup"><span data-stu-id="77ec2-108">The **Get-AzureRmDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="77ec2-109">Если не указать параметры *Name* или *RecordType* , этот командлет возвращает все наборы записей указанного типа в зоне.</span><span class="sxs-lookup"><span data-stu-id="77ec2-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="77ec2-110">Если указать параметр *RecordType* , но не параметр *Name* , этот командлет возвращает все наборы записей с указанным типом записи.</span><span class="sxs-lookup"><span data-stu-id="77ec2-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="77ec2-111">Вы можете использовать оператор конвейера для передачи объекта **dnsZone** в этот командлет или передавать объект **dnsZone** в качестве параметра *зоны* или можно указать зону и группу ресурсов по имени.</span><span class="sxs-lookup"><span data-stu-id="77ec2-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="77ec2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77ec2-112">EXAMPLES</span></span>

### <span data-ttu-id="77ec2-113">Пример 1: получение наборов записей с указанным именем и типом</span><span class="sxs-lookup"><span data-stu-id="77ec2-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="77ec2-114">Эта команда получает набор записей с именем www в заданной группе ресурсов и зоне, а затем сохраняет его в переменной $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="77ec2-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="77ec2-115">Так как указаны параметры *Name* и *RecordType* , возвращается только один объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="77ec2-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="77ec2-116">Пример 2: получение наборов записей указанного типа</span><span class="sxs-lookup"><span data-stu-id="77ec2-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="77ec2-117">Эта команда получает массив всех наборов записей типа A в зоне с именем myzone.com в группе ресурсов с именем MyResourceGroup и сохраняет их в переменной $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="77ec2-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="77ec2-118">Пример 3: получение всех наборов записей в зоне</span><span class="sxs-lookup"><span data-stu-id="77ec2-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="77ec2-119">Эта команда получает массив всех наборов записей в зоне с именем myzone.com в группе ресурсов с именем MyResourceGroup, а затем сохраняет их в переменной $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="77ec2-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="77ec2-120">Пример 4: получение всех наборов записей в зоне с помощью объекта DnsZone</span><span class="sxs-lookup"><span data-stu-id="77ec2-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

<span data-ttu-id="77ec2-121">Этот пример эквивалентен примеру 3 выше.</span><span class="sxs-lookup"><span data-stu-id="77ec2-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="77ec2-122">На этот раз зона задается с помощью объекта Zone.</span><span class="sxs-lookup"><span data-stu-id="77ec2-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="77ec2-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77ec2-123">PARAMETERS</span></span>

### <span data-ttu-id="77ec2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ec2-124">-DefaultProfile</span></span>
<span data-ttu-id="77ec2-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="77ec2-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77ec2-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="77ec2-126">-Name</span></span>
<span data-ttu-id="77ec2-127">Указывает имя **набора записей** для получения.</span><span class="sxs-lookup"><span data-stu-id="77ec2-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="77ec2-128">Если параметр *Name* не указан, возвращаются все наборы записей указанного типа.</span><span class="sxs-lookup"><span data-stu-id="77ec2-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77ec2-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="77ec2-129">-RecordType</span></span>
<span data-ttu-id="77ec2-130">Указывает тип DNS-записи, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="77ec2-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="77ec2-131">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="77ec2-131">Valid values are:</span></span> 
- <span data-ttu-id="77ec2-132">Помощью</span><span class="sxs-lookup"><span data-stu-id="77ec2-132">A</span></span>
- <span data-ttu-id="77ec2-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="77ec2-133">AAAA</span></span>
- <span data-ttu-id="77ec2-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="77ec2-134">CNAME</span></span>
- <span data-ttu-id="77ec2-135">МХ</span><span class="sxs-lookup"><span data-stu-id="77ec2-135">MX</span></span>
- <span data-ttu-id="77ec2-136">СЛУЖБУ</span><span class="sxs-lookup"><span data-stu-id="77ec2-136">NS</span></span>
- <span data-ttu-id="77ec2-137">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="77ec2-137">PTR</span></span>
- <span data-ttu-id="77ec2-138">ЗОНЫ</span><span class="sxs-lookup"><span data-stu-id="77ec2-138">SOA</span></span>
- <span data-ttu-id="77ec2-139">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="77ec2-139">SRV</span></span>
- <span data-ttu-id="77ec2-140">TXT если параметр *RecordType* не указан, необходимо также опустить параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="77ec2-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="77ec2-141">Затем этот командлет возвращает все наборы записей в зоне (для всех имен и типов).</span><span class="sxs-lookup"><span data-stu-id="77ec2-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77ec2-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77ec2-142">-ResourceGroupName</span></span>
<span data-ttu-id="77ec2-143">Указывает группу ресурсов, которая содержит зону DNS.</span><span class="sxs-lookup"><span data-stu-id="77ec2-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="77ec2-144">Имя зоны также должно быть указано с помощью параметра *zonename* .</span><span class="sxs-lookup"><span data-stu-id="77ec2-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="77ec2-145">Кроме того, вы можете указать зону и группу ресурсов, передав объект **dnsZone** с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="77ec2-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77ec2-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="77ec2-146">-Zone</span></span>
<span data-ttu-id="77ec2-147">Указывает зону DNS, которая содержит набор записей, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="77ec2-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="77ec2-148">Кроме того, вы можете указать зону с помощью параметров *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="77ec2-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77ec2-149">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="77ec2-149">-ZoneName</span></span>
<span data-ttu-id="77ec2-150">Указывает имя зоны DNS, которая содержит набор записей, для которого требуется получить доступ.</span><span class="sxs-lookup"><span data-stu-id="77ec2-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="77ec2-151">Группа ресурсов, содержащая зону, также должна быть указана с помощью параметра *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="77ec2-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="77ec2-152">Кроме того, вы можете указать зону и группу ресурсов, передав объект зоны DNS с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="77ec2-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77ec2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ec2-153">CommonParameters</span></span>
<span data-ttu-id="77ec2-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77ec2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ec2-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77ec2-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ec2-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77ec2-156">INPUTS</span></span>

### <span data-ttu-id="77ec2-157">System. String</span><span class="sxs-lookup"><span data-stu-id="77ec2-157">System.String</span></span>

### <span data-ttu-id="77ec2-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="77ec2-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="77ec2-159">Параметры: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77ec2-159">Parameters: Zone (ByValue)</span></span>

### <span data-ttu-id="77ec2-160">System. Nullable "1 [[Microsoft. Azure. Management. DNS. Models. RecordType, Microsoft. Azure. Management. DNS, Version = 2.1.0.0, культура = нейтральная, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="77ec2-160">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=2.1.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="77ec2-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77ec2-161">OUTPUTS</span></span>

### <span data-ttu-id="77ec2-162">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="77ec2-162">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="77ec2-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="77ec2-163">NOTES</span></span>

## <span data-ttu-id="77ec2-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77ec2-164">RELATED LINKS</span></span>

[<span data-ttu-id="77ec2-165">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="77ec2-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="77ec2-166">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="77ec2-166">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="77ec2-167">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="77ec2-167">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)


