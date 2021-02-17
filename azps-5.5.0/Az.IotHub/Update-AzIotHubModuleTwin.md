---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234116"
---
# <span data-ttu-id="4e134-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="4e134-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="4e134-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e134-102">SYNOPSIS</span></span>
<span data-ttu-id="4e134-103">Обновляет теги и нужные свойства модуля устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="4e134-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="4e134-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e134-104">SYNTAX</span></span>

### <span data-ttu-id="4e134-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e134-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e134-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4e134-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e134-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4e134-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e134-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e134-108">DESCRIPTION</span></span>
<span data-ttu-id="4e134-109">Обновляет или заменяет устройство.</span><span class="sxs-lookup"><span data-stu-id="4e134-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="4e134-110">Дополнительные https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins сведения см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="4e134-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="4e134-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e134-111">EXAMPLES</span></span>

### <span data-ttu-id="4e134-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e134-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="4e134-113">Возвращает обновленный объект module для устройства.</span><span class="sxs-lookup"><span data-stu-id="4e134-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="4e134-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4e134-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="4e134-115">Возвращает объект модуля устройства с обновленными нужными свойствами.</span><span class="sxs-lookup"><span data-stu-id="4e134-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="4e134-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4e134-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="4e134-117">Возвращает объект модуля устройства с обновленным свойством тегов.</span><span class="sxs-lookup"><span data-stu-id="4e134-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="4e134-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="4e134-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="4e134-119">Возвращает объект replaced device module .</span><span class="sxs-lookup"><span data-stu-id="4e134-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="4e134-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e134-120">PARAMETERS</span></span>

### <span data-ttu-id="4e134-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e134-121">-DefaultProfile</span></span>
<span data-ttu-id="4e134-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e134-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e134-123">-Desired</span><span class="sxs-lookup"><span data-stu-id="4e134-123">-Desired</span></span>
<span data-ttu-id="4e134-124">Добавьте или обновйте нужное свойство в модуле.</span><span class="sxs-lookup"><span data-stu-id="4e134-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="4e134-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4e134-125">-DeviceId</span></span>
<span data-ttu-id="4e134-126">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="4e134-126">Target Device Id.</span></span>

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

### <span data-ttu-id="4e134-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e134-127">-InputObject</span></span>
<span data-ttu-id="4e134-128">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="4e134-128">IotHub object</span></span>

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

### <span data-ttu-id="4e134-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4e134-129">-IotHubName</span></span>
<span data-ttu-id="4e134-130">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="4e134-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4e134-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="4e134-131">-ModuleId</span></span>
<span data-ttu-id="4e134-132">ИД целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="4e134-132">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e134-133">-Partial</span><span class="sxs-lookup"><span data-stu-id="4e134-133">-Partial</span></span>
<span data-ttu-id="4e134-134">Позволяет обновить теги и нужные свойства модуля лишь частично.</span><span class="sxs-lookup"><span data-stu-id="4e134-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="4e134-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e134-135">-ResourceGroupName</span></span>
<span data-ttu-id="4e134-136">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4e134-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4e134-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e134-137">-ResourceId</span></span>
<span data-ttu-id="4e134-138">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="4e134-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4e134-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e134-139">-Tag</span></span>
<span data-ttu-id="4e134-140">Добавьте или обновйте свойство тегов в модуле.</span><span class="sxs-lookup"><span data-stu-id="4e134-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="4e134-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e134-141">-Confirm</span></span>
<span data-ttu-id="4e134-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4e134-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e134-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e134-143">-WhatIf</span></span>
<span data-ttu-id="4e134-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e134-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e134-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4e134-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e134-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e134-146">CommonParameters</span></span>
<span data-ttu-id="4e134-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e134-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e134-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e134-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e134-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e134-149">INPUTS</span></span>

### <span data-ttu-id="4e134-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4e134-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4e134-151">System.String</span><span class="sxs-lookup"><span data-stu-id="4e134-151">System.String</span></span>

## <span data-ttu-id="4e134-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e134-152">OUTPUTS</span></span>

### <span data-ttu-id="4e134-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="4e134-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="4e134-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e134-154">NOTES</span></span>

## <span data-ttu-id="4e134-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e134-155">RELATED LINKS</span></span>
