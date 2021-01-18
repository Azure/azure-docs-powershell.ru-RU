---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505436"
---
# <span data-ttu-id="5ed6b-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5ed6b-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="5ed6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ed6b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed6b-103">Удаляет виртуальную сетевую связь из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="5ed6b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ed6b-104">SYNTAX</span></span>

### <span data-ttu-id="5ed6b-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ed6b-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ed6b-106">Объект</span><span class="sxs-lookup"><span data-stu-id="5ed6b-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ed6b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ed6b-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ed6b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ed6b-108">DESCRIPTION</span></span>
<span data-ttu-id="5ed6b-109">Командлет **Remove-AzPrivateDnsVirtualNetworkLink** окончательно удаляет частную ссылку на службу доменных имен (DNS) из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="5ed6b-110">Объект **PSPrivateDnsVirtualNetworkLink** можно передать с помощью параметра *Link* или с помощью оператора конвейера. Кроме того, можно указать параметры *Name* *ZoneName* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="5ed6b-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="5ed6b-111">С помощью переменных Confirm и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5ed6b-112">При указании ссылки с помощью объекта **PSPrivateDnsVirtualNetworkLink** (передается через параметр pipeline или *Link),* ссылка не удаляется, если она была изменена в личных DNS Azure после извлечения локального объекта **PSPrivateDnsVirtualNetworkLink.**</span><span class="sxs-lookup"><span data-stu-id="5ed6b-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="5ed6b-113">Это обеспечивает защиту при одновременном смене зоны.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="5ed6b-114">Это можно сделать с помощью параметра *Overwrite,* который удаляет зону независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="5ed6b-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ed6b-115">EXAMPLES</span></span>

### <span data-ttu-id="5ed6b-116">Пример 1. Удаление ссылки</span><span class="sxs-lookup"><span data-stu-id="5ed6b-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="5ed6b-117">Эта команда удаляет ссылку mylink, связанную с myzone.com зоны, из группы ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="5ed6b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ed6b-118">PARAMETERS</span></span>

### <span data-ttu-id="5ed6b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed6b-119">-DefaultProfile</span></span>
<span data-ttu-id="5ed6b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ed6b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ed6b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ed6b-121">-InputObject</span></span>
<span data-ttu-id="5ed6b-122">Объект виртуальной сетевой связи, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-122">The virtual network link object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed6b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5ed6b-123">-Name</span></span>
<span data-ttu-id="5ed6b-124">Указывает имя удаляемой ссылки.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="5ed6b-125">Необходимо также указать параметр *ResourceGroupName* и *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="5ed6b-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="5ed6b-126">Ссылку также можно указать с помощью *параметра Link.*</span><span class="sxs-lookup"><span data-stu-id="5ed6b-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="5ed6b-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="5ed6b-127">-Overwrite</span></span>
<span data-ttu-id="5ed6b-128">При указании зоны с помощью объекта **PSPrivateDnsVirtualNetworkLink** (передается через параметр pipeline или *Link),* она не удаляется, если она была изменена в Azure DNS после извлечения локального объекта **PSPrivateDnsVirtualNetworkLink.**</span><span class="sxs-lookup"><span data-stu-id="5ed6b-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="5ed6b-129">Это обеспечивает защиту при одновременном смене зоны.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="5ed6b-130">Это можно сделать с помощью параметра *Overwrite,* который удаляет зону независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="5ed6b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ed6b-131">-PassThru</span></span>
<span data-ttu-id="5ed6b-132">Используется для передачи результата (boolean) операции удаления виртуальной сетевой связи далее по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="5ed6b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ed6b-133">-ResourceGroupName</span></span>
<span data-ttu-id="5ed6b-134">Имя группы ресурсов, которая содержит ссылку для удаления.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="5ed6b-135">Необходимо также указать параметр *ZoneName* и *Name.*</span><span class="sxs-lookup"><span data-stu-id="5ed6b-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="5ed6b-136">Кроме того, вы можете указать зону DNS с помощью объекта **PSPrivateDnsVirtualNetworkLink,** который передается через канал или параметр *Link.*</span><span class="sxs-lookup"><span data-stu-id="5ed6b-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="5ed6b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ed6b-137">-ResourceId</span></span>
<span data-ttu-id="5ed6b-138">Определяет ARM ресурса ссылки.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="5ed6b-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="5ed6b-139">-ZoneName</span></span>
<span data-ttu-id="5ed6b-140">Указывает имя частной зоны DNS, с которую связана ссылка.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="5ed6b-141">Необходимо также указать параметр *ResourceGroupName* и *Name.*</span><span class="sxs-lookup"><span data-stu-id="5ed6b-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="5ed6b-142">Ссылку также можно указать с помощью *параметра Link.*</span><span class="sxs-lookup"><span data-stu-id="5ed6b-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="5ed6b-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ed6b-143">-Confirm</span></span>
<span data-ttu-id="5ed6b-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ed6b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ed6b-145">-WhatIf</span></span>
<span data-ttu-id="5ed6b-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ed6b-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ed6b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed6b-148">CommonParameters</span></span>
<span data-ttu-id="5ed6b-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ed6b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed6b-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ed6b-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed6b-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ed6b-151">INPUTS</span></span>

### <span data-ttu-id="5ed6b-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5ed6b-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="5ed6b-153">System.String</span><span class="sxs-lookup"><span data-stu-id="5ed6b-153">System.String</span></span>

## <span data-ttu-id="5ed6b-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ed6b-154">OUTPUTS</span></span>

### <span data-ttu-id="5ed6b-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ed6b-155">System.Boolean</span></span>

## <span data-ttu-id="5ed6b-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ed6b-156">NOTES</span></span>

## <span data-ttu-id="5ed6b-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ed6b-157">RELATED LINKS</span></span>

[<span data-ttu-id="5ed6b-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5ed6b-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="5ed6b-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5ed6b-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="5ed6b-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="5ed6b-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
