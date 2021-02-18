---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230417"
---
# <span data-ttu-id="1bec8-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1bec8-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="1bec8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bec8-102">SYNOPSIS</span></span>
<span data-ttu-id="1bec8-103">Получает набор записей DNS.</span><span class="sxs-lookup"><span data-stu-id="1bec8-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="1bec8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1bec8-104">SYNTAX</span></span>

### <span data-ttu-id="1bec8-105">Поля</span><span class="sxs-lookup"><span data-stu-id="1bec8-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bec8-106">Объект</span><span class="sxs-lookup"><span data-stu-id="1bec8-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bec8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bec8-107">DESCRIPTION</span></span>
<span data-ttu-id="1bec8-108">С **помощью cmdlet Get-AzDnsRecordSet** можно получить набор записей службы доменных имен (DNS) с указанным именем и типом в указанной зоне.</span><span class="sxs-lookup"><span data-stu-id="1bec8-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="1bec8-109">Если *параметры Name* или *RecordType* не заданы, этот cmdlet возвращает все наборы записей указанного типа в зоне.</span><span class="sxs-lookup"><span data-stu-id="1bec8-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="1bec8-110">Если для *параметра RecordType* задан параметр RecordType, но не параметр *Name,* этот cmdlet возвращает все наборы записей указанного типа записи.</span><span class="sxs-lookup"><span data-stu-id="1bec8-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="1bec8-111">Вы можете использовать оператор конвейера, чтобы передать объект **DnsZone** этому cmdlet, или передать объект **DnsZone** в качестве параметра *зоны.* Кроме того, вы также можете указать зону и группу ресурсов по имени.</span><span class="sxs-lookup"><span data-stu-id="1bec8-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="1bec8-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1bec8-112">EXAMPLES</span></span>

### <span data-ttu-id="1bec8-113">Пример 1. Получить наборы записей с указанным именем и типом</span><span class="sxs-lookup"><span data-stu-id="1bec8-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="1bec8-114">Эта команда получает набор записей типа A "www" в указанной группе ресурсов и зоне, а затем сохраняет его в переменной $RecordSet ресурса.</span><span class="sxs-lookup"><span data-stu-id="1bec8-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="1bec8-115">Так как *параметры Name* *и RecordType* заданы, возвращается только один объект **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="1bec8-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="1bec8-116">Пример 2. Получить наборы записей указанного типа</span><span class="sxs-lookup"><span data-stu-id="1bec8-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="1bec8-117">Эта команда получает массив всех наборов записей типа A в зоне myzone.com в группе ресурсов MyResourceGroup, а затем сохраняет их в переменной $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="1bec8-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="1bec8-118">Пример 3. Получить все наборы записей в зоне</span><span class="sxs-lookup"><span data-stu-id="1bec8-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="1bec8-119">Эта команда получает массив всех наборов записей в зоне с именем myzone.com в группе ресурсов MyResourceGroup, а затем сохраняет их в переменной $RecordSets ресурса.</span><span class="sxs-lookup"><span data-stu-id="1bec8-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="1bec8-120">Пример 4. Получить все наборы записей в зоне с помощью объекта DnsZone</span><span class="sxs-lookup"><span data-stu-id="1bec8-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="1bec8-121">Этот пример эквивалентен примеру 3 выше.</span><span class="sxs-lookup"><span data-stu-id="1bec8-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="1bec8-122">На этот раз зона определяется с использованием объекта зоны.</span><span class="sxs-lookup"><span data-stu-id="1bec8-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="1bec8-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bec8-123">PARAMETERS</span></span>

