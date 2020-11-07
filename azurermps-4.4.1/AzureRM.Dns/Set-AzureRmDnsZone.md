---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: 9d4e0e376e611e1373d30ab6b3aeafb51f363c31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734062"
---
# <span data-ttu-id="b46b4-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b46b4-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="b46b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b46b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b46b4-103">Обновление свойств зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="b46b4-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b46b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b46b4-104">SYNTAX</span></span>

### <span data-ttu-id="b46b4-105">»</span><span class="sxs-lookup"><span data-stu-id="b46b4-105">Fields</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b46b4-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="b46b4-106">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b46b4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b46b4-107">DESCRIPTION</span></span>
<span data-ttu-id="b46b4-108">Командлет **Set-AzureRmDnsZone** обновляет указанную зону DNS в службе Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="b46b4-108">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="b46b4-109">Этот командлет не обновляет наборы записей в зоне.</span><span class="sxs-lookup"><span data-stu-id="b46b4-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="b46b4-110">Вы можете передать объект **dnsZone** как параметр или с помощью оператора конвейера или указать параметры *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="b46b4-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="b46b4-111">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b46b4-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="b46b4-112">Если зона DNS была передана как объект (с помощью объекта Zone или канала), она не будет обновлена, если она была изменена в службе DNS Azure, поскольку был получен локальный объект DnsZone.</span><span class="sxs-lookup"><span data-stu-id="b46b4-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="b46b4-113">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="b46b4-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="b46b4-114">Вы можете отключить это поведение с параметром *перезаписи* , который обновляет зону независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="b46b4-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="b46b4-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b46b4-115">EXAMPLES</span></span>

### <span data-ttu-id="b46b4-116">Пример 1: обновление зоны DNS</span><span class="sxs-lookup"><span data-stu-id="b46b4-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="b46b4-117">Первая команда получает зону с именем myzone.com из указанной группы ресурсов, а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="b46b4-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="b46b4-118">Вторая команда обновляет теги для $Zone.</span><span class="sxs-lookup"><span data-stu-id="b46b4-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="b46b4-119">Последняя команда фиксирует изменения.</span><span class="sxs-lookup"><span data-stu-id="b46b4-119">The final command commits the change.</span></span>

### <span data-ttu-id="b46b4-120">Пример 2: обновление тегов для зоны</span><span class="sxs-lookup"><span data-stu-id="b46b4-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="b46b4-121">Эта команда обновляет теги для зоны с именем myzone.com, но сначала явно не получает зону.</span><span class="sxs-lookup"><span data-stu-id="b46b4-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="b46b4-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b46b4-122">PARAMETERS</span></span>

### <span data-ttu-id="b46b4-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b46b4-123">-Name</span></span>
<span data-ttu-id="b46b4-124">Указывает имя DNS-зоны, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="b46b4-124">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="b46b4-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="b46b4-125">-Overwrite</span></span>
<span data-ttu-id="b46b4-126">Если зона DNS была передана как объект (с помощью объекта Zone или канала), она не будет обновлена, если она была изменена в службе DNS Azure, поскольку был получен локальный объект DnsZone.</span><span class="sxs-lookup"><span data-stu-id="b46b4-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="b46b4-127">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="b46b4-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="b46b4-128">Вы можете отключить это поведение с параметром *перезаписи* , который обновляет зону независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="b46b4-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="b46b4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b46b4-129">-ResourceGroupName</span></span>
<span data-ttu-id="b46b4-130">Указывает имя группы ресурсов, содержащей зону для обновления.</span><span class="sxs-lookup"><span data-stu-id="b46b4-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="b46b4-131">Кроме того, необходимо указать параметр ZoneName.</span><span class="sxs-lookup"><span data-stu-id="b46b4-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="b46b4-132">Кроме того, вы можете указать зону, используя объект DnsZone с параметром *зоны* или конвейером.</span><span class="sxs-lookup"><span data-stu-id="b46b4-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="b46b4-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="b46b4-133">-Tag</span></span>
<span data-ttu-id="b46b4-134">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="b46b4-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b46b4-135">Например:</span><span class="sxs-lookup"><span data-stu-id="b46b4-135">For example:</span></span>

<span data-ttu-id="b46b4-136">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="b46b4-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b46b4-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="b46b4-137">-Zone</span></span>
<span data-ttu-id="b46b4-138">Указывает зону DNS для обновления.</span><span class="sxs-lookup"><span data-stu-id="b46b4-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="b46b4-139">Кроме того, вы можете указать зону с помощью параметров *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="b46b4-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="b46b4-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b46b4-140">-Confirm</span></span>
<span data-ttu-id="b46b4-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b46b4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b46b4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b46b4-142">-WhatIf</span></span>
<span data-ttu-id="b46b4-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b46b4-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b46b4-144">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b46b4-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b46b4-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b46b4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b46b4-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b46b4-146">-DefaultProfile</span></span>
<span data-ttu-id="b46b4-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b46b4-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b46b4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b46b4-148">CommonParameters</span></span>
<span data-ttu-id="b46b4-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b46b4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b46b4-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b46b4-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b46b4-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b46b4-151">INPUTS</span></span>

### <span data-ttu-id="b46b4-152">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="b46b4-152">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="b46b4-153">Вы можете передать на этот командлет объект DnsZone.</span><span class="sxs-lookup"><span data-stu-id="b46b4-153">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="b46b4-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b46b4-154">OUTPUTS</span></span>

### <span data-ttu-id="b46b4-155">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="b46b4-155">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="b46b4-156">Этот командлет возвращает объект DnsZone, который представляет обновленную зону DNS с новым тегом ETag.</span><span class="sxs-lookup"><span data-stu-id="b46b4-156">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="b46b4-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="b46b4-157">NOTES</span></span>
<span data-ttu-id="b46b4-158">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b46b4-158">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b46b4-159">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="b46b4-159">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="b46b4-160">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="b46b4-160">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="b46b4-161">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b46b4-161">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b46b4-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b46b4-162">RELATED LINKS</span></span>

[<span data-ttu-id="b46b4-163">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b46b4-163">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="b46b4-164">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b46b4-164">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="b46b4-165">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="b46b4-165">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
