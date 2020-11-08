---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243606"
---
# <span data-ttu-id="b0be5-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b0be5-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="b0be5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0be5-102">SYNOPSIS</span></span>
<span data-ttu-id="b0be5-103">Удаляет набор записей.</span><span class="sxs-lookup"><span data-stu-id="b0be5-103">Deletes a record set.</span></span>

## <span data-ttu-id="b0be5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0be5-104">SYNTAX</span></span>

### <span data-ttu-id="b0be5-105">»</span><span class="sxs-lookup"><span data-stu-id="b0be5-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0be5-106">Смешивания</span><span class="sxs-lookup"><span data-stu-id="b0be5-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0be5-107">DataObject</span><span class="sxs-lookup"><span data-stu-id="b0be5-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0be5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0be5-108">DESCRIPTION</span></span>
<span data-ttu-id="b0be5-109">Командлет **Remove-AzDnsRecordSet** удаляет набор записей из указанной зоны.</span><span class="sxs-lookup"><span data-stu-id="b0be5-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="b0be5-110">Вы не можете удалить записи SOA или сервера имен (NS), которые будут автоматически созданы на зоне Апекс.</span><span class="sxs-lookup"><span data-stu-id="b0be5-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="b0be5-111">Вы можете передать в этот командлет объект **набора записей** с помощью оператора конвейера или в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="b0be5-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="b0be5-112">Чтобы определить набор записей по имени и типу, не используя объект **Recordset** , необходимо передать зону как объект **dnsZone** с помощью оператора конвейера или в качестве параметра либо можно указать параметры *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="b0be5-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="b0be5-113">Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b0be5-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b0be5-114">При указании набора записей с помощью объекта **Recordset** набор записей не удаляется, если он был изменен в Azure DNS, так как был получен объект локального **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b0be5-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="b0be5-115">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="b0be5-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="b0be5-116">Вы можете отключить этот параметр с помощью параметра *overwrite* , который удаляет набор записей независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="b0be5-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="b0be5-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0be5-117">EXAMPLES</span></span>

### <span data-ttu-id="b0be5-118">Пример 1: удаление набор записей</span><span class="sxs-lookup"><span data-stu-id="b0be5-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="b0be5-119">Первая команда получает указанный наборы записей и сохраняет ее в переменной $RecordSet. Вторая команда удаляет запись, указанную в $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="b0be5-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="b0be5-120">Пример 2: удаление набор записей и отключение всех подтверждений</span><span class="sxs-lookup"><span data-stu-id="b0be5-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="b0be5-121">Первая команда получает указанный наборы записей.</span><span class="sxs-lookup"><span data-stu-id="b0be5-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="b0be5-122">Вторая команда удаляет наборы записей, даже если она была изменена.</span><span class="sxs-lookup"><span data-stu-id="b0be5-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="b0be5-123">Запросы на подтверждение подавляются.</span><span class="sxs-lookup"><span data-stu-id="b0be5-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="b0be5-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0be5-124">PARAMETERS</span></span>

### <span data-ttu-id="b0be5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0be5-125">-DefaultProfile</span></span>
<span data-ttu-id="b0be5-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b0be5-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0be5-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b0be5-127">-Name</span></span>
<span data-ttu-id="b0be5-128">Указывает имя **набора записей** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b0be5-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="b0be5-129">Когда вы указываете набор записей по имени, зона DNS должна быть указана с помощью параметра *Zone* или параметров *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="b0be5-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="b0be5-130">Кроме того, набор записей можно указать с помощью объекта **Recordset** , передаваемого с помощью параметра *Recordset* .</span><span class="sxs-lookup"><span data-stu-id="b0be5-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0be5-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="b0be5-131">-Overwrite</span></span>
<span data-ttu-id="b0be5-132">При указании набора записей с помощью объекта **Recordset** набор записей не удаляется, если он был изменен в Azure DNS, так как был получен объект локального **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b0be5-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="b0be5-133">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="b0be5-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="b0be5-134">Это может быть подавлено с помощью параметра *overwrite* , который удаляет набор записей независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="b0be5-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0be5-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0be5-135">-PassThru</span></span>
<span data-ttu-id="b0be5-136">PassThru</span><span class="sxs-lookup"><span data-stu-id="b0be5-136">passthru</span></span>

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

