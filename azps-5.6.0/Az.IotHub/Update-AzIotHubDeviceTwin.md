---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 84f1485f84996c1c0e98768914afffd501722ab7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978483"
---
# <span data-ttu-id="6e1b7-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="6e1b7-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="6e1b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1b7-103">Обновляет теги и нужные свойства устройства.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="6e1b7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6e1b7-104">SYNTAX</span></span>

### <span data-ttu-id="6e1b7-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e1b7-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e1b7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6e1b7-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e1b7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6e1b7-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e1b7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e1b7-108">DESCRIPTION</span></span>
<span data-ttu-id="6e1b7-109">Обновляет или заменяет устройство.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="6e1b7-110">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins сведения см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="6e1b7-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6e1b7-111">EXAMPLES</span></span>

### <span data-ttu-id="6e1b7-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6e1b7-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="6e1b7-113">Возвращает обновленный объект обновления устройства.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="6e1b7-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6e1b7-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="6e1b7-115">Возвращает объект устройства с обновленными нужными свойствами.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="6e1b7-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6e1b7-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="6e1b7-117">Возвращает объект устройства с обновленным свойством тегов.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="6e1b7-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6e1b7-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="6e1b7-119">Возвращает замененный объект устройства.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="6e1b7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e1b7-120">PARAMETERS</span></span>

### <span data-ttu-id="6e1b7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1b7-121">-DefaultProfile</span></span>
<span data-ttu-id="6e1b7-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e1b7-123">-Desired</span><span class="sxs-lookup"><span data-stu-id="6e1b7-123">-Desired</span></span>
<span data-ttu-id="6e1b7-124">Добавьте или обновйте нужное свойство на устройстве.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="6e1b7-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6e1b7-125">-DeviceId</span></span>
<span data-ttu-id="6e1b7-126">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-126">Target Device Id.</span></span>

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

### <span data-ttu-id="6e1b7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e1b7-127">-InputObject</span></span>
<span data-ttu-id="6e1b7-128">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="6e1b7-128">IotHub object</span></span>

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

### <span data-ttu-id="6e1b7-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6e1b7-129">-IotHubName</span></span>
<span data-ttu-id="6e1b7-130">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="6e1b7-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6e1b7-131">-Partial</span><span class="sxs-lookup"><span data-stu-id="6e1b7-131">-Partial</span></span>
<span data-ttu-id="6e1b7-132">Позволяет обновить теги и нужные свойства устройства лишь частично.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="6e1b7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e1b7-133">-ResourceGroupName</span></span>
<span data-ttu-id="6e1b7-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6e1b7-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6e1b7-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e1b7-135">-ResourceId</span></span>
<span data-ttu-id="6e1b7-136">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="6e1b7-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6e1b7-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="6e1b7-137">-Tag</span></span>
<span data-ttu-id="6e1b7-138">Добавьте или обновйте свойство тегов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="6e1b7-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e1b7-139">-Confirm</span></span>
<span data-ttu-id="6e1b7-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e1b7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e1b7-141">-WhatIf</span></span>
<span data-ttu-id="6e1b7-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e1b7-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e1b7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1b7-144">CommonParameters</span></span>
<span data-ttu-id="6e1b7-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e1b7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1b7-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e1b7-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1b7-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e1b7-147">INPUTS</span></span>

### <span data-ttu-id="6e1b7-148">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6e1b7-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6e1b7-149">System.String</span><span class="sxs-lookup"><span data-stu-id="6e1b7-149">System.String</span></span>

## <span data-ttu-id="6e1b7-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6e1b7-150">OUTPUTS</span></span>

### <span data-ttu-id="6e1b7-151">System.String</span><span class="sxs-lookup"><span data-stu-id="6e1b7-151">System.String</span></span>

## <span data-ttu-id="6e1b7-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6e1b7-152">NOTES</span></span>

## <span data-ttu-id="6e1b7-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e1b7-153">RELATED LINKS</span></span>
