---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247473"
---
# <span data-ttu-id="a5a60-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a5a60-101">New-AzDnsZone</span></span>

## <span data-ttu-id="a5a60-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5a60-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a60-103">Создание новой зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="a5a60-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="a5a60-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5a60-104">SYNTAX</span></span>

### <span data-ttu-id="a5a60-105">Идентификаторы (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5a60-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a60-106">Названия</span><span class="sxs-lookup"><span data-stu-id="a5a60-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a60-107">Object</span><span class="sxs-lookup"><span data-stu-id="a5a60-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5a60-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5a60-108">DESCRIPTION</span></span>
<span data-ttu-id="a5a60-109">Командлет **New-AzDnsZone** создает новую зону DNS (Domain Name System) в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a5a60-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="a5a60-110">Необходимо указать уникальное имя зоны DNS для параметра *Name* , иначе командлет будет возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="a5a60-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="a5a60-111">После создания зоны используйте командлет New-AzDnsRecordSet для создания наборов записей в зоне.</span><span class="sxs-lookup"><span data-stu-id="a5a60-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="a5a60-112">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a5a60-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="a5a60-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5a60-113">EXAMPLES</span></span>

### <span data-ttu-id="a5a60-114">Пример 1: создание зоны DNS</span><span class="sxs-lookup"><span data-stu-id="a5a60-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a5a60-115">Эта команда создает новую зону DNS с именем myzone.com в заданной группе ресурсов, а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="a5a60-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="a5a60-116">Пример 2: создание частной зоны DNS путем указания идентификаторов виртуальных сетей</span><span class="sxs-lookup"><span data-stu-id="a5a60-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="a5a60-117">Эта команда создает новую зону DNS с именем myprivatezone.com в заданной группе ресурсов с помощью связанной виртуальной сети разрешения (с указанием ее идентификатора), а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="a5a60-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="a5a60-118">Пример 3: создание частной зоны DNS путем указания объектов виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a5a60-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="a5a60-119">Эта команда создает новую зону DNS с именем myprivatezone.com в заданной группе ресурсов с соответствующей виртуальной сетью разрешения (на которую указывает переменная $ResVirtualNetwork), а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="a5a60-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="a5a60-120">Пример 4: создание зоны DNS с делегированием с указанием имени родительской зоны</span><span class="sxs-lookup"><span data-stu-id="a5a60-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="a5a60-121">Эта команда создает новую дочернюю зону DNS с именем mychild.zone.com в указанной группе ресурсов и сохраняет в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="a5a60-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="a5a60-122">Она также добавляет делегирование в родительской зоне DNS с именем zone.com, находящейся в той же подписке и группе ресурсов, что и дочерняя зона.</span><span class="sxs-lookup"><span data-stu-id="a5a60-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="a5a60-123">Пример 5: создание зоны DNS с делегированием с указанием идентификатора родительской зоны</span><span class="sxs-lookup"><span data-stu-id="a5a60-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="a5a60-124">Эта команда создает новую дочернюю зону DNS с именем mychild.zone.com в указанной группе ресурсов и сохраняет в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="a5a60-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="a5a60-125">Кроме того, он добавляет делегирование в родительской зоне DNS с именем zone.com в группе ресурсов "другие-RG", а также в том случае, если создана подписку для дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="a5a60-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="a5a60-126">Пример 6: создание зоны DNS с делегированием путем задания родительского объекта зоны</span><span class="sxs-lookup"><span data-stu-id="a5a60-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="a5a60-127">Эта команда создает новую дочернюю зону DNS с именем mychild.zone.com в указанной группе ресурсов и сохраняет в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="a5a60-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="a5a60-128">Она также добавляет делегирование в родительской зоне DNS под названием zone.com, как оно передается в объекте ParentZone.</span><span class="sxs-lookup"><span data-stu-id="a5a60-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="a5a60-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5a60-129">PARAMETERS</span></span>

