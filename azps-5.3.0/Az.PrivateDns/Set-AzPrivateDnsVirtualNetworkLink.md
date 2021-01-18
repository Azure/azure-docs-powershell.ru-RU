---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3ffcc30dc0291be06c27ee53ee0ee7ea14f3e2c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505431"
---
# <span data-ttu-id="270ad-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="270ad-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="270ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="270ad-102">SYNOPSIS</span></span>
<span data-ttu-id="270ad-103">Обновления и наборы виртуальной сетевой связи, связанной с закрытой зоной и группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="270ad-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="270ad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="270ad-104">SYNTAX</span></span>

### <span data-ttu-id="270ad-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="270ad-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="270ad-106">Объект</span><span class="sxs-lookup"><span data-stu-id="270ad-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="270ad-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="270ad-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="270ad-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="270ad-108">DESCRIPTION</span></span>
<span data-ttu-id="270ad-109">Командлет **Set-AzPrivateDnsVirtualNetworkLink** обновляет ссылку, связанную с зоной из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="270ad-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="270ad-110">Объект **PSPrivateDnsVirtualNetworkLink** можно передать с помощью параметра *Link* или с помощью оператора конвейера. Кроме того, можно указать параметры *Name* *ZoneName* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="270ad-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="270ad-111">С помощью переменных Confirm и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="270ad-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="270ad-112">При указании зоны с помощью объекта **PSPrivateDnsVirtualNetworkLink** (передается через канал или параметр *Link),* ссылка не обновляется, если она была изменена в Azure DNS после извлечения локального объекта **PSPrivateDnsVirtualNetworkLink.**</span><span class="sxs-lookup"><span data-stu-id="270ad-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="270ad-113">Это обеспечивает защиту от изменения одновременной связи.</span><span class="sxs-lookup"><span data-stu-id="270ad-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="270ad-114">Это можно сделать с помощью параметра *Overwrite,* который обновляет ссылку независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="270ad-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="270ad-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="270ad-115">EXAMPLES</span></span>

### <span data-ttu-id="270ad-116">Пример 1. Настройка ссылки</span><span class="sxs-lookup"><span data-stu-id="270ad-116">Example 1: Set a link</span></span>
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="270ad-117">Этот набор команд isRegistrationEnabled to True для ссылки mylink, связанной с зоной myzone.com из группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="270ad-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="270ad-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="270ad-118">PARAMETERS</span></span>

### <span data-ttu-id="270ad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="270ad-119">-DefaultProfile</span></span>
<span data-ttu-id="270ad-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="270ad-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="270ad-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="270ad-121">-InputObject</span></span>
<span data-ttu-id="270ad-122">Объект виртуальной сетевой связи, который нужно установить.</span><span class="sxs-lookup"><span data-stu-id="270ad-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="270ad-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="270ad-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="270ad-124">Boolean that represents if registration is enabled on the virtual network link.</span><span class="sxs-lookup"><span data-stu-id="270ad-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="270ad-125">-Name</span><span class="sxs-lookup"><span data-stu-id="270ad-125">-Name</span></span>
<span data-ttu-id="270ad-126">Указывает имя ссылки, которую этот cmdlet удаляет.</span><span class="sxs-lookup"><span data-stu-id="270ad-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="270ad-127">Необходимо также указать параметр *ResourceGroupName* и *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="270ad-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="270ad-128">Кроме того, вы можете указать частную ссылку DNS с помощью *параметра ссылки.*</span><span class="sxs-lookup"><span data-stu-id="270ad-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="270ad-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="270ad-129">-Overwrite</span></span>
<span data-ttu-id="270ad-130">При указании ссылки с помощью объекта **PSPrivateDnsVirtualNetworkLink** (передается через канал или параметр *Link),* ссылка не удаляется, если она была изменена в Azure DNS после извлечения локального объекта **PSPrivateDnsVirtualNetworkLink.**</span><span class="sxs-lookup"><span data-stu-id="270ad-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="270ad-131">Это обеспечивает защиту от изменения одновременной связи.</span><span class="sxs-lookup"><span data-stu-id="270ad-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="270ad-132">Это можно сделать с помощью параметра *Overwrite,* который удаляет ссылку независимо от одновременного изменения.</span><span class="sxs-lookup"><span data-stu-id="270ad-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="270ad-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="270ad-133">-ResourceGroupName</span></span>
<span data-ttu-id="270ad-134">Имя группы ресурсов, которая содержит ссылку для удаления.</span><span class="sxs-lookup"><span data-stu-id="270ad-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="270ad-135">Необходимо также указать параметр *ZoneName* и *Name.*</span><span class="sxs-lookup"><span data-stu-id="270ad-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="270ad-136">Кроме того, можно указать виртуальную сетевую ссылку с помощью объекта **PSPrivateDnsVirtualNetworkLink,** переданного через канал или параметр *Link.*</span><span class="sxs-lookup"><span data-stu-id="270ad-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="270ad-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="270ad-137">-ResourceId</span></span>
<span data-ttu-id="270ad-138">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="270ad-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="270ad-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="270ad-139">-Tag</span></span>
<span data-ttu-id="270ad-140">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="270ad-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="270ad-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="270ad-141">-ZoneName</span></span>
<span data-ttu-id="270ad-142">Указывает имя зоны DNS, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="270ad-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="270ad-143">Необходимо также указать *параметр Name* и *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="270ad-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="270ad-144">Кроме того, вы можете указать частную ссылку DNS с помощью *параметра ссылки.*</span><span class="sxs-lookup"><span data-stu-id="270ad-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="270ad-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="270ad-145">-Confirm</span></span>
<span data-ttu-id="270ad-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="270ad-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="270ad-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="270ad-147">-WhatIf</span></span>
<span data-ttu-id="270ad-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="270ad-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="270ad-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="270ad-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="270ad-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270ad-150">CommonParameters</span></span>
<span data-ttu-id="270ad-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="270ad-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270ad-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="270ad-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270ad-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="270ad-153">INPUTS</span></span>

### <span data-ttu-id="270ad-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="270ad-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="270ad-155">System.String</span><span class="sxs-lookup"><span data-stu-id="270ad-155">System.String</span></span>

## <span data-ttu-id="270ad-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="270ad-156">OUTPUTS</span></span>

### <span data-ttu-id="270ad-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="270ad-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="270ad-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="270ad-158">NOTES</span></span>

## <span data-ttu-id="270ad-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="270ad-159">RELATED LINKS</span></span>

[<span data-ttu-id="270ad-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="270ad-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="270ad-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="270ad-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="270ad-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="270ad-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
