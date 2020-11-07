---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 9b6d84f9007a872db0e41efa78d8e16d7269eb02
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910415"
---
# <span data-ttu-id="9e989-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="9e989-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="9e989-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e989-102">SYNOPSIS</span></span>
<span data-ttu-id="9e989-103">Обновление свойств зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="9e989-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="9e989-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e989-104">SYNTAX</span></span>

### <span data-ttu-id="9e989-105">»</span><span class="sxs-lookup"><span data-stu-id="9e989-105">Fields</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e989-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="9e989-106">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e989-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e989-107">DESCRIPTION</span></span>
<span data-ttu-id="9e989-108">Командлет **Set-AzDnsZone** обновляет указанную зону DNS в службе Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="9e989-108">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="9e989-109">Этот командлет не обновляет наборы записей в зоне.</span><span class="sxs-lookup"><span data-stu-id="9e989-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="9e989-110">Вы можете передать объект **dnsZone** как параметр или с помощью оператора конвейера или указать параметры *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="9e989-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="9e989-111">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9e989-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="9e989-112">Если зона DNS была передана как объект (с помощью объекта Zone или канала), она не будет обновлена, если она была изменена в службе DNS Azure, поскольку был получен локальный объект DnsZone.</span><span class="sxs-lookup"><span data-stu-id="9e989-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="9e989-113">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="9e989-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="9e989-114">Вы можете отключить это поведение с параметром *перезаписи* , который обновляет зону независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="9e989-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="9e989-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e989-115">EXAMPLES</span></span>

### <span data-ttu-id="9e989-116">Пример 1: обновление зоны DNS</span><span class="sxs-lookup"><span data-stu-id="9e989-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="9e989-117">Первая команда получает зону с именем myzone.com из указанной группы ресурсов, а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="9e989-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="9e989-118">Вторая команда обновляет теги для $Zone.</span><span class="sxs-lookup"><span data-stu-id="9e989-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="9e989-119">Последняя команда фиксирует изменения.</span><span class="sxs-lookup"><span data-stu-id="9e989-119">The final command commits the change.</span></span>

### <span data-ttu-id="9e989-120">Пример 2: обновление тегов для зоны</span><span class="sxs-lookup"><span data-stu-id="9e989-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="9e989-121">Эта команда обновляет теги для зоны с именем myzone.com, но сначала явно не получает зону.</span><span class="sxs-lookup"><span data-stu-id="9e989-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="9e989-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e989-122">PARAMETERS</span></span>

### <span data-ttu-id="9e989-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e989-123">-Name</span></span>
<span data-ttu-id="9e989-124">Указывает имя DNS-зоны, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="9e989-124">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="9e989-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="9e989-125">-Overwrite</span></span>
<span data-ttu-id="9e989-126">Если зона DNS была передана как объект (с помощью объекта Zone или канала), она не будет обновлена, если она была изменена в службе DNS Azure, поскольку был получен локальный объект DnsZone.</span><span class="sxs-lookup"><span data-stu-id="9e989-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="9e989-127">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="9e989-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="9e989-128">Вы можете отключить это поведение с параметром *перезаписи* , который обновляет зону независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="9e989-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e989-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e989-129">-ResourceGroupName</span></span>
<span data-ttu-id="9e989-130">Указывает имя группы ресурсов, содержащей зону для обновления.</span><span class="sxs-lookup"><span data-stu-id="9e989-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="9e989-131">Кроме того, необходимо указать параметр ZoneName.</span><span class="sxs-lookup"><span data-stu-id="9e989-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="9e989-132">Кроме того, вы можете указать зону, используя объект DnsZone с параметром *зоны* или конвейером.</span><span class="sxs-lookup"><span data-stu-id="9e989-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="9e989-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="9e989-133">-Tag</span></span>
<span data-ttu-id="9e989-134">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="9e989-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9e989-135">Например:</span><span class="sxs-lookup"><span data-stu-id="9e989-135">For example:</span></span>

<span data-ttu-id="9e989-136">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="9e989-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e989-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="9e989-137">-Zone</span></span>
<span data-ttu-id="9e989-138">Указывает зону DNS для обновления.</span><span class="sxs-lookup"><span data-stu-id="9e989-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="9e989-139">Кроме того, вы можете указать зону с помощью параметров *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="9e989-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="9e989-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e989-140">-Confirm</span></span>
<span data-ttu-id="9e989-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e989-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e989-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e989-142">-WhatIf</span></span>
<span data-ttu-id="9e989-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e989-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e989-144">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e989-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e989-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e989-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e989-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e989-146">CommonParameters</span></span>
<span data-ttu-id="9e989-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e989-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e989-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e989-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e989-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e989-149">INPUTS</span></span>

### <span data-ttu-id="9e989-150">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="9e989-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="9e989-151">Вы можете передать на этот командлет объект DnsZone.</span><span class="sxs-lookup"><span data-stu-id="9e989-151">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="9e989-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e989-152">OUTPUTS</span></span>

### <span data-ttu-id="9e989-153">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="9e989-153">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="9e989-154">Этот командлет возвращает объект DnsZone, который представляет обновленную зону DNS с новым тегом ETag.</span><span class="sxs-lookup"><span data-stu-id="9e989-154">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="9e989-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e989-155">NOTES</span></span>
<span data-ttu-id="9e989-156">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9e989-156">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="9e989-157">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="9e989-157">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="9e989-158">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="9e989-158">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="9e989-159">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9e989-159">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9e989-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e989-160">RELATED LINKS</span></span>

[<span data-ttu-id="9e989-161">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="9e989-161">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="9e989-162">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="9e989-162">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="9e989-163">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="9e989-163">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)