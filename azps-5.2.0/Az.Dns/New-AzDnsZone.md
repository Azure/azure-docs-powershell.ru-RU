---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402372"
---
# <span data-ttu-id="bafd6-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="bafd6-101">New-AzDnsZone</span></span>

## <span data-ttu-id="bafd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bafd6-102">SYNOPSIS</span></span>
<span data-ttu-id="bafd6-103">Создает новую зону DNS.</span><span class="sxs-lookup"><span data-stu-id="bafd6-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="bafd6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bafd6-104">SYNTAX</span></span>

### <span data-ttu-id="bafd6-105">ИД (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bafd6-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bafd6-106">Имена</span><span class="sxs-lookup"><span data-stu-id="bafd6-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bafd6-107">Объекты</span><span class="sxs-lookup"><span data-stu-id="bafd6-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bafd6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bafd6-108">DESCRIPTION</span></span>
<span data-ttu-id="bafd6-109">Для создания новой зоны службы доменных имен (DNS) в указанной группе ресурсов будет создаваться новый зоны **New-AzDnsZone.**</span><span class="sxs-lookup"><span data-stu-id="bafd6-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="bafd6-110">Необходимо указать уникальное имя зоны DNS для параметра *Name,* иначе при этом будет возвращена ошибка.</span><span class="sxs-lookup"><span data-stu-id="bafd6-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="bafd6-111">После создания зоны создайте в New-AzDnsRecordSet наборы записей с помощью New-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="bafd6-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="bafd6-112">Параметр Confirm  и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafd6-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="bafd6-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bafd6-113">EXAMPLES</span></span>

### <span data-ttu-id="bafd6-114">Пример 1. Создание зоны DNS</span><span class="sxs-lookup"><span data-stu-id="bafd6-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="bafd6-115">Эта команда создает новую зону DNS myzone.com в указанной группе ресурсов, а затем сохраняет ее в переменной $Zone ресурса.</span><span class="sxs-lookup"><span data-stu-id="bafd6-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="bafd6-116">Пример 2. Создание частной зоны DNS с указанием виртуальных сетевых ID</span><span class="sxs-lookup"><span data-stu-id="bafd6-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="bafd6-117">Эта команда создает новую частную зону DNS с именем myprivatezone.com в указанной группе ресурсов с связанным разрешением виртуальной сети (указывает ее ИД), а затем сохраняет ее в переменной $Zone ресурса.</span><span class="sxs-lookup"><span data-stu-id="bafd6-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="bafd6-118">Пример 3. Создание частной зоны DNS с указанием виртуальных сетевых объектов</span><span class="sxs-lookup"><span data-stu-id="bafd6-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="bafd6-119">Эта команда создает новую частную зону DNS с именем myprivatezone.com в указанной группе ресурсов с связанным разрешением виртуальной сети (на нее ссылается переменная $ResVirtualNetwork), а затем сохраняет ее в переменной $Zone ресурса.</span><span class="sxs-lookup"><span data-stu-id="bafd6-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="bafd6-120">Пример 4. Создание зоны DNS с делегирования путем указания имени родительской зоны</span><span class="sxs-lookup"><span data-stu-id="bafd6-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="bafd6-121">Эта команда создает новую зону DNS ребенка с именем mychild.zone.com в указанной группе ресурсов и сохраняет в переменной $Zone ресурса.</span><span class="sxs-lookup"><span data-stu-id="bafd6-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="bafd6-122">Она также добавляет делегирования в родительскую зону DNS zone.com в той же подписке и группе ресурсов, что и для детей.</span><span class="sxs-lookup"><span data-stu-id="bafd6-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="bafd6-123">Пример 5. Создание зоны DNS с делегирования путем указания родительского зоны</span><span class="sxs-lookup"><span data-stu-id="bafd6-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="bafd6-124">Эта команда создает новую зону DNS ребенка с именем mychild.zone.com в указанной группе ресурсов и сохраняет ее в $Zone переменной.</span><span class="sxs-lookup"><span data-stu-id="bafd6-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="bafd6-125">Она также добавляет делегирования в родительскую зону DNS zone.com в группе ресурсов с другой предоставленной подпиской, то же, что и в созданной зоне для детей.</span><span class="sxs-lookup"><span data-stu-id="bafd6-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="bafd6-126">Пример 6. Создание зоны DNS с делегирования путем указания объекта родительской зоны</span><span class="sxs-lookup"><span data-stu-id="bafd6-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="bafd6-127">Эта команда создает новую зону DNS ребенка с именем mychild.zone.com в указанной группе ресурсов и сохраняет в переменной $Zone ресурса.</span><span class="sxs-lookup"><span data-stu-id="bafd6-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="bafd6-128">Она также добавляет делегирования в родительскую зону DNS zone.com как переданную в объекте ParentZone.</span><span class="sxs-lookup"><span data-stu-id="bafd6-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="bafd6-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bafd6-129">PARAMETERS</span></span>