### <span data-ttu-id="b0be5-137">-Набор записей</span><span class="sxs-lookup"><span data-stu-id="b0be5-137">-RecordSet</span></span>
<span data-ttu-id="b0be5-138">Указывает объект **набора записей** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b0be5-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="b0be5-139">Кроме того, можно задать набор записей с помощью параметров *имени* и *зоны* либо с помощью параметров *Name* , *имя_зоны* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="b0be5-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0be5-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="b0be5-140">-RecordType</span></span>
<span data-ttu-id="b0be5-141">Указывает тип DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="b0be5-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="b0be5-142">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="b0be5-142">Valid values are:</span></span>
- <span data-ttu-id="b0be5-143">Помощью</span><span class="sxs-lookup"><span data-stu-id="b0be5-143">A</span></span>
- <span data-ttu-id="b0be5-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="b0be5-144">AAAA</span></span>
- <span data-ttu-id="b0be5-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="b0be5-145">CNAME</span></span>
- <span data-ttu-id="b0be5-146">МХ</span><span class="sxs-lookup"><span data-stu-id="b0be5-146">MX</span></span>
- <span data-ttu-id="b0be5-147">СЛУЖБУ</span><span class="sxs-lookup"><span data-stu-id="b0be5-147">NS</span></span>
- <span data-ttu-id="b0be5-148">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="b0be5-148">PTR</span></span>
- <span data-ttu-id="b0be5-149">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="b0be5-149">SRV</span></span>
- <span data-ttu-id="b0be5-150">Записи SOA (TXT) удаляются автоматически при удалении зоны.</span><span class="sxs-lookup"><span data-stu-id="b0be5-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="b0be5-151">Записи SOA нельзя удалять вручную.</span><span class="sxs-lookup"><span data-stu-id="b0be5-151">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0be5-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0be5-152">-ResourceGroupName</span></span>
<span data-ttu-id="b0be5-153">Указывает группу ресурсов, которая содержит DNS-зону, которая содержит **набор записей** для удаления.</span><span class="sxs-lookup"><span data-stu-id="b0be5-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="b0be5-154">Этот параметр применяется только в том случае, если набор записей и зона DNS указаны с использованием параметров *Name* и *zonename* .</span><span class="sxs-lookup"><span data-stu-id="b0be5-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="b0be5-155">Кроме того, вы можете задать набор записей с помощью параметра " *набор записей* " или параметров " *имя* " и " *зона* ".</span><span class="sxs-lookup"><span data-stu-id="b0be5-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="b0be5-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="b0be5-156">-Zone</span></span>
<span data-ttu-id="b0be5-157">Указывает DNS-зону, которая содержит **набор записей** для удаления.</span><span class="sxs-lookup"><span data-stu-id="b0be5-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="b0be5-158">Этот параметр применяется только при указании заданной записи с помощью параметра *Name* .</span><span class="sxs-lookup"><span data-stu-id="b0be5-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="b0be5-159">Кроме того, вы можете задать набор записей с помощью параметра " *набор записей* " или параметров *Name* , *имя_зоны* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="b0be5-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0be5-160">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="b0be5-160">-ZoneName</span></span>
<span data-ttu-id="b0be5-161">Указывает имя зоны, содержащей **набор записей** для удаления.</span><span class="sxs-lookup"><span data-stu-id="b0be5-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="b0be5-162">Кроме того, необходимо указать параметры *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="b0be5-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="b0be5-163">Кроме того, можно задать набор записей с помощью параметра " *набор записей* ", а также параметров *имени* и *зоны* .</span><span class="sxs-lookup"><span data-stu-id="b0be5-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="b0be5-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0be5-164">-Confirm</span></span>
<span data-ttu-id="b0be5-165">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b0be5-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0be5-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0be5-166">-WhatIf</span></span>
<span data-ttu-id="b0be5-167">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b0be5-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0be5-168">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b0be5-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0be5-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0be5-169">CommonParameters</span></span>
<span data-ttu-id="b0be5-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0be5-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0be5-171">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0be5-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0be5-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0be5-172">INPUTS</span></span>

### <span data-ttu-id="b0be5-173">Microsoft. Azure. Management. DNS. Models. RecordType</span><span class="sxs-lookup"><span data-stu-id="b0be5-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="b0be5-174">System. String</span><span class="sxs-lookup"><span data-stu-id="b0be5-174">System.String</span></span>

### <span data-ttu-id="b0be5-175">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="b0be5-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="b0be5-176">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b0be5-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="b0be5-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0be5-177">OUTPUTS</span></span>

### <span data-ttu-id="b0be5-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0be5-178">System.Boolean</span></span>

## <span data-ttu-id="b0be5-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0be5-179">NOTES</span></span>
<span data-ttu-id="b0be5-180">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b0be5-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b0be5-181">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="b0be5-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="b0be5-182">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="b0be5-182">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="b0be5-183">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b0be5-183">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b0be5-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0be5-184">RELATED LINKS</span></span>

[<span data-ttu-id="b0be5-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b0be5-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="b0be5-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b0be5-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="b0be5-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b0be5-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
