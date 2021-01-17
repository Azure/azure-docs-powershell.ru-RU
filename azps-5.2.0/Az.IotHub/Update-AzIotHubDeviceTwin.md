---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 451f809687ea768800f0e9e33ef4c5af9c425150
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391303"
---
# <span data-ttu-id="dc8ac-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="dc8ac-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="dc8ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="dc8ac-103">Обновляет теги и нужные свойства устройства.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="dc8ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc8ac-104">SYNTAX</span></span>

### <span data-ttu-id="dc8ac-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc8ac-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc8ac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc8ac-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc8ac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dc8ac-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc8ac-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc8ac-108">DESCRIPTION</span></span>
<span data-ttu-id="dc8ac-109">Обновляет или заменяет устройство.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="dc8ac-110">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins сведения см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="dc8ac-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc8ac-111">EXAMPLES</span></span>

### <span data-ttu-id="dc8ac-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc8ac-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="dc8ac-113">Возвращает обновленный объект обновления устройства.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="dc8ac-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dc8ac-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="dc8ac-115">Возвращает объект устройства с обновленными нужными свойствами.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="dc8ac-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="dc8ac-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="dc8ac-117">Возвращает объект устройства с обновленным свойством тегов.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="dc8ac-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="dc8ac-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="dc8ac-119">Возвращает замененный объект устройства.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="dc8ac-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc8ac-120">PARAMETERS</span></span>

### <span data-ttu-id="dc8ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc8ac-121">-DefaultProfile</span></span>
<span data-ttu-id="dc8ac-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc8ac-123">-Desired</span><span class="sxs-lookup"><span data-stu-id="dc8ac-123">-Desired</span></span>
<span data-ttu-id="dc8ac-124">Добавьте или обновйте нужное свойство на устройстве.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="dc8ac-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="dc8ac-125">-DeviceId</span></span>
<span data-ttu-id="dc8ac-126">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-126">Target Device Id.</span></span>

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

### <span data-ttu-id="dc8ac-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc8ac-127">-InputObject</span></span>
<span data-ttu-id="dc8ac-128">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="dc8ac-128">IotHub object</span></span>

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

### <span data-ttu-id="dc8ac-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="dc8ac-129">-IotHubName</span></span>
<span data-ttu-id="dc8ac-130">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="dc8ac-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dc8ac-131">-Partial</span><span class="sxs-lookup"><span data-stu-id="dc8ac-131">-Partial</span></span>
<span data-ttu-id="dc8ac-132">Позволяет обновить теги и нужные свойства устройства лишь частично.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="dc8ac-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc8ac-133">-ResourceGroupName</span></span>
<span data-ttu-id="dc8ac-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="dc8ac-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dc8ac-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc8ac-135">-ResourceId</span></span>
<span data-ttu-id="dc8ac-136">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="dc8ac-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dc8ac-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="dc8ac-137">-Tag</span></span>
<span data-ttu-id="dc8ac-138">Добавьте или обновйте свойство тегов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="dc8ac-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc8ac-139">-Confirm</span></span>
<span data-ttu-id="dc8ac-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc8ac-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc8ac-141">-WhatIf</span></span>
<span data-ttu-id="dc8ac-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc8ac-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc8ac-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc8ac-144">CommonParameters</span></span>
<span data-ttu-id="dc8ac-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc8ac-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc8ac-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc8ac-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc8ac-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc8ac-147">INPUTS</span></span>

### <span data-ttu-id="dc8ac-148">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dc8ac-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dc8ac-149">System.String</span><span class="sxs-lookup"><span data-stu-id="dc8ac-149">System.String</span></span>

## <span data-ttu-id="dc8ac-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc8ac-150">OUTPUTS</span></span>

### <span data-ttu-id="dc8ac-151">System.String</span><span class="sxs-lookup"><span data-stu-id="dc8ac-151">System.String</span></span>

## <span data-ttu-id="dc8ac-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc8ac-152">NOTES</span></span>

## <span data-ttu-id="dc8ac-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc8ac-153">RELATED LINKS</span></span>