### <span data-ttu-id="a5a60-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a60-130">-DefaultProfile</span></span>
<span data-ttu-id="a5a60-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a5a60-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5a60-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a5a60-132">-Name</span></span>
<span data-ttu-id="a5a60-133">Указывает имя зоны DNS, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="a5a60-133">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="a5a60-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="a5a60-134">-ParentZone</span></span>
<span data-ttu-id="a5a60-135">Полное имя родительской зоны для добавления делегирования (без точки завершения).</span><span class="sxs-lookup"><span data-stu-id="a5a60-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="a5a60-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="a5a60-136">-ParentZoneId</span></span>
<span data-ttu-id="a5a60-137">Идентификатор ресурса родительской зоны для добавления делегирования (без точки завершения).</span><span class="sxs-lookup"><span data-stu-id="a5a60-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="a5a60-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="a5a60-138">-ParentZoneName</span></span>
<span data-ttu-id="a5a60-139">Полное имя родительской зоны для добавления делегирования (без точки завершения).</span><span class="sxs-lookup"><span data-stu-id="a5a60-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="a5a60-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a5a60-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="a5a60-141">Список виртуальных сетей, которые будут регистрировать записи hostname для виртуальных машин в этой зоне DNS, доступны только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="a5a60-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="a5a60-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="a5a60-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="a5a60-143">Список идентификаторов виртуальных сетей, которые будут регистрировать записи hostname для виртуальных машин в этой зоне DNS, только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="a5a60-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="a5a60-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a5a60-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="a5a60-145">Список виртуальных сетей, которые можно использовать для разрешения записей в этой зоне DNS, только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="a5a60-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="a5a60-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="a5a60-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="a5a60-147">Список идентификаторов виртуальных сетей, которые можно использовать для разрешения записей в этой зоне DNS, только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="a5a60-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="a5a60-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a60-148">-ResourceGroupName</span></span>
<span data-ttu-id="a5a60-149">Указывает группу ресурсов, в которой нужно создать зону.</span><span class="sxs-lookup"><span data-stu-id="a5a60-149">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="a5a60-150">-Тег</span><span class="sxs-lookup"><span data-stu-id="a5a60-150">-Tag</span></span>
<span data-ttu-id="a5a60-151">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="a5a60-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a5a60-152">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="a5a60-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a5a60-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="a5a60-153">-ZoneType</span></span>
<span data-ttu-id="a5a60-154">Тип зоны (Public или private).</span><span class="sxs-lookup"><span data-stu-id="a5a60-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="a5a60-155">Зоны, для которых не задан тип или тип общедоступной, становятся доступными на общедоступной плоскости DNS-обслуживания, используемой в иерархии DNS.</span><span class="sxs-lookup"><span data-stu-id="a5a60-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="a5a60-156">Зоны с типом "частный" отображаются только в наборе связанных виртуальных сетей (Эта функция доступна в предварительной версии).</span><span class="sxs-lookup"><span data-stu-id="a5a60-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="a5a60-157">Это свойство не может быть изменено для зоны.</span><span class="sxs-lookup"><span data-stu-id="a5a60-157">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="a5a60-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5a60-158">-Confirm</span></span>
<span data-ttu-id="a5a60-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a5a60-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5a60-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a60-160">-WhatIf</span></span>
<span data-ttu-id="a5a60-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a5a60-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5a60-162">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a5a60-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5a60-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a5a60-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5a60-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a60-164">CommonParameters</span></span>
<span data-ttu-id="a5a60-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5a60-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a60-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a60-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a60-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5a60-167">INPUTS</span></span>

### <span data-ttu-id="a5a60-168">System. String</span><span class="sxs-lookup"><span data-stu-id="a5a60-168">System.String</span></span>

### <span data-ttu-id="a5a60-169">System. Nullable "1 [[Microsoft. Azure. Management. DNS. Models. ZoneType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, культура = нейтральная, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a5a60-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a5a60-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a5a60-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a5a60-171">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a5a60-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a5a60-172">System. Collections. Generic. List "1 [[Microsoft. Azure. Management. internal. Network. Common. IResourceReference, Microsoft. Azure. Windows. Clients. Network, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a5a60-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a5a60-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5a60-173">OUTPUTS</span></span>

### <span data-ttu-id="a5a60-174">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a5a60-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="a5a60-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5a60-175">NOTES</span></span>
<span data-ttu-id="a5a60-176">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a5a60-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="a5a60-177">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="a5a60-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="a5a60-178">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="a5a60-178">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="a5a60-179">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a5a60-179">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a5a60-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5a60-180">RELATED LINKS</span></span>

[<span data-ttu-id="a5a60-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a5a60-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="a5a60-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a5a60-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="a5a60-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="a5a60-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)