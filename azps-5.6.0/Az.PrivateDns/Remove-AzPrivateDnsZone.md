---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: 8c8e7059a6c23c928180b8d6fab3cfdbbfd9ed5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970408"
---
# <span data-ttu-id="1b47c-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1b47c-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="1b47c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b47c-102">SYNOPSIS</span></span>
<span data-ttu-id="1b47c-103">Удаляет частную зону DNS из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b47c-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="1b47c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b47c-104">SYNTAX</span></span>

### <span data-ttu-id="1b47c-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b47c-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b47c-106">Объект</span><span class="sxs-lookup"><span data-stu-id="1b47c-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b47c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b47c-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b47c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b47c-108">DESCRIPTION</span></span>
<span data-ttu-id="1b47c-109">**Cmdlet Remove-AzPrivateDnsZone** окончательно удаляет частную зону службы доменных имен (DNS) из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b47c-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="1b47c-110">Все наборы записей, содержащиеся в зоне, также удаляются.</span><span class="sxs-lookup"><span data-stu-id="1b47c-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="1b47c-111">Передать объект **PrivateDnsZone** можно с помощью параметра *PrivateZone* или с помощью оператора конвейера. Кроме того, можно указать параметры *Name* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="1b47c-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1b47c-112">Параметр Confirm и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b47c-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1b47c-113">При указании зоны с использованием объекта **PrivateDnsZone** (передается через канал или параметр зоны), она не удаляется, если она была изменена в Azure DNS после извлечения локального объекта **PrivateDnsZone** (только операции непосредственно в подсчете ресурсов зоны DNS в качестве изменений, операции с наборами записей в зоне не учитываются). </span><span class="sxs-lookup"><span data-stu-id="1b47c-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="1b47c-114">Это обеспечивает защиту при одновременном смене зоны.</span><span class="sxs-lookup"><span data-stu-id="1b47c-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="1b47c-115">Это можно сделать с помощью параметра *Overwrite,* который удаляет зону независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="1b47c-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="1b47c-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b47c-116">EXAMPLES</span></span>

### <span data-ttu-id="1b47c-117">Пример 1. Удаление закрытой зоны</span><span class="sxs-lookup"><span data-stu-id="1b47c-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="1b47c-118">Эта команда удаляет зону с именем myzone.com из группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1b47c-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="1b47c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b47c-119">PARAMETERS</span></span>

### <span data-ttu-id="1b47c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b47c-120">-DefaultProfile</span></span>
<span data-ttu-id="1b47c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1b47c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b47c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1b47c-122">-Name</span></span>
<span data-ttu-id="1b47c-123">Указывает имя закрытой зоны DNS, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b47c-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="1b47c-124">Необходимо также указать параметр *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="1b47c-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="1b47c-125">Кроме того, вы можете указать зону DNS с помощью *параметра Zone.*</span><span class="sxs-lookup"><span data-stu-id="1b47c-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="1b47c-126">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="1b47c-126">-Overwrite</span></span>
<span data-ttu-id="1b47c-127">При указании зоны с использованием объекта **PrivateDnsZone** (передается через канал или параметр зоны), она не удаляется, если она была изменена в Azure DNS с момента извлечения локального объекта **PrivateDnsZone** (только операции непосредственно в подсчете ресурсов зоны DNS в качестве изменений, операции с наборами записей в зоне не учитываются). </span><span class="sxs-lookup"><span data-stu-id="1b47c-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="1b47c-128">Это обеспечивает защиту при одновременном смене зоны.</span><span class="sxs-lookup"><span data-stu-id="1b47c-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="1b47c-129">Это можно сделать с помощью параметра *Overwrite,* который удаляет зону независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="1b47c-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="1b47c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b47c-130">-PassThru</span></span>
<span data-ttu-id="1b47c-131">Используется для передачи результата (boolean) операции удаления частной зоны далее по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="1b47c-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b47c-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="1b47c-132">-PrivateZone</span></span>
<span data-ttu-id="1b47c-133">Объект закрытой зоны, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1b47c-133">The private zone object to delete.</span></span>

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

### <span data-ttu-id="1b47c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b47c-134">-ResourceGroupName</span></span>
<span data-ttu-id="1b47c-135">Имя группы ресурсов, которая содержит удаляемую зону.</span><span class="sxs-lookup"><span data-stu-id="1b47c-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="1b47c-136">Необходимо также указать *параметр ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="1b47c-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="1b47c-137">Кроме того, вы можете указать зону DNS с помощью объекта **PrivateDnsZone,** переданного через канал или параметр *зоны.*</span><span class="sxs-lookup"><span data-stu-id="1b47c-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="1b47c-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b47c-138">-ResourceId</span></span>
<span data-ttu-id="1b47c-139">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="1b47c-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="1b47c-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b47c-140">-Confirm</span></span>
<span data-ttu-id="1b47c-141">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1b47c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b47c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b47c-142">-WhatIf</span></span>
<span data-ttu-id="1b47c-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b47c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b47c-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1b47c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b47c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b47c-145">CommonParameters</span></span>
<span data-ttu-id="1b47c-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b47c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b47c-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b47c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b47c-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b47c-148">INPUTS</span></span>

### <span data-ttu-id="1b47c-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1b47c-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="1b47c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="1b47c-150">System.String</span></span>

## <span data-ttu-id="1b47c-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b47c-151">OUTPUTS</span></span>

### <span data-ttu-id="1b47c-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1b47c-152">System.Boolean</span></span>

## <span data-ttu-id="1b47c-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b47c-153">NOTES</span></span>

## <span data-ttu-id="1b47c-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b47c-154">RELATED LINKS</span></span>

[<span data-ttu-id="1b47c-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1b47c-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="1b47c-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1b47c-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="1b47c-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1b47c-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
