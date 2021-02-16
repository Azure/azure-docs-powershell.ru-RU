---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213081"
---
# <span data-ttu-id="bb296-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="bb296-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="bb296-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb296-102">SYNOPSIS</span></span>
<span data-ttu-id="bb296-103">Обновляет частную зону DNS из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb296-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="bb296-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bb296-104">SYNTAX</span></span>

### <span data-ttu-id="bb296-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb296-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb296-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb296-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb296-107">Объект</span><span class="sxs-lookup"><span data-stu-id="bb296-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb296-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb296-108">DESCRIPTION</span></span>
<span data-ttu-id="bb296-109">**Cmdlet Set-AzPrivateDnsZone** окончательно обновляет зону частного доменного имени (DNS) из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb296-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="bb296-110">Передать объект **PrivateDnsZone** можно с помощью параметра *PrivateZone* или с помощью оператора конвейера. Кроме того, можно указать параметры *Name* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="bb296-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="bb296-111">Параметр Confirm и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb296-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="bb296-112">При указании зоны с использованием объекта **PrivateDnsZone** (передается через канал или параметр зоны), она не обновляется, если она была изменена в Azure DNS с момента получения локального объекта **PrivateDnsZone** (только операции непосредственно в подсчете ресурсов зоны DNS в качестве изменений, операции с наборами записей в зоне не учитываются). </span><span class="sxs-lookup"><span data-stu-id="bb296-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="bb296-113">Это обеспечивает защиту при одновременном смене зоны.</span><span class="sxs-lookup"><span data-stu-id="bb296-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="bb296-114">Это можно сделать с помощью параметра *Overwrite,* который обновляет зону независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="bb296-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="bb296-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bb296-115">EXAMPLES</span></span>

### <span data-ttu-id="bb296-116">Пример 1. Обновление частной зоны</span><span class="sxs-lookup"><span data-stu-id="bb296-116">Example 1: Updates a private zone</span></span>
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

## <span data-ttu-id="bb296-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb296-117">PARAMETERS</span></span>

### <span data-ttu-id="bb296-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb296-118">-DefaultProfile</span></span>
<span data-ttu-id="bb296-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bb296-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb296-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bb296-120">-Name</span></span>
<span data-ttu-id="bb296-121">Указывает имя зоны частных DNS, которую обновляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb296-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="bb296-122">Необходимо также указать параметр *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="bb296-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="bb296-123">Кроме того, вы можете указать частную зону DNS с помощью *параметра Zone.*</span><span class="sxs-lookup"><span data-stu-id="bb296-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="bb296-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="bb296-124">-Overwrite</span></span>
<span data-ttu-id="bb296-125">При указании зоны с использованием объекта **PrivateDnsZone** (передается через канал или параметр зоны), зона не обновляется, если она была изменена в Azure DNS с момента получения локального объекта **DnsZone** (только операции непосредственно в подсчете ресурсов зоны DNS в качестве изменений, операции с наборами записей в зоне не учитываются). </span><span class="sxs-lookup"><span data-stu-id="bb296-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="bb296-126">Это обеспечивает защиту при одновременном смене зоны.</span><span class="sxs-lookup"><span data-stu-id="bb296-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="bb296-127">Это можно сделать с помощью параметра *Overwrite,* который обновляет зону независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="bb296-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="bb296-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="bb296-128">-PrivateZone</span></span>
<span data-ttu-id="bb296-129">Объект зоны, который нужно установить.</span><span class="sxs-lookup"><span data-stu-id="bb296-129">The zone object to set.</span></span>

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

### <span data-ttu-id="bb296-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb296-130">-ResourceGroupName</span></span>
<span data-ttu-id="bb296-131">Имя группы ресурсов, которая содержит обновляемую зону.</span><span class="sxs-lookup"><span data-stu-id="bb296-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="bb296-132">Необходимо также указать *параметр ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="bb296-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="bb296-133">Кроме того, вы можете указать частную зону DNS с помощью объекта **DnsZone,** переданного через канал или параметр *Zone.*</span><span class="sxs-lookup"><span data-stu-id="bb296-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="bb296-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb296-134">-ResourceId</span></span>
<span data-ttu-id="bb296-135">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="bb296-135">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="bb296-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="bb296-136">-Tag</span></span>
<span data-ttu-id="bb296-137">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="bb296-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="bb296-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb296-138">-Confirm</span></span>
<span data-ttu-id="bb296-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb296-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb296-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb296-140">-WhatIf</span></span>
<span data-ttu-id="bb296-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb296-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb296-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bb296-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb296-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb296-143">CommonParameters</span></span>
<span data-ttu-id="bb296-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb296-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb296-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb296-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb296-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb296-146">INPUTS</span></span>

### <span data-ttu-id="bb296-147">System.String</span><span class="sxs-lookup"><span data-stu-id="bb296-147">System.String</span></span>

### <span data-ttu-id="bb296-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="bb296-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="bb296-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bb296-149">OUTPUTS</span></span>

### <span data-ttu-id="bb296-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="bb296-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="bb296-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bb296-151">NOTES</span></span>

## <span data-ttu-id="bb296-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb296-152">RELATED LINKS</span></span>

[<span data-ttu-id="bb296-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="bb296-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="bb296-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="bb296-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="bb296-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="bb296-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
