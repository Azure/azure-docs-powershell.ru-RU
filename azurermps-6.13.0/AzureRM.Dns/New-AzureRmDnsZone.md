---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: ed438e3e649d26db5b0da85b833794ad1872fa9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565452"
---
# <span data-ttu-id="2d7cf-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2d7cf-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="2d7cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7cf-103">Создание новой зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d7cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d7cf-104">SYNTAX</span></span>

### <span data-ttu-id="2d7cf-105">Идентификаторы (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d7cf-105">Ids (Default)</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7cf-106">Object</span><span class="sxs-lookup"><span data-stu-id="2d7cf-106">Objects</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d7cf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d7cf-107">DESCRIPTION</span></span>
<span data-ttu-id="2d7cf-108">Командлет **New-AzureRmDnsZone** создает новую зону DNS (Domain Name System) в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-108">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="2d7cf-109">Необходимо указать уникальное имя зоны DNS для параметра *Name* , иначе командлет будет возвращать ошибку.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="2d7cf-110">После создания зоны используйте командлет New-AzureRmDnsRecordSet для создания наборов записей в зоне.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-110">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="2d7cf-111">Вы можете использовать параметр *Confirm* и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="2d7cf-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d7cf-112">EXAMPLES</span></span>

### <span data-ttu-id="2d7cf-113">Пример 1: создание зоны DNS</span><span class="sxs-lookup"><span data-stu-id="2d7cf-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2d7cf-114">Эта команда создает новую зону DNS с именем myzone.com в заданной группе ресурсов, а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="2d7cf-115">Пример 2: создание частной зоны DNS путем указания идентификаторов виртуальных сетей</span><span class="sxs-lookup"><span data-stu-id="2d7cf-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="2d7cf-116">Эта команда создает новую зону DNS с именем myprivatezone.com в заданной группе ресурсов с помощью связанной виртуальной сети разрешения (с указанием ее идентификатора), а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="2d7cf-117">Пример 3: создание частной зоны DNS путем указания объектов виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="2d7cf-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzureRmVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="2d7cf-118">Эта команда создает новую зону DNS с именем myprivatezone.com в заданной группе ресурсов с соответствующей виртуальной сетью разрешения (на которую указывает переменная $ResVirtualNetwork), а затем сохраняет ее в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="2d7cf-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d7cf-119">PARAMETERS</span></span>

### <span data-ttu-id="2d7cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7cf-120">-DefaultProfile</span></span>
<span data-ttu-id="2d7cf-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2d7cf-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d7cf-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d7cf-122">-Name</span></span>
<span data-ttu-id="2d7cf-123">Указывает имя зоны DNS, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-123">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="2d7cf-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2d7cf-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="2d7cf-125">Список виртуальных сетей, которые будут регистрировать записи hostname для виртуальных машин в этой зоне DNS, доступны только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="2d7cf-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2d7cf-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="2d7cf-127">Список идентификаторов виртуальных сетей, которые будут регистрировать записи hostname для виртуальных машин в этой зоне DNS, только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="2d7cf-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2d7cf-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="2d7cf-129">Список виртуальных сетей, которые можно использовать для разрешения записей в этой зоне DNS, только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="2d7cf-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2d7cf-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="2d7cf-131">Список идентификаторов виртуальных сетей, которые можно использовать для разрешения записей в этой зоне DNS, только для частных зон.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="2d7cf-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7cf-132">-ResourceGroupName</span></span>
<span data-ttu-id="2d7cf-133">Указывает группу ресурсов, в которой нужно создать зону.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-133">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="2d7cf-134">-Тег</span><span class="sxs-lookup"><span data-stu-id="2d7cf-134">-Tag</span></span>
<span data-ttu-id="2d7cf-135">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2d7cf-136">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2d7cf-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2d7cf-137">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="2d7cf-137">-ZoneType</span></span>
<span data-ttu-id="2d7cf-138">Тип зоны (Public или private).</span><span class="sxs-lookup"><span data-stu-id="2d7cf-138">The type of the zone, Public or Private.</span></span> <span data-ttu-id="2d7cf-139">Зоны, для которых не задан тип или тип общедоступной, становятся доступными на общедоступной плоскости DNS-обслуживания, используемой в иерархии DNS.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-139">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="2d7cf-140">Зоны с типом "частный" отображаются только в наборе связанных виртуальных сетей (Эта функция доступна в предварительной версии).</span><span class="sxs-lookup"><span data-stu-id="2d7cf-140">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="2d7cf-141">Это свойство не может быть изменено для зоны.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-141">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="2d7cf-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d7cf-142">-Confirm</span></span>
<span data-ttu-id="2d7cf-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d7cf-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d7cf-144">-WhatIf</span></span>
<span data-ttu-id="2d7cf-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d7cf-146">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d7cf-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d7cf-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7cf-148">CommonParameters</span></span>
<span data-ttu-id="2d7cf-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7cf-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d7cf-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7cf-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d7cf-151">INPUTS</span></span>

### <span data-ttu-id="2d7cf-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2d7cf-152">System.String</span></span>

### <span data-ttu-id="2d7cf-153">System. Nullable "1 [[Microsoft. Azure. Management. DNS. Models. ZoneType, Microsoft. Azure. Management. DNS, Version = 2.1.0.0, культура = нейтральная, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2d7cf-153">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=2.1.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2d7cf-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d7cf-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2d7cf-155">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2d7cf-155">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2d7cf-156">System. Collections. Generic. List "1 [[Microsoft. Azure. Management. internal. Network. Common. IResourceReference, Microsoft. Azure. System. Common. Network, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="2d7cf-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.Commands.Common.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2d7cf-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d7cf-157">OUTPUTS</span></span>

### <span data-ttu-id="2d7cf-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="2d7cf-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="2d7cf-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d7cf-159">NOTES</span></span>
<span data-ttu-id="2d7cf-160">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-160">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2d7cf-161">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-161">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="2d7cf-162">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-162">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="2d7cf-163">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2d7cf-163">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2d7cf-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d7cf-164">RELATED LINKS</span></span>

[<span data-ttu-id="2d7cf-165">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2d7cf-165">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="2d7cf-166">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2d7cf-166">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="2d7cf-167">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2d7cf-167">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
