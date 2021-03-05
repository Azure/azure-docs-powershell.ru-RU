---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: d1b5fb606262b680d4e83f9c8e0a9ea166070ed4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984696"
---
# <span data-ttu-id="b8591-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b8591-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="b8591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8591-102">SYNOPSIS</span></span>
<span data-ttu-id="b8591-103">Обновляет свойства зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="b8591-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="b8591-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b8591-104">SYNTAX</span></span>

### <span data-ttu-id="b8591-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8591-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8591-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="b8591-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8591-107">Объект</span><span class="sxs-lookup"><span data-stu-id="b8591-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8591-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8591-108">DESCRIPTION</span></span>
<span data-ttu-id="b8591-109">**Cmdlet Set-AzDnsZone** обновляет указанную зону DNS в службе Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="b8591-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="b8591-110">Этот cmdlet не обновляет наборы записей в зоне.</span><span class="sxs-lookup"><span data-stu-id="b8591-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="b8591-111">Объект **DnsZone** можно передать в качестве параметра или с помощью оператора конвейера. Кроме того, можно указать параметры *ZoneName* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="b8591-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="b8591-112">Параметр Confirm  и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8591-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b8591-113">При передаче зоны DNS в качестве объекта (с использованием объекта Zone или через конвейер) она не обновляется, если она была изменена в Azure DNS после извлечения локального объекта DnsZone.</span><span class="sxs-lookup"><span data-stu-id="b8591-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="b8591-114">Это обеспечивает защиту от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="b8591-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="b8591-115">Это поведение можно скрыть с помощью параметра *Overwrite,* который обновляет зону независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="b8591-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="b8591-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b8591-116">EXAMPLES</span></span>

### <span data-ttu-id="b8591-117">Пример 1. Обновление зоны DNS</span><span class="sxs-lookup"><span data-stu-id="b8591-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="b8591-118">Первая команда получает зону с именем myzone.com из указанной группы ресурсов, а затем сохраняет ее в переменной $Zone ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8591-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="b8591-119">Вторая команда обновляет теги для $Zone.</span><span class="sxs-lookup"><span data-stu-id="b8591-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="b8591-120">Конечная команда зафиксировать изменение.</span><span class="sxs-lookup"><span data-stu-id="b8591-120">The final command commits the change.</span></span>

### <span data-ttu-id="b8591-121">Пример 2. Обновление тегов для зоны</span><span class="sxs-lookup"><span data-stu-id="b8591-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="b8591-122">Эта команда обновляет теги зоны с именем myzone.com, не получая ее явным образом.</span><span class="sxs-lookup"><span data-stu-id="b8591-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="b8591-123">Пример 3. Связывание частной зоны с виртуальной сетью путем указания ее ID</span><span class="sxs-lookup"><span data-stu-id="b8591-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="b8591-124">Эта команда связывает зону myprivatezone.com DNS с виртуальной сетевой myvnet в качестве сети регистрации, указав ее ID.</span><span class="sxs-lookup"><span data-stu-id="b8591-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="b8591-125">Пример 4. Связывание частной зоны с виртуальной сетью путем указания сетевого объекта.</span><span class="sxs-lookup"><span data-stu-id="b8591-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="b8591-126">Эта команда связывает частную зону DNS myprivatezone.com с виртуальной сетевой myvnet в качестве сети регистрации путем передачи командлету командлета $vnet, представленного переменной Set-AzDnsZone сети.</span><span class="sxs-lookup"><span data-stu-id="b8591-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="b8591-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8591-127">PARAMETERS</span></span>

