---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236445"
---
# <span data-ttu-id="37b1e-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="37b1e-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="37b1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="37b1e-103">Добавляйте неграничные устройства в качестве дочерних устройств на пограничном устройстве.</span><span class="sxs-lookup"><span data-stu-id="37b1e-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="37b1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37b1e-104">SYNTAX</span></span>

### <span data-ttu-id="37b1e-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37b1e-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37b1e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="37b1e-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37b1e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="37b1e-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37b1e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37b1e-108">DESCRIPTION</span></span>
<span data-ttu-id="37b1e-109">Добавьте указанный список с разделителями-запятыми в качестве дочернего элемента указанного Edge устройства.</span><span class="sxs-lookup"><span data-stu-id="37b1e-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="37b1e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37b1e-110">EXAMPLES</span></span>

### <span data-ttu-id="37b1e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="37b1e-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="37b1e-112">Добавляйте неграничные устройства в качестве дочерних устройств на пограничном устройстве.</span><span class="sxs-lookup"><span data-stu-id="37b1e-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="37b1e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="37b1e-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="37b1e-114">Добавляйте неграничные устройства как дочерние элементы на пограничном устройстве, независимо от того, что неedge-устройство уже является дочерним для другого пограничного устройства.</span><span class="sxs-lookup"><span data-stu-id="37b1e-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="37b1e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37b1e-115">PARAMETERS</span></span>

### <span data-ttu-id="37b1e-116">-Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="37b1e-116">-Children</span></span>
<span data-ttu-id="37b1e-117">Дочерний список устройств (разделенный запятыми) включает только устройства без краев.</span><span class="sxs-lookup"><span data-stu-id="37b1e-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b1e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b1e-118">-DefaultProfile</span></span>
<span data-ttu-id="37b1e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37b1e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37b1e-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="37b1e-120">-DeviceId</span></span>
<span data-ttu-id="37b1e-121">Идентификатор устройства Edge.</span><span class="sxs-lookup"><span data-stu-id="37b1e-121">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b1e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="37b1e-122">-Force</span></span>
<span data-ttu-id="37b1e-123">Перезаписывает родительский объект устройства, не являющегося Edge.</span><span class="sxs-lookup"><span data-stu-id="37b1e-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="37b1e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37b1e-124">-InputObject</span></span>
<span data-ttu-id="37b1e-125">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="37b1e-125">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37b1e-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="37b1e-126">-IotHubName</span></span>
<span data-ttu-id="37b1e-127">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="37b1e-127">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b1e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b1e-128">-ResourceGroupName</span></span>
<span data-ttu-id="37b1e-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="37b1e-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b1e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37b1e-130">-ResourceId</span></span>
<span data-ttu-id="37b1e-131">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="37b1e-131">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37b1e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37b1e-132">-Confirm</span></span>
<span data-ttu-id="37b1e-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="37b1e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37b1e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b1e-134">-WhatIf</span></span>
<span data-ttu-id="37b1e-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="37b1e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37b1e-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="37b1e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37b1e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b1e-137">CommonParameters</span></span>
<span data-ttu-id="37b1e-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37b1e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b1e-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37b1e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b1e-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37b1e-140">INPUTS</span></span>

### <span data-ttu-id="37b1e-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="37b1e-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="37b1e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="37b1e-142">System.String</span></span>

## <span data-ttu-id="37b1e-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37b1e-143">OUTPUTS</span></span>

### <span data-ttu-id="37b1e-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="37b1e-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="37b1e-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="37b1e-145">NOTES</span></span>

## <span data-ttu-id="37b1e-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37b1e-146">RELATED LINKS</span></span>
