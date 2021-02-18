---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214817"
---
# <span data-ttu-id="295cc-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="295cc-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="295cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="295cc-102">SYNOPSIS</span></span>
<span data-ttu-id="295cc-103">Удаляет набор записей.</span><span class="sxs-lookup"><span data-stu-id="295cc-103">Deletes a record set.</span></span>

## <span data-ttu-id="295cc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="295cc-104">SYNTAX</span></span>

### <span data-ttu-id="295cc-105">Поля</span><span class="sxs-lookup"><span data-stu-id="295cc-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="295cc-106">Смешанный</span><span class="sxs-lookup"><span data-stu-id="295cc-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="295cc-107">Объект</span><span class="sxs-lookup"><span data-stu-id="295cc-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="295cc-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="295cc-108">DESCRIPTION</span></span>
<span data-ttu-id="295cc-109">Для удаления указанного набора записей из указанной зоны будет удален набор записей **Remove-AzDnsRecordSet.**</span><span class="sxs-lookup"><span data-stu-id="295cc-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="295cc-110">Нельзя удалить soA или NS-записи, автоматически созданные в апексе зоны.</span><span class="sxs-lookup"><span data-stu-id="295cc-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="295cc-111">Передать объект **RecordSet** этому cmdlet можно с помощью оператора конвейера или параметра.</span><span class="sxs-lookup"><span data-stu-id="295cc-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="295cc-112">Чтобы определить запись, заданную по имени и типу, без использования объекта **RecordSet,** необходимо передать эту зону в качестве объекта **DnsZone** этому cmdlet с помощью оператора конвейера или в качестве параметра либо указать *параметры ZoneName* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="295cc-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="295cc-113">С помощью переменных Confirm и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="295cc-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="295cc-114">При указании набора записей с использованием объекта **RecordSet** набор записей не удаляется, если он был изменен в Azure DNS после извлечения локального объекта **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="295cc-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="295cc-115">Это обеспечивает защиту от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="295cc-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="295cc-116">Вы можете скрыть это с помощью параметра *Overwrite,* который удаляет набор записей независимо от изменений одновременно.</span><span class="sxs-lookup"><span data-stu-id="295cc-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="295cc-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="295cc-117">EXAMPLES</span></span>

### <span data-ttu-id="295cc-118">Пример 1. Удаление набора записей</span><span class="sxs-lookup"><span data-stu-id="295cc-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="295cc-119">Первая команда получает указанный набор записей, а затем сохраняет его в $RecordSet переменной. Вторая команда удаляет набор записей из $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="295cc-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="295cc-120">Пример 2. Удаление набора записей и подавления всего подтверждения</span><span class="sxs-lookup"><span data-stu-id="295cc-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="295cc-121">Первая команда получает указанный набор записей.</span><span class="sxs-lookup"><span data-stu-id="295cc-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="295cc-122">Вторая команда удаляет набор записей, даже если он изменился до этого времени.</span><span class="sxs-lookup"><span data-stu-id="295cc-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="295cc-123">Запросы на подтверждение будут подавляться.</span><span class="sxs-lookup"><span data-stu-id="295cc-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="295cc-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="295cc-124">PARAMETERS</span></span>

### <span data-ttu-id="295cc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="295cc-125">-DefaultProfile</span></span>
<span data-ttu-id="295cc-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="295cc-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="295cc-127">-Name</span><span class="sxs-lookup"><span data-stu-id="295cc-127">-Name</span></span>
<span data-ttu-id="295cc-128">Имя наборов **записей,** которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="295cc-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="295cc-129">При указании записи, заданной по имени, необходимо указать зону DNS с помощью параметра *Zone* или *ZoneName* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="295cc-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="295cc-130">Набор записей также можно укадрять с помощью объекта **RecordSet,** который передается с помощью *параметра RecordSet.*</span><span class="sxs-lookup"><span data-stu-id="295cc-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="295cc-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="295cc-131">-Overwrite</span></span>
<span data-ttu-id="295cc-132">При указании набора записей с использованием объекта **RecordSet** набор записей не удаляется, если он был изменен в Azure DNS после извлечения локального объекта **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="295cc-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="295cc-133">Это обеспечивает защиту от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="295cc-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="295cc-134">Это можно сделать с помощью параметра *Overwrite,* который удаляет набор записей независимо от изменений одновременно.</span><span class="sxs-lookup"><span data-stu-id="295cc-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="295cc-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="295cc-135">-PassThru</span></span>
<span data-ttu-id="295cc-136">passthru</span><span class="sxs-lookup"><span data-stu-id="295cc-136">passthru</span></span>

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