### <span data-ttu-id="b8591-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8591-128">-DefaultProfile</span></span>
<span data-ttu-id="b8591-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b8591-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8591-130">-Name</span><span class="sxs-lookup"><span data-stu-id="b8591-130">-Name</span></span>
<span data-ttu-id="b8591-131">Указывает имя зоны DNS, которая будет обновляться.</span><span class="sxs-lookup"><span data-stu-id="b8591-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8591-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="b8591-132">-Overwrite</span></span>
<span data-ttu-id="b8591-133">При передаче зоны DNS в качестве объекта (с использованием объекта Zone или через конвейер) она не обновляется, если она была изменена в Azure DNS после извлечения локального объекта DnsZone.</span><span class="sxs-lookup"><span data-stu-id="b8591-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="b8591-134">Это обеспечивает защиту от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="b8591-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="b8591-135">Это поведение можно скрыть с помощью параметра *Overwrite,* который обновляет зону независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="b8591-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="b8591-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b8591-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="b8591-137">Список виртуальных сетей, которые будут регистрировать записи об именах хостов виртуальной машины в этой зоне DNS, доступен только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="b8591-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8591-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b8591-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="b8591-139">Список виртуальных сетевых кодов, которые будут регистрировать записи об именах хостов виртуальных машин в этой зоне DNS, доступен только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="b8591-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8591-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b8591-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="b8591-141">Список виртуальных сетей для разрешения записей в этой зоне DNS, доступный только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="b8591-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8591-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="b8591-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="b8591-143">Список виртуальных сетевых ИД, которые можно разрешать записи в этой зоне DNS, доступен только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="b8591-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8591-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8591-144">-ResourceGroupName</span></span>
<span data-ttu-id="b8591-145">Имя группы ресурсов, которая содержит зону для обновления.</span><span class="sxs-lookup"><span data-stu-id="b8591-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="b8591-146">Необходимо также указать параметр ZoneName.</span><span class="sxs-lookup"><span data-stu-id="b8591-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="b8591-147">Кроме того, вы можете указать зону с помощью объекта DnsZone с *параметром Zone (Зона)* или pipeline (Канал).</span><span class="sxs-lookup"><span data-stu-id="b8591-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8591-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="b8591-148">-Tag</span></span>
<span data-ttu-id="b8591-149">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="b8591-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b8591-150">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="b8591-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8591-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="b8591-151">-Zone</span></span>
<span data-ttu-id="b8591-152">Указывает зону DNS, которая будет обновляться.</span><span class="sxs-lookup"><span data-stu-id="b8591-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="b8591-153">Вы также можете указать зону с помощью параметров *ZoneName* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="b8591-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="b8591-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8591-154">-Confirm</span></span>
<span data-ttu-id="b8591-155">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8591-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8591-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8591-156">-WhatIf</span></span>
<span data-ttu-id="b8591-157">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8591-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8591-158">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8591-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8591-159">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b8591-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8591-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8591-160">CommonParameters</span></span>
<span data-ttu-id="b8591-161">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8591-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8591-162">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8591-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8591-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8591-163">INPUTS</span></span>

### <span data-ttu-id="b8591-164">System.String</span><span class="sxs-lookup"><span data-stu-id="b8591-164">System.String</span></span>

### <span data-ttu-id="b8591-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b8591-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b8591-166">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8591-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b8591-167">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b8591-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b8591-168">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="b8591-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="b8591-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b8591-169">OUTPUTS</span></span>

### <span data-ttu-id="b8591-170">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="b8591-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="b8591-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b8591-171">NOTES</span></span>
<span data-ttu-id="b8591-172">С помощью параметра *Confirm* (Подтвердить) можно управлять запросом на подтверждение с помощью этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8591-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b8591-173">По умолчанию с помощью cmdlet вы можете получить подтверждение, если переменная $ConfirmPreference Windows PowerShell имеет значение "Средний" или "Ниже".</span><span class="sxs-lookup"><span data-stu-id="b8591-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="b8591-174">Если указать *"Подтвердить"* или *"$True:$True",* этот cmdlet запросит подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="b8591-174">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="b8591-175">Если *указать confirm:$False,* то при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="b8591-175">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b8591-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8591-176">RELATED LINKS</span></span>

[<span data-ttu-id="b8591-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b8591-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="b8591-178">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b8591-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="b8591-179">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b8591-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
