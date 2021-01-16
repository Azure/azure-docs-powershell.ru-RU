---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397052"
---
# <span data-ttu-id="27770-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="27770-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="27770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27770-102">SYNOPSIS</span></span>
<span data-ttu-id="27770-103">Добавляйте устройства, не скийи в качестве детей, на устройство границы.</span><span class="sxs-lookup"><span data-stu-id="27770-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="27770-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="27770-104">SYNTAX</span></span>

### <span data-ttu-id="27770-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27770-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27770-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="27770-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27770-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="27770-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27770-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27770-108">DESCRIPTION</span></span>
<span data-ttu-id="27770-109">Добавьте указанный список с разделиными запятой не edge-ids устройств как дети указанного edge-устройства.</span><span class="sxs-lookup"><span data-stu-id="27770-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="27770-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="27770-110">EXAMPLES</span></span>

### <span data-ttu-id="27770-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27770-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="27770-112">Добавляйте устройства, не скийи в качестве детей, на устройство границы.</span><span class="sxs-lookup"><span data-stu-id="27770-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="27770-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="27770-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="27770-114">Добавляйте не edge-устройства в качестве детей на устройство, независимо от того, что устройство с другими краями устройства уже является ребенком другого edge устройства.</span><span class="sxs-lookup"><span data-stu-id="27770-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="27770-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27770-115">PARAMETERS</span></span>

### <span data-ttu-id="27770-116">-Дети</span><span class="sxs-lookup"><span data-stu-id="27770-116">-Children</span></span>
<span data-ttu-id="27770-117">Список устройств ребенка (разделенный запятой) включает только устройства, не включающее в себя границы.</span><span class="sxs-lookup"><span data-stu-id="27770-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="27770-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27770-118">-DefaultProfile</span></span>
<span data-ttu-id="27770-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27770-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27770-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="27770-120">-DeviceId</span></span>
<span data-ttu-id="27770-121">Id of edge device.</span><span class="sxs-lookup"><span data-stu-id="27770-121">Id of edge device.</span></span>

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

### <span data-ttu-id="27770-122">-Force</span><span class="sxs-lookup"><span data-stu-id="27770-122">-Force</span></span>
<span data-ttu-id="27770-123">Переопишет родительское устройство на устройстве, которое не является границым.</span><span class="sxs-lookup"><span data-stu-id="27770-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="27770-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27770-124">-InputObject</span></span>
<span data-ttu-id="27770-125">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="27770-125">IotHub object</span></span>

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

### <span data-ttu-id="27770-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="27770-126">-IotHubName</span></span>
<span data-ttu-id="27770-127">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="27770-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="27770-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27770-128">-ResourceGroupName</span></span>
<span data-ttu-id="27770-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="27770-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="27770-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27770-130">-ResourceId</span></span>
<span data-ttu-id="27770-131">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="27770-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="27770-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27770-132">-Confirm</span></span>
<span data-ttu-id="27770-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27770-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27770-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27770-134">-WhatIf</span></span>
<span data-ttu-id="27770-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27770-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27770-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="27770-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27770-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27770-137">CommonParameters</span></span>
<span data-ttu-id="27770-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27770-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27770-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27770-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27770-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27770-140">INPUTS</span></span>

### <span data-ttu-id="27770-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="27770-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="27770-142">System.String</span><span class="sxs-lookup"><span data-stu-id="27770-142">System.String</span></span>

## <span data-ttu-id="27770-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="27770-143">OUTPUTS</span></span>

### <span data-ttu-id="27770-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice Темы</span><span class="sxs-lookup"><span data-stu-id="27770-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="27770-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="27770-145">NOTES</span></span>

## <span data-ttu-id="27770-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27770-146">RELATED LINKS</span></span>
