---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403596"
---
# <span data-ttu-id="1cec2-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1cec2-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="1cec2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cec2-102">SYNOPSIS</span></span>
<span data-ttu-id="1cec2-103">Удаляет частную зону DNS из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1cec2-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="1cec2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1cec2-104">SYNTAX</span></span>

### <span data-ttu-id="1cec2-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1cec2-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cec2-106">Объект</span><span class="sxs-lookup"><span data-stu-id="1cec2-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cec2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cec2-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cec2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cec2-108">DESCRIPTION</span></span>
<span data-ttu-id="1cec2-109">**Cmdlet Remove-AzPrivateDnsZone** окончательно удаляет частную зону службы доменных имен (DNS) из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1cec2-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="1cec2-110">Все наборы записей, содержащиеся в зоне, также удаляются.</span><span class="sxs-lookup"><span data-stu-id="1cec2-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="1cec2-111">Передать объект **PrivateDnsZone** можно с помощью параметра *PrivateZone* или с помощью оператора конвейера. Кроме того, можно указать параметры *Name* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="1cec2-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1cec2-112">С помощью переменных Confirm и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cec2-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1cec2-113">При указании зоны с использованием объекта **PrivateDnsZone** (передается через канал или параметр зоны), она не удаляется, если она была изменена в Azure DNS после извлечения локального объекта **PrivateDnsZone** (только операции непосредственно в подсчете ресурсов зоны DNS в качестве изменений, операции с наборами записей в зоне не учитываются). </span><span class="sxs-lookup"><span data-stu-id="1cec2-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="1cec2-114">Это обеспечивает защиту при одновременном смене зоны.</span><span class="sxs-lookup"><span data-stu-id="1cec2-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="1cec2-115">Это можно сделать с помощью параметра *Overwrite,* который удаляет зону независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="1cec2-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="1cec2-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1cec2-116">EXAMPLES</span></span>

### <span data-ttu-id="1cec2-117">Пример 1. Удаление закрытой зоны</span><span class="sxs-lookup"><span data-stu-id="1cec2-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="1cec2-118">Эта команда удаляет зону с именем myzone.com из группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1cec2-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="1cec2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cec2-119">PARAMETERS</span></span>

### <span data-ttu-id="1cec2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cec2-120">-DefaultProfile</span></span>
<span data-ttu-id="1cec2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1cec2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cec2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1cec2-122">-Name</span></span>
<span data-ttu-id="1cec2-123">Указывает имя закрытой зоны DNS, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cec2-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="1cec2-124">Необходимо также указать параметр *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="1cec2-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="1cec2-125">Кроме того, вы можете указать зону DNS с помощью *параметра Zone.*</span><span class="sxs-lookup"><span data-stu-id="1cec2-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="1cec2-126">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="1cec2-126">-Overwrite</span></span>
<span data-ttu-id="1cec2-127">При указании зоны с использованием объекта **PrivateDnsZone** (передается через канал или параметр зоны), она не удаляется, если она была изменена в Azure DNS после извлечения локального объекта **PrivateDnsZone** (только операции непосредственно в подсчете ресурсов зоны DNS в качестве изменений, операции с наборами записей в зоне не учитываются). </span><span class="sxs-lookup"><span data-stu-id="1cec2-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="1cec2-128">Это обеспечивает защиту при одновременном смене зоны.</span><span class="sxs-lookup"><span data-stu-id="1cec2-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="1cec2-129">Это можно сделать с помощью параметра *Overwrite,* который удаляет зону независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="1cec2-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="1cec2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cec2-130">-PassThru</span></span>
<span data-ttu-id="1cec2-131">Используется для передачи результата (boolean) операции удаления частной зоны далее по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="1cec2-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="1cec2-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="1cec2-132">-PrivateZone</span></span>
<span data-ttu-id="1cec2-133">Объект закрытой зоны, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1cec2-133">The private zone object to delete.</span></span>

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

### <span data-ttu-id="1cec2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cec2-134">-ResourceGroupName</span></span>
<span data-ttu-id="1cec2-135">Имя группы ресурсов, которая содержит удаляемую зону.</span><span class="sxs-lookup"><span data-stu-id="1cec2-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="1cec2-136">Необходимо также указать *параметр ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="1cec2-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="1cec2-137">Кроме того, вы можете указать зону DNS с помощью объекта **PrivateDnsZone,** переданного через канал или параметр *зоны.*</span><span class="sxs-lookup"><span data-stu-id="1cec2-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="1cec2-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cec2-138">-ResourceId</span></span>
<span data-ttu-id="1cec2-139">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="1cec2-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="1cec2-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cec2-140">-Confirm</span></span>
<span data-ttu-id="1cec2-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cec2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cec2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cec2-142">-WhatIf</span></span>
<span data-ttu-id="1cec2-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cec2-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cec2-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1cec2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cec2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cec2-145">CommonParameters</span></span>
<span data-ttu-id="1cec2-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cec2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cec2-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cec2-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cec2-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1cec2-148">INPUTS</span></span>

### <span data-ttu-id="1cec2-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1cec2-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="1cec2-150">System.String</span><span class="sxs-lookup"><span data-stu-id="1cec2-150">System.String</span></span>

## <span data-ttu-id="1cec2-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1cec2-151">OUTPUTS</span></span>

### <span data-ttu-id="1cec2-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1cec2-152">System.Boolean</span></span>

## <span data-ttu-id="1cec2-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1cec2-153">NOTES</span></span>

## <span data-ttu-id="1cec2-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cec2-154">RELATED LINKS</span></span>

[<span data-ttu-id="1cec2-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1cec2-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="1cec2-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1cec2-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="1cec2-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1cec2-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