### <span data-ttu-id="bafd6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafd6-130">-DefaultProfile</span></span>
<span data-ttu-id="bafd6-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bafd6-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bafd6-132">-Name</span><span class="sxs-lookup"><span data-stu-id="bafd6-132">-Name</span></span>
<span data-ttu-id="bafd6-133">Имя зоны DNS, которая будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="bafd6-133">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafd6-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="bafd6-134">-ParentZone</span></span>
<span data-ttu-id="bafd6-135">Полное имя родительской зоны, в который нужно добавить делегирования (без конечной точки).</span><span class="sxs-lookup"><span data-stu-id="bafd6-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafd6-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="bafd6-136">-ParentZoneId</span></span>
<span data-ttu-id="bafd6-137">ИД ресурса родительской зоны для добавления делегирования (без конечной точки).</span><span class="sxs-lookup"><span data-stu-id="bafd6-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafd6-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="bafd6-138">-ParentZoneName</span></span>
<span data-ttu-id="bafd6-139">Полное имя родительской зоны, в который нужно добавить делегирования (без конечной точки).</span><span class="sxs-lookup"><span data-stu-id="bafd6-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafd6-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bafd6-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="bafd6-141">Список виртуальных сетей, которые будут регистрировать записи об имени виртуальных машин в этой зоне DNS, доступен только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="bafd6-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafd6-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="bafd6-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="bafd6-143">Список виртуальных сетевых кодов, которые будут регистрировать записи об именах хостов виртуальных машин в этой зоне DNS, доступен только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="bafd6-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafd6-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bafd6-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="bafd6-145">Список виртуальных сетей для разрешения записей в этой зоне DNS, доступный только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="bafd6-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafd6-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="bafd6-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="bafd6-147">Список виртуальных сетевых ИД, которые можно разрешать записи в этой зоне DNS, доступен только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="bafd6-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafd6-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bafd6-148">-ResourceGroupName</span></span>
<span data-ttu-id="bafd6-149">Определяет группу ресурсов, в которой нужно создать зону.</span><span class="sxs-lookup"><span data-stu-id="bafd6-149">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafd6-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="bafd6-150">-Tag</span></span>
<span data-ttu-id="bafd6-151">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="bafd6-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bafd6-152">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="bafd6-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafd6-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="bafd6-153">-ZoneType</span></span>
<span data-ttu-id="bafd6-154">Тип зоны (общедоступный или закрытый).</span><span class="sxs-lookup"><span data-stu-id="bafd6-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="bafd6-155">Зоны без типа и с типом "Общедоступный" доступны в общедоступных DNS-компаниях, обслуживающих самолет, для использования в иерархии DNS.</span><span class="sxs-lookup"><span data-stu-id="bafd6-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="bafd6-156">Зоны с типом "Частное" видны только в наборе связанных виртуальных сетей (функция предварительной версии).</span><span class="sxs-lookup"><span data-stu-id="bafd6-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="bafd6-157">Это свойство нельзя изменить для зоны.</span><span class="sxs-lookup"><span data-stu-id="bafd6-157">This property cannot be changed for a zone.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafd6-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bafd6-158">-Confirm</span></span>
<span data-ttu-id="bafd6-159">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bafd6-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bafd6-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bafd6-160">-WhatIf</span></span>
<span data-ttu-id="bafd6-161">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafd6-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bafd6-162">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafd6-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bafd6-163">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bafd6-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bafd6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafd6-164">CommonParameters</span></span>
<span data-ttu-id="bafd6-165">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bafd6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafd6-166">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bafd6-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafd6-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bafd6-167">INPUTS</span></span>

### <span data-ttu-id="bafd6-168">System.String</span><span class="sxs-lookup"><span data-stu-id="bafd6-168">System.String</span></span>

### <span data-ttu-id="bafd6-169">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bafd6-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="bafd6-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bafd6-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bafd6-171">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bafd6-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bafd6-172">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bafd6-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="bafd6-173">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bafd6-173">OUTPUTS</span></span>

### <span data-ttu-id="bafd6-174">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="bafd6-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="bafd6-175">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bafd6-175">NOTES</span></span>
<span data-ttu-id="bafd6-176">С помощью параметра *Confirm* (Подтвердить) можно управлять запросом на подтверждение с помощью этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafd6-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="bafd6-177">По умолчанию с помощью cmdlet вы можете получить подтверждение, если переменная $ConfirmPreference Windows PowerShell имеет значение "Средний" или "Ниже".</span><span class="sxs-lookup"><span data-stu-id="bafd6-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="bafd6-178">Если указать *"Подтвердить"* или *"$True:$True",* этот cmdlet запросит подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="bafd6-178">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="bafd6-179">Если *указать confirm:$False,* то при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="bafd6-179">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="bafd6-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bafd6-180">RELATED LINKS</span></span>

[<span data-ttu-id="bafd6-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="bafd6-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="bafd6-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bafd6-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="bafd6-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="bafd6-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
