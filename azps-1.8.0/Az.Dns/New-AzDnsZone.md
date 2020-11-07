---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: eb7a2f3494521a5505db0224bb1ae0ff948d406f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730891"
---
# <span data-ttu-id="4abb5-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="4abb5-101">New-AzDnsZone</span></span>

## <span data-ttu-id="4abb5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4abb5-102">SYNOPSIS</span></span>
<span data-ttu-id="4abb5-103">Создание новой зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="4abb5-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="4abb5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4abb5-104">SYNTAX</span></span>

### <span data-ttu-id="4abb5-105">Идентификаторы (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4abb5-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4abb5-106">Object</span><span class="sxs-lookup"><span data-stu-id="4abb5-106">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4abb5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4abb5-107">DESCRIPTION</span></span>
<span data-ttu-id="4abb5-108">Командлет **New-AzDnsZone** создает новую зону DNS (Domain Name System) в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4abb5-108">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="4abb5-109">Необходимо указать уникальное имя зоны DNS для параметра *Name* , иначе командлет будет возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="4abb5-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="4abb5-110">После создания зоны используйте командлет New-AzDnsRecordSet для создания наборов записей в зоне.</span><span class="sxs-lookup"><span data-stu-id="4abb5-110">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="4abb5-111">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4abb5-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="4abb5-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4abb5-112">EXAMPLES</span></span>

### <span data-ttu-id="4abb5-113">Пример 1: создание зоны DNS</span><span class="sxs-lookup"><span data-stu-id="4abb5-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="4abb5-114">Эта команда создает новую зону DNS с именем myzone.com в заданной группе ресурсов, а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="4abb5-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="4abb5-115">Пример 2: создание частной зоны DNS путем указания идентификаторов виртуальных сетей</span><span class="sxs-lookup"><span data-stu-id="4abb5-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="4abb5-116">Эта команда создает новую зону DNS с именем myprivatezone.com в заданной группе ресурсов с помощью связанной виртуальной сети разрешения (с указанием ее идентификатора), а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="4abb5-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="4abb5-117">Пример 3: создание частной зоны DNS путем указания объектов виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="4abb5-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="4abb5-118">Эта команда создает новую зону DNS с именем myprivatezone.com в заданной группе ресурсов с соответствующей виртуальной сетью разрешения (на которую указывает переменная $ResVirtualNetwork), а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="4abb5-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="4abb5-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4abb5-119">PARAMETERS</span></span>

### <span data-ttu-id="4abb5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abb5-120">-DefaultProfile</span></span>
<span data-ttu-id="4abb5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4abb5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4abb5-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4abb5-122">-Name</span></span>
<span data-ttu-id="4abb5-123">Указывает имя зоны DNS, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="4abb5-123">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="4abb5-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4abb5-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="4abb5-125">Список виртуальных сетей, которые будут регистрировать записи hostname для виртуальных машин в этой зоне DNS, доступны только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="4abb5-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="4abb5-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="4abb5-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="4abb5-127">Список идентификаторов виртуальных сетей, которые будут регистрировать записи hostname для виртуальных машин в этой зоне DNS, только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="4abb5-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="4abb5-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4abb5-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="4abb5-129">Список виртуальных сетей, которые можно использовать для разрешения записей в этой зоне DNS, только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="4abb5-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="4abb5-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="4abb5-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="4abb5-131">Список идентификаторов виртуальных сетей, которые можно использовать для разрешения записей в этой зоне DNS, только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="4abb5-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="4abb5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4abb5-132">-ResourceGroupName</span></span>
<span data-ttu-id="4abb5-133">Указывает группу ресурсов, в которой нужно создать зону.</span><span class="sxs-lookup"><span data-stu-id="4abb5-133">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="4abb5-134">-Тег</span><span class="sxs-lookup"><span data-stu-id="4abb5-134">-Tag</span></span>
<span data-ttu-id="4abb5-135">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="4abb5-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4abb5-136">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="4abb5-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4abb5-137">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="4abb5-137">-ZoneType</span></span>
<span data-ttu-id="4abb5-138">Тип зоны (Public или private).</span><span class="sxs-lookup"><span data-stu-id="4abb5-138">The type of the zone, Public or Private.</span></span> <span data-ttu-id="4abb5-139">Зоны, для которых не задан тип или тип общедоступной, становятся доступными на общедоступной плоскости DNS-обслуживания, используемой в иерархии DNS.</span><span class="sxs-lookup"><span data-stu-id="4abb5-139">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="4abb5-140">Зоны с типом "частный" отображаются только в наборе связанных виртуальных сетей (Эта функция доступна в предварительной версии).</span><span class="sxs-lookup"><span data-stu-id="4abb5-140">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="4abb5-141">Это свойство не может быть изменено для зоны.</span><span class="sxs-lookup"><span data-stu-id="4abb5-141">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="4abb5-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4abb5-142">-Confirm</span></span>
<span data-ttu-id="4abb5-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4abb5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4abb5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4abb5-144">-WhatIf</span></span>
<span data-ttu-id="4abb5-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4abb5-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4abb5-146">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4abb5-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4abb5-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4abb5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4abb5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abb5-148">CommonParameters</span></span>
<span data-ttu-id="4abb5-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4abb5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abb5-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4abb5-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abb5-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4abb5-151">INPUTS</span></span>

### <span data-ttu-id="4abb5-152">System. String</span><span class="sxs-lookup"><span data-stu-id="4abb5-152">System.String</span></span>

### <span data-ttu-id="4abb5-153">System. Nullable "1 [[Microsoft. Azure. Management. DNS. Models. ZoneType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, культура = нейтральная, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4abb5-153">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="4abb5-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4abb5-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4abb5-155">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4abb5-155">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4abb5-156">System. Collections. Generic. List "1 [[Microsoft. Azure. Management. internal. Network. Common. IResourceReference, Microsoft. Azure. Windows. Clients. Network, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4abb5-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="4abb5-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4abb5-157">OUTPUTS</span></span>

### <span data-ttu-id="4abb5-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="4abb5-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="4abb5-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="4abb5-159">NOTES</span></span>
<span data-ttu-id="4abb5-160">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4abb5-160">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4abb5-161">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="4abb5-161">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="4abb5-162">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="4abb5-162">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="4abb5-163">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4abb5-163">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4abb5-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4abb5-164">RELATED LINKS</span></span>

[<span data-ttu-id="4abb5-165">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="4abb5-165">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="4abb5-166">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4abb5-166">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="4abb5-167">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="4abb5-167">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
