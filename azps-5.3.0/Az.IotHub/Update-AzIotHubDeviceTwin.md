---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 451f809687ea768800f0e9e33ef4c5af9c425150
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425871"
---
# <span data-ttu-id="2a5b4-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="2a5b4-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="2a5b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a5b4-102">SYNOPSIS</span></span>
<span data-ttu-id="2a5b4-103">Обновляет теги и нужные свойства устройства.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="2a5b4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a5b4-104">SYNTAX</span></span>

### <span data-ttu-id="2a5b4-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a5b4-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a5b4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2a5b4-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a5b4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2a5b4-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a5b4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a5b4-108">DESCRIPTION</span></span>
<span data-ttu-id="2a5b4-109">Обновляет или заменяет устройство.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="2a5b4-110">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins сведения см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="2a5b4-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a5b4-111">EXAMPLES</span></span>

### <span data-ttu-id="2a5b4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a5b4-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="2a5b4-113">Возвращает обновленный объект обновления устройства.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="2a5b4-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2a5b4-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="2a5b4-115">Возвращает объект устройства с обновленными нужными свойствами.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="2a5b4-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2a5b4-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="2a5b4-117">Возвращает объект устройства с обновленным свойством тегов.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="2a5b4-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="2a5b4-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="2a5b4-119">Возвращает замененный объект устройства.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="2a5b4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a5b4-120">PARAMETERS</span></span>

### <span data-ttu-id="2a5b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a5b4-121">-DefaultProfile</span></span>
<span data-ttu-id="2a5b4-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a5b4-123">-Desired</span><span class="sxs-lookup"><span data-stu-id="2a5b4-123">-Desired</span></span>
<span data-ttu-id="2a5b4-124">Добавьте или обновйте нужное свойство на устройстве.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="2a5b4-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2a5b4-125">-DeviceId</span></span>
<span data-ttu-id="2a5b4-126">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-126">Target Device Id.</span></span>

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

### <span data-ttu-id="2a5b4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a5b4-127">-InputObject</span></span>
<span data-ttu-id="2a5b4-128">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="2a5b4-128">IotHub object</span></span>

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

### <span data-ttu-id="2a5b4-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2a5b4-129">-IotHubName</span></span>
<span data-ttu-id="2a5b4-130">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="2a5b4-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2a5b4-131">-Partial</span><span class="sxs-lookup"><span data-stu-id="2a5b4-131">-Partial</span></span>
<span data-ttu-id="2a5b4-132">Позволяет обновить теги и нужные свойства устройства лишь частично.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="2a5b4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a5b4-133">-ResourceGroupName</span></span>
<span data-ttu-id="2a5b4-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2a5b4-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2a5b4-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a5b4-135">-ResourceId</span></span>
<span data-ttu-id="2a5b4-136">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="2a5b4-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2a5b4-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="2a5b4-137">-Tag</span></span>
<span data-ttu-id="2a5b4-138">Добавьте или обновйте свойство тегов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="2a5b4-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a5b4-139">-Confirm</span></span>
<span data-ttu-id="2a5b4-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a5b4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a5b4-141">-WhatIf</span></span>
<span data-ttu-id="2a5b4-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a5b4-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a5b4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a5b4-144">CommonParameters</span></span>
<span data-ttu-id="2a5b4-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a5b4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a5b4-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a5b4-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a5b4-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a5b4-147">INPUTS</span></span>

### <span data-ttu-id="2a5b4-148">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2a5b4-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2a5b4-149">System.String</span><span class="sxs-lookup"><span data-stu-id="2a5b4-149">System.String</span></span>

## <span data-ttu-id="2a5b4-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a5b4-150">OUTPUTS</span></span>

### <span data-ttu-id="2a5b4-151">System.String</span><span class="sxs-lookup"><span data-stu-id="2a5b4-151">System.String</span></span>

## <span data-ttu-id="2a5b4-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a5b4-152">NOTES</span></span>

## <span data-ttu-id="2a5b4-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a5b4-153">RELATED LINKS</span></span>