### <span data-ttu-id="1bec8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bec8-124">-DefaultProfile</span></span>
<span data-ttu-id="1bec8-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1bec8-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bec8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1bec8-126">-Name</span></span>
<span data-ttu-id="1bec8-127">Имя наборов **записей,** которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="1bec8-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="1bec8-128">Если параметр Name  не задан, возвращаются все наборы записей указанного типа.</span><span class="sxs-lookup"><span data-stu-id="1bec8-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="1bec8-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="1bec8-129">-RecordType</span></span>
<span data-ttu-id="1bec8-130">Определяет тип записи DNS, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bec8-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="1bec8-131">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="1bec8-131">Valid values are:</span></span> 
- <span data-ttu-id="1bec8-132">A</span><span class="sxs-lookup"><span data-stu-id="1bec8-132">A</span></span>
- <span data-ttu-id="1bec8-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="1bec8-133">AAAA</span></span>
- <span data-ttu-id="1bec8-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="1bec8-134">CNAME</span></span>
- <span data-ttu-id="1bec8-135">MX</span><span class="sxs-lookup"><span data-stu-id="1bec8-135">MX</span></span>
- <span data-ttu-id="1bec8-136">NS</span><span class="sxs-lookup"><span data-stu-id="1bec8-136">NS</span></span>
- <span data-ttu-id="1bec8-137">PTR</span><span class="sxs-lookup"><span data-stu-id="1bec8-137">PTR</span></span>
- <span data-ttu-id="1bec8-138">SOA</span><span class="sxs-lookup"><span data-stu-id="1bec8-138">SOA</span></span>
- <span data-ttu-id="1bec8-139">SRV</span><span class="sxs-lookup"><span data-stu-id="1bec8-139">SRV</span></span>
- <span data-ttu-id="1bec8-140">TXT Если параметр *RecordType* не указан, необходимо также опустить параметр *Name.*</span><span class="sxs-lookup"><span data-stu-id="1bec8-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="1bec8-141">Затем этот cmdlet возвращает все наборы записей в зоне (всех имен и типов).</span><span class="sxs-lookup"><span data-stu-id="1bec8-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

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

### <span data-ttu-id="1bec8-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bec8-142">-ResourceGroupName</span></span>
<span data-ttu-id="1bec8-143">Определяет группу ресурсов, которая содержит зону DNS.</span><span class="sxs-lookup"><span data-stu-id="1bec8-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="1bec8-144">Имя зоны также должно быть указано с помощью *параметра ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="1bec8-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="1bec8-145">Кроме того, вы можете указать зону и группу ресурсов, указав объект **DnsZone** с помощью *параметра Zone.*</span><span class="sxs-lookup"><span data-stu-id="1bec8-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="1bec8-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="1bec8-146">-Zone</span></span>
<span data-ttu-id="1bec8-147">Определяет зону DNS, которая содержит набор записей, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bec8-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="1bec8-148">Вы также можете указать зону с помощью параметров *ZoneName* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="1bec8-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="1bec8-149">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="1bec8-149">-ZoneName</span></span>
<span data-ttu-id="1bec8-150">Имя зоны DNS, которая содержит набор записей, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="1bec8-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="1bec8-151">Также должна быть указана группа ресурсов, содержащая зону, с использованием *параметра ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="1bec8-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="1bec8-152">Вы также можете указать зону и группу ресурсов, указав объект зоны DNS с помощью *параметра Zone (Зона).*</span><span class="sxs-lookup"><span data-stu-id="1bec8-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="1bec8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bec8-153">CommonParameters</span></span>
<span data-ttu-id="1bec8-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bec8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bec8-155">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bec8-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bec8-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1bec8-156">INPUTS</span></span>

### <span data-ttu-id="1bec8-157">System.String</span><span class="sxs-lookup"><span data-stu-id="1bec8-157">System.String</span></span>

### <span data-ttu-id="1bec8-158">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="1bec8-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="1bec8-159">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1bec8-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="1bec8-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1bec8-160">OUTPUTS</span></span>

### <span data-ttu-id="1bec8-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1bec8-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="1bec8-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1bec8-162">NOTES</span></span>

## <span data-ttu-id="1bec8-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bec8-163">RELATED LINKS</span></span>

[<span data-ttu-id="1bec8-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1bec8-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="1bec8-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1bec8-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="1bec8-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1bec8-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


