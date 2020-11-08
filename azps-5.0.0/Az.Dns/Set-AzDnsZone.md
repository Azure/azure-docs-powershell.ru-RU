---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 956dbc54d565c4aed074df54b550f8c8aa7b18ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248717"
---
# <span data-ttu-id="cd4aa-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="cd4aa-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="cd4aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4aa-103">Обновление свойств зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="cd4aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd4aa-104">SYNTAX</span></span>

### <span data-ttu-id="cd4aa-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd4aa-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd4aa-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="cd4aa-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd4aa-107">DataObject</span><span class="sxs-lookup"><span data-stu-id="cd4aa-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd4aa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd4aa-108">DESCRIPTION</span></span>
<span data-ttu-id="cd4aa-109">Командлет **Set-AzDnsZone** обновляет указанную зону DNS в службе Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="cd4aa-110">Этот командлет не обновляет наборы записей в зоне.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="cd4aa-111">Вы можете передать объект **dnsZone** как параметр или с помощью оператора конвейера или указать параметры *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="cd4aa-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="cd4aa-112">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="cd4aa-113">Если зона DNS была передана как объект (с помощью объекта Zone или канала), она не будет обновлена, если она была изменена в службе DNS Azure, поскольку был получен локальный объект DnsZone.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="cd4aa-114">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="cd4aa-115">Вы можете отключить это поведение с параметром *перезаписи* , который обновляет зону независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="cd4aa-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd4aa-116">EXAMPLES</span></span>

### <span data-ttu-id="cd4aa-117">Пример 1: обновление зоны DNS</span><span class="sxs-lookup"><span data-stu-id="cd4aa-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="cd4aa-118">Первая команда получает зону с именем myzone.com из указанной группы ресурсов, а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="cd4aa-119">Вторая команда обновляет теги для $Zone.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="cd4aa-120">Последняя команда фиксирует изменения.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-120">The final command commits the change.</span></span>

### <span data-ttu-id="cd4aa-121">Пример 2: обновление тегов для зоны</span><span class="sxs-lookup"><span data-stu-id="cd4aa-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="cd4aa-122">Эта команда обновляет теги для зоны с именем myzone.com, но сначала явно не получает зону.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="cd4aa-123">Пример 3: связывание частной зоны с виртуальной сетью с указанием идентификатора</span><span class="sxs-lookup"><span data-stu-id="cd4aa-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="cd4aa-124">Эта команда связывает личную зону DNS myprivatezone.com с виртуальной сетью myvnet как сеть регистрации, указав ее идентификатор.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="cd4aa-125">Пример 4: привязка частной зоны к виртуальной сети путем указания сетевого объекта.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="cd4aa-126">Эта команда связывает частную зону DNS myprivatezone.com с виртуальной сетью myvnet в качестве сети регистрации, передавая объект виртуальной сети, представленный переменной $vnet, в командлет Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="cd4aa-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd4aa-127">PARAMETERS</span></span>

### <span data-ttu-id="cd4aa-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd4aa-128">-DefaultProfile</span></span>
<span data-ttu-id="cd4aa-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cd4aa-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd4aa-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cd4aa-130">-Name</span></span>
<span data-ttu-id="cd4aa-131">Указывает имя DNS-зоны, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-131">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="cd4aa-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="cd4aa-132">-Overwrite</span></span>
<span data-ttu-id="cd4aa-133">Если зона DNS была передана как объект (с помощью объекта Zone или канала), она не будет обновлена, если она была изменена в службе DNS Azure, поскольку был получен локальный объект DnsZone.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="cd4aa-134">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="cd4aa-135">Вы можете отключить это поведение с параметром *перезаписи* , который обновляет зону независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="cd4aa-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cd4aa-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="cd4aa-137">Список виртуальных сетей, которые будут регистрировать записи hostname для виртуальных машин в этой зоне DNS, доступны только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="cd4aa-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="cd4aa-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="cd4aa-139">Список идентификаторов виртуальных сетей, которые будут регистрировать записи hostname для виртуальных машин в этой зоне DNS, только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="cd4aa-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cd4aa-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="cd4aa-141">Список виртуальных сетей, которые можно использовать для разрешения записей в этой зоне DNS, только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="cd4aa-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="cd4aa-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="cd4aa-143">Список идентификаторов виртуальных сетей, которые можно использовать для разрешения записей в этой зоне DNS, только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="cd4aa-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd4aa-144">-ResourceGroupName</span></span>
<span data-ttu-id="cd4aa-145">Указывает имя группы ресурсов, содержащей зону для обновления.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="cd4aa-146">Кроме того, необходимо указать параметр ZoneName.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="cd4aa-147">Кроме того, вы можете указать зону, используя объект DnsZone с параметром *зоны* или конвейером.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="cd4aa-148">-Тег</span><span class="sxs-lookup"><span data-stu-id="cd4aa-148">-Tag</span></span>
<span data-ttu-id="cd4aa-149">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cd4aa-150">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="cd4aa-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cd4aa-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="cd4aa-151">-Zone</span></span>
<span data-ttu-id="cd4aa-152">Указывает зону DNS для обновления.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="cd4aa-153">Кроме того, вы можете указать зону с помощью параметров *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="cd4aa-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="cd4aa-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd4aa-154">-Confirm</span></span>
<span data-ttu-id="cd4aa-155">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd4aa-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd4aa-156">-WhatIf</span></span>
<span data-ttu-id="cd4aa-157">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd4aa-158">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd4aa-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd4aa-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4aa-160">CommonParameters</span></span>
<span data-ttu-id="cd4aa-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4aa-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd4aa-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4aa-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd4aa-163">INPUTS</span></span>

### <span data-ttu-id="cd4aa-164">System. String</span><span class="sxs-lookup"><span data-stu-id="cd4aa-164">System.String</span></span>

### <span data-ttu-id="cd4aa-165">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cd4aa-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cd4aa-166">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cd4aa-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cd4aa-167">System. Collections. Generic. List "1 [[Microsoft. Azure. Management. internal. Network. Common. IResourceReference, Microsoft. Azure. Windows. Clients. Network, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cd4aa-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="cd4aa-168">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="cd4aa-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="cd4aa-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd4aa-169">OUTPUTS</span></span>

### <span data-ttu-id="cd4aa-170">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="cd4aa-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="cd4aa-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd4aa-171">NOTES</span></span>
<span data-ttu-id="cd4aa-172">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="cd4aa-173">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="cd4aa-174">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-174">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="cd4aa-175">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cd4aa-175">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="cd4aa-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd4aa-176">RELATED LINKS</span></span>

[<span data-ttu-id="cd4aa-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="cd4aa-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="cd4aa-178">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="cd4aa-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="cd4aa-179">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="cd4aa-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
