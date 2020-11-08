---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235490"
---
# <span data-ttu-id="ba68e-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ba68e-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="ba68e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba68e-102">SYNOPSIS</span></span>
<span data-ttu-id="ba68e-103">Удаление ссылки на виртуальную сеть из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba68e-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="ba68e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba68e-104">SYNTAX</span></span>

### <span data-ttu-id="ba68e-105">Поля (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba68e-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba68e-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="ba68e-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba68e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba68e-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba68e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba68e-108">DESCRIPTION</span></span>
<span data-ttu-id="ba68e-109">Командлет **Remove-AzPrivateDnsVirtualNetworkLink** окончательно удаляет частную ссылку DNS (Domain Name System) из заданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba68e-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="ba68e-110">Вы можете передать объект **PSPrivateDnsVirtualNetworkLink** с помощью параметра *Link* или оператора Pipeline либо указать *имя* *имя_зоны* и *ResourceGroupName* для параметров.</span><span class="sxs-lookup"><span data-stu-id="ba68e-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="ba68e-111">Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ba68e-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ba68e-112">При указании ссылки с помощью объекта **PSPrivateDnsVirtualNetworkLink** , который передается через конвейер или параметр *Link* , ссылка не удаляется, если она была изменена в службе Azure Private DNS с момента получения локального объекта **PSPrivateDnsVirtualNetworkLink** .</span><span class="sxs-lookup"><span data-stu-id="ba68e-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="ba68e-113">Это обеспечивает защиту для одновременных изменений зоны.</span><span class="sxs-lookup"><span data-stu-id="ba68e-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="ba68e-114">Это может быть подавлено с помощью параметра *overwrite* , что приводит к удалению зоны независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="ba68e-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="ba68e-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba68e-115">EXAMPLES</span></span>

### <span data-ttu-id="ba68e-116">Пример 1: Удаление ссылки</span><span class="sxs-lookup"><span data-stu-id="ba68e-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="ba68e-117">Эта команда удаляет связь с именем Mylink, связанную с зоной myzone.com, из группы ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ba68e-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="ba68e-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba68e-118">PARAMETERS</span></span>

### <span data-ttu-id="ba68e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba68e-119">-DefaultProfile</span></span>
<span data-ttu-id="ba68e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ba68e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba68e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba68e-121">-InputObject</span></span>
<span data-ttu-id="ba68e-122">Объект связи виртуальной сети, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ba68e-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="ba68e-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba68e-123">-Name</span></span>
<span data-ttu-id="ba68e-124">Указывает имя удаляемой ссылки.</span><span class="sxs-lookup"><span data-stu-id="ba68e-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="ba68e-125">Кроме того, необходимо указать параметр *ResourceGroupName* и *zonename* .</span><span class="sxs-lookup"><span data-stu-id="ba68e-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="ba68e-126">Кроме того, вы можете указать ссылку с помощью параметра *Link* .</span><span class="sxs-lookup"><span data-stu-id="ba68e-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="ba68e-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ba68e-127">-Overwrite</span></span>
<span data-ttu-id="ba68e-128">При указании зоны с помощью объекта **PSPrivateDnsVirtualNetworkLink** , который передается через конвейер или параметр *Link* , зона не удаляется, если она была изменена в Azure DNS с момента получения локального объекта **PSPrivateDnsVirtualNetworkLink** .</span><span class="sxs-lookup"><span data-stu-id="ba68e-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="ba68e-129">Это обеспечивает защиту для одновременных изменений зоны.</span><span class="sxs-lookup"><span data-stu-id="ba68e-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="ba68e-130">Это может быть подавлено с помощью параметра *overwrite* , что приводит к удалению зоны независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="ba68e-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="ba68e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba68e-131">-PassThru</span></span>
<span data-ttu-id="ba68e-132">Используется для передачи результата (логического значения) для операции удалить виртуальную сеть, расположенную дальше по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="ba68e-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="ba68e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba68e-133">-ResourceGroupName</span></span>
<span data-ttu-id="ba68e-134">Указывает имя группы ресурсов, которая содержит ссылку для удаления.</span><span class="sxs-lookup"><span data-stu-id="ba68e-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="ba68e-135">Кроме того, необходимо указать параметр *zonename* и *Name* .</span><span class="sxs-lookup"><span data-stu-id="ba68e-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="ba68e-136">Кроме того, вы можете указать зону DNS с помощью объекта **PSPrivateDnsVirtualNetworkLink** , который передается с помощью конвейера или параметра *ссылки* .</span><span class="sxs-lookup"><span data-stu-id="ba68e-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="ba68e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba68e-137">-ResourceId</span></span>
<span data-ttu-id="ba68e-138">Указывает идентификатор ресурса ARM ссылки.</span><span class="sxs-lookup"><span data-stu-id="ba68e-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="ba68e-139">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="ba68e-139">-ZoneName</span></span>
<span data-ttu-id="ba68e-140">Указывает имя частной зоны DNS, с которой связана ссылка.</span><span class="sxs-lookup"><span data-stu-id="ba68e-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="ba68e-141">Кроме того, необходимо указать параметр *ResourceGroupName* и *Name* .</span><span class="sxs-lookup"><span data-stu-id="ba68e-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="ba68e-142">Кроме того, вы можете указать ссылку с помощью параметра *Link* .</span><span class="sxs-lookup"><span data-stu-id="ba68e-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="ba68e-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba68e-143">-Confirm</span></span>
<span data-ttu-id="ba68e-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba68e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba68e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba68e-145">-WhatIf</span></span>
<span data-ttu-id="ba68e-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba68e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba68e-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba68e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba68e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba68e-148">CommonParameters</span></span>
<span data-ttu-id="ba68e-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba68e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba68e-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba68e-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba68e-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba68e-151">INPUTS</span></span>

### <span data-ttu-id="ba68e-152">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ba68e-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="ba68e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ba68e-153">System.String</span></span>

## <span data-ttu-id="ba68e-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba68e-154">OUTPUTS</span></span>

### <span data-ttu-id="ba68e-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba68e-155">System.Boolean</span></span>

## <span data-ttu-id="ba68e-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba68e-156">NOTES</span></span>

## <span data-ttu-id="ba68e-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba68e-157">RELATED LINKS</span></span>

[<span data-ttu-id="ba68e-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ba68e-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="ba68e-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ba68e-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="ba68e-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ba68e-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
