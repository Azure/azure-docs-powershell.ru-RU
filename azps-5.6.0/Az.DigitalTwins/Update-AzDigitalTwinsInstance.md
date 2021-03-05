---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 967b50b024e02d4a88fa2a1d91905acad5385b6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984889"
---
# <span data-ttu-id="b6731-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="b6731-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="b6731-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6731-102">SYNOPSIS</span></span>
<span data-ttu-id="b6731-103">Обновление метаданных DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b6731-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="b6731-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6731-104">SYNTAX</span></span>

### <span data-ttu-id="b6731-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6731-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6731-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="b6731-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6731-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b6731-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6731-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b6731-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6731-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6731-109">DESCRIPTION</span></span>
<span data-ttu-id="b6731-110">Обновление метаданных DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b6731-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="b6731-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6731-111">EXAMPLES</span></span>

### <span data-ttu-id="b6731-112">Пример 1. UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6731-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b6731-113">Обновление указанного формата DigitalTwinsInstance службой ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6731-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="b6731-114">Пример 2. Обновление AzDigitalTwinsInstance другим azDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="b6731-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="b6731-115">Обновление AzDigitalTwinsInstance другим azDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="b6731-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="b6731-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6731-116">PARAMETERS</span></span>

### <span data-ttu-id="b6731-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6731-117">-DefaultProfile</span></span>
<span data-ttu-id="b6731-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6731-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6731-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="b6731-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="b6731-120">Описание службы DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="b6731-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="b6731-121">Чтобы создать новую таблицу, см. раздел "ЗАМЕТКИ" для свойств DIGITALTWINSPATCHDESCRIPTION и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b6731-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6731-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6731-122">-InputObject</span></span>
<span data-ttu-id="b6731-123">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b6731-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6731-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6731-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6731-125">Имя группы ресурсов, которая содержит digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b6731-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6731-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b6731-126">-ResourceName</span></span>
<span data-ttu-id="b6731-127">Имя digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b6731-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6731-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6731-128">-SubscriptionId</span></span>
<span data-ttu-id="b6731-129">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="b6731-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6731-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6731-130">-Tag</span></span>
<span data-ttu-id="b6731-131">Теги экземпляра</span><span class="sxs-lookup"><span data-stu-id="b6731-131">Instance tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6731-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6731-132">-Confirm</span></span>
<span data-ttu-id="b6731-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b6731-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6731-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6731-134">-WhatIf</span></span>
<span data-ttu-id="b6731-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6731-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6731-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b6731-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6731-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6731-137">CommonParameters</span></span>
<span data-ttu-id="b6731-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6731-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6731-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6731-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6731-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6731-140">INPUTS</span></span>

### <span data-ttu-id="b6731-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="b6731-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="b6731-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="b6731-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="b6731-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6731-143">OUTPUTS</span></span>

### <span data-ttu-id="b6731-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="b6731-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="b6731-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6731-145">NOTES</span></span>

<span data-ttu-id="b6731-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b6731-146">ALIASES</span></span>

<span data-ttu-id="b6731-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b6731-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6731-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b6731-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6731-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b6731-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6731-150">DIGITALTWINSPATCHDESCRIPTION: <IDigitalTwinsPatchDescription> описание службы DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="b6731-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="b6731-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Теги экземпляра</span><span class="sxs-lookup"><span data-stu-id="b6731-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="b6731-152">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="b6731-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="b6731-153">INPUTOBJECT <IDigitalTwinsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="b6731-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6731-154">`[EndpointName <String>]`: Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b6731-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="b6731-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b6731-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6731-156">`[Location <String>]`: Расположение DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b6731-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b6731-157">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b6731-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b6731-158">`[ResourceName <String>]`: Имя DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="b6731-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="b6731-159">`[SubscriptionId <String>]`: идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="b6731-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="b6731-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6731-160">RELATED LINKS</span></span>