### <span data-ttu-id="295cc-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="295cc-137">-RecordSet</span></span>
<span data-ttu-id="295cc-138">Определяет объект **RecordSet,** который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="295cc-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="295cc-139">Кроме того, набор записей можно настроить с помощью параметров  *Name* и *Zone* (Имя), *ZoneName*(Имя зоны) и *ResourceGroupName (Имя* группы ресурсов).</span><span class="sxs-lookup"><span data-stu-id="295cc-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="295cc-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="295cc-140">-RecordType</span></span>
<span data-ttu-id="295cc-141">Тип записи DNS.</span><span class="sxs-lookup"><span data-stu-id="295cc-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="295cc-142">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="295cc-142">Valid values are:</span></span>
- <span data-ttu-id="295cc-143">A</span><span class="sxs-lookup"><span data-stu-id="295cc-143">A</span></span>
- <span data-ttu-id="295cc-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="295cc-144">AAAA</span></span>
- <span data-ttu-id="295cc-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="295cc-145">CNAME</span></span>
- <span data-ttu-id="295cc-146">MX</span><span class="sxs-lookup"><span data-stu-id="295cc-146">MX</span></span>
- <span data-ttu-id="295cc-147">NS</span><span class="sxs-lookup"><span data-stu-id="295cc-147">NS</span></span>
- <span data-ttu-id="295cc-148">PTR</span><span class="sxs-lookup"><span data-stu-id="295cc-148">PTR</span></span>
- <span data-ttu-id="295cc-149">SRV</span><span class="sxs-lookup"><span data-stu-id="295cc-149">SRV</span></span>
- <span data-ttu-id="295cc-150">При удалении зоны записи TXT SOA удаляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="295cc-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="295cc-151">Удалить записи SOA вручную нельзя.</span><span class="sxs-lookup"><span data-stu-id="295cc-151">You cannot manually delete SOA records.</span></span>

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

### <span data-ttu-id="295cc-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="295cc-152">-ResourceGroupName</span></span>
<span data-ttu-id="295cc-153">Определяет группу ресурсов, которая содержит зону DNS, которая содержит **набор записей,** который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="295cc-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="295cc-154">Этот параметр применяется только в том случае, если набор записей и зона DNS заданы с использованием параметров *Name* и *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="295cc-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="295cc-155">Кроме того, набор записей можно указать с помощью *параметра RecordSet* или *параметров Name* и *Zone.*</span><span class="sxs-lookup"><span data-stu-id="295cc-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="295cc-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="295cc-156">-Zone</span></span>
<span data-ttu-id="295cc-157">Определяет зону DNS, которая содержит **набор записей,** который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="295cc-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="295cc-158">Этот параметр применяется только при указании набора записей с помощью *параметра Name.*</span><span class="sxs-lookup"><span data-stu-id="295cc-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="295cc-159">Кроме того, набор записей можно указать с помощью параметра *RecordSet* или параметров *Name,* *ZoneName* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="295cc-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="295cc-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="295cc-160">-ZoneName</span></span>
<span data-ttu-id="295cc-161">Имя зоны, которая содержит **набор записей,** который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="295cc-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="295cc-162">Необходимо также указать *параметры Name* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="295cc-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="295cc-163">Кроме того, набор записей можно укадрять с помощью *параметра RecordSet* или *параметра Name* и *Zone.*</span><span class="sxs-lookup"><span data-stu-id="295cc-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="295cc-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="295cc-164">-Confirm</span></span>
<span data-ttu-id="295cc-165">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="295cc-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="295cc-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="295cc-166">-WhatIf</span></span>
<span data-ttu-id="295cc-167">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="295cc-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="295cc-168">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="295cc-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="295cc-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="295cc-169">CommonParameters</span></span>
<span data-ttu-id="295cc-170">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="295cc-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="295cc-171">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="295cc-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="295cc-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="295cc-172">INPUTS</span></span>

### <span data-ttu-id="295cc-173">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="295cc-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="295cc-174">System.String</span><span class="sxs-lookup"><span data-stu-id="295cc-174">System.String</span></span>

### <span data-ttu-id="295cc-175">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="295cc-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="295cc-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="295cc-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="295cc-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="295cc-177">OUTPUTS</span></span>

### <span data-ttu-id="295cc-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="295cc-178">System.Boolean</span></span>

## <span data-ttu-id="295cc-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="295cc-179">NOTES</span></span>
<span data-ttu-id="295cc-180">С помощью параметра *Confirm* (Подтвердить) можно управлять запросом на подтверждение с помощью этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="295cc-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="295cc-181">По умолчанию с помощью cmdlet вы можете получить подтверждение, если переменная $ConfirmPreference Windows PowerShell имеет значение "Средний" или "Ниже".</span><span class="sxs-lookup"><span data-stu-id="295cc-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="295cc-182">Если указать *"Подтвердить"* или *"$True:$True",* этот cmdlet запросит подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="295cc-182">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="295cc-183">Если *указать confirm:$False,* то при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="295cc-183">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="295cc-184">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="295cc-184">RELATED LINKS</span></span>

[<span data-ttu-id="295cc-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="295cc-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="295cc-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="295cc-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="295cc-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="295cc-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
