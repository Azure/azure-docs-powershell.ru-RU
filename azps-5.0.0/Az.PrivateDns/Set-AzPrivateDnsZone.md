---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318899"
---
# <span data-ttu-id="5b628-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5b628-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="5b628-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b628-102">SYNOPSIS</span></span>
<span data-ttu-id="5b628-103">Обновление частной зоны DNS из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b628-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="5b628-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b628-104">SYNTAX</span></span>

### <span data-ttu-id="5b628-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b628-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b628-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b628-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b628-107">DataObject</span><span class="sxs-lookup"><span data-stu-id="5b628-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b628-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b628-108">DESCRIPTION</span></span>
<span data-ttu-id="5b628-109">Командлет **Set-AzPrivateDnsZone** постоянно обновляет закрытую зону доменных имен (DNS) для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b628-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="5b628-110">Вы можете передать объект **PrivateDnsZone** с помощью параметра *PrivateZone* или с помощью оператора конвейера или можно указать параметры *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="5b628-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="5b628-111">Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5b628-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5b628-112">При указании зоны с помощью объекта **PrivateDnsZone** (который передается через конвейер или параметр *зоны* ), зона не обновляется, если она была изменена в Azure DNS с момента получения изменений локального объекта **PrivateDnsZone** (операции с наборами записей в этой зоне не будут возобновляться в соответствии с изменениями.</span><span class="sxs-lookup"><span data-stu-id="5b628-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="5b628-113">Это обеспечивает защиту для одновременных изменений зоны.</span><span class="sxs-lookup"><span data-stu-id="5b628-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="5b628-114">Это может быть подавлено с помощью параметра *overwrite* , который обновляет зону независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="5b628-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="5b628-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b628-115">EXAMPLES</span></span>

### <span data-ttu-id="5b628-116">Пример 1: обновление частной зоны</span><span class="sxs-lookup"><span data-stu-id="5b628-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="5b628-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b628-117">PARAMETERS</span></span>

### <span data-ttu-id="5b628-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b628-118">-DefaultProfile</span></span>
<span data-ttu-id="5b628-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5b628-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b628-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b628-120">-Name</span></span>
<span data-ttu-id="5b628-121">Указывает имя частной DNS-зоны, которая обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5b628-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="5b628-122">Кроме того, необходимо указать параметр *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="5b628-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="5b628-123">Кроме того, вы можете указать частную зону DNS с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="5b628-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b628-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="5b628-124">-Overwrite</span></span>
<span data-ttu-id="5b628-125">При указании зоны с помощью объекта **PrivateDnsZone** (который передается через конвейер или параметр *зоны* ), зона не обновляется, если она была изменена в Azure DNS с момента получения изменений локального объекта **dnsZone** (операции с наборами записей в этой зоне не будут возобновляться в соответствии с изменениями.</span><span class="sxs-lookup"><span data-stu-id="5b628-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="5b628-126">Это обеспечивает защиту для одновременных изменений зоны.</span><span class="sxs-lookup"><span data-stu-id="5b628-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="5b628-127">Это может быть подавлено с помощью параметра *overwrite* , который обновляет зону независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="5b628-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="5b628-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="5b628-128">-PrivateZone</span></span>
<span data-ttu-id="5b628-129">Объект зоны, который нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="5b628-129">The zone object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b628-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b628-130">-ResourceGroupName</span></span>
<span data-ttu-id="5b628-131">Указывает имя группы ресурсов, содержащей зону, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="5b628-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="5b628-132">Кроме того, необходимо указать параметр *zonename* .</span><span class="sxs-lookup"><span data-stu-id="5b628-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="5b628-133">Кроме того, вы можете указать частную DNS-зону с помощью объекта **dnsZone** , передаваемого через конвейер или параметр *Zone* .</span><span class="sxs-lookup"><span data-stu-id="5b628-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b628-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b628-134">-ResourceId</span></span>
<span data-ttu-id="5b628-135">Частный секретный ИД зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="5b628-135">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b628-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="5b628-136">-Tag</span></span>
<span data-ttu-id="5b628-137">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b628-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b628-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b628-138">-Confirm</span></span>
<span data-ttu-id="5b628-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5b628-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b628-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b628-140">-WhatIf</span></span>
<span data-ttu-id="5b628-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5b628-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b628-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5b628-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b628-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b628-143">CommonParameters</span></span>
<span data-ttu-id="5b628-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b628-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b628-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b628-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b628-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b628-146">INPUTS</span></span>

### <span data-ttu-id="5b628-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5b628-147">System.String</span></span>

### <span data-ttu-id="5b628-148">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5b628-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="5b628-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b628-149">OUTPUTS</span></span>

### <span data-ttu-id="5b628-150">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5b628-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="5b628-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b628-151">NOTES</span></span>

## <span data-ttu-id="5b628-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b628-152">RELATED LINKS</span></span>

[<span data-ttu-id="5b628-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5b628-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="5b628-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5b628-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="5b628-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5b628-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
