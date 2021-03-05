---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: e41030f30e3c5651aca3ddf716af99c919e6e6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997898"
---
# <span data-ttu-id="18109-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="18109-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="18109-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18109-102">SYNOPSIS</span></span>
<span data-ttu-id="18109-103">Добавляйте устройства, не скийи в качестве детей, на устройство границы.</span><span class="sxs-lookup"><span data-stu-id="18109-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="18109-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="18109-104">SYNTAX</span></span>

### <span data-ttu-id="18109-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="18109-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18109-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="18109-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18109-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="18109-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18109-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18109-108">DESCRIPTION</span></span>
<span data-ttu-id="18109-109">Добавьте указанный список не edge-ids устройств с разделиями-запятой как дети указанного edgeного устройства.</span><span class="sxs-lookup"><span data-stu-id="18109-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="18109-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="18109-110">EXAMPLES</span></span>

### <span data-ttu-id="18109-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="18109-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="18109-112">Добавляйте устройства, не скийи в качестве детей, на устройство границы.</span><span class="sxs-lookup"><span data-stu-id="18109-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="18109-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="18109-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="18109-114">Добавляйте не edge-устройства в качестве детей на устройство, независимо от того, что устройство с другими краями устройства уже является ребенком другого edge устройства.</span><span class="sxs-lookup"><span data-stu-id="18109-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="18109-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18109-115">PARAMETERS</span></span>

### <span data-ttu-id="18109-116">-Дети</span><span class="sxs-lookup"><span data-stu-id="18109-116">-Children</span></span>
<span data-ttu-id="18109-117">Список устройств ребенка (разделенный запятой) включает только устройства, не включающее в себя границы.</span><span class="sxs-lookup"><span data-stu-id="18109-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="18109-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18109-118">-DefaultProfile</span></span>
<span data-ttu-id="18109-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18109-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18109-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="18109-120">-DeviceId</span></span>
<span data-ttu-id="18109-121">Id of edge device.</span><span class="sxs-lookup"><span data-stu-id="18109-121">Id of edge device.</span></span>

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

### <span data-ttu-id="18109-122">-Force</span><span class="sxs-lookup"><span data-stu-id="18109-122">-Force</span></span>
<span data-ttu-id="18109-123">Переопишет родительское устройство на устройстве, которое не является границым.</span><span class="sxs-lookup"><span data-stu-id="18109-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="18109-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18109-124">-InputObject</span></span>
<span data-ttu-id="18109-125">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="18109-125">IotHub object</span></span>

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

### <span data-ttu-id="18109-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="18109-126">-IotHubName</span></span>
<span data-ttu-id="18109-127">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="18109-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="18109-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18109-128">-ResourceGroupName</span></span>
<span data-ttu-id="18109-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="18109-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="18109-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18109-130">-ResourceId</span></span>
<span data-ttu-id="18109-131">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="18109-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="18109-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18109-132">-Confirm</span></span>
<span data-ttu-id="18109-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="18109-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18109-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18109-134">-WhatIf</span></span>
<span data-ttu-id="18109-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18109-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18109-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="18109-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18109-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18109-137">CommonParameters</span></span>
<span data-ttu-id="18109-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18109-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18109-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18109-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18109-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18109-140">INPUTS</span></span>

### <span data-ttu-id="18109-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="18109-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="18109-142">System.String</span><span class="sxs-lookup"><span data-stu-id="18109-142">System.String</span></span>

## <span data-ttu-id="18109-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18109-143">OUTPUTS</span></span>

### <span data-ttu-id="18109-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice Темы</span><span class="sxs-lookup"><span data-stu-id="18109-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="18109-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="18109-145">NOTES</span></span>

## <span data-ttu-id="18109-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18109-146">RELATED LINKS</span></span>
