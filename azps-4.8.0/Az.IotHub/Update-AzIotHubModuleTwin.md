---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078233"
---
# <span data-ttu-id="79aa0-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="79aa0-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="79aa0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="79aa0-103">Обновляет Теги и нужные свойства модуля устройства IoT двойной.</span><span class="sxs-lookup"><span data-stu-id="79aa0-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="79aa0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79aa0-104">SYNTAX</span></span>

### <span data-ttu-id="79aa0-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79aa0-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79aa0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="79aa0-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79aa0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="79aa0-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79aa0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79aa0-108">DESCRIPTION</span></span>
<span data-ttu-id="79aa0-109">Обновляет или заменяет двойной устройства.</span><span class="sxs-lookup"><span data-stu-id="79aa0-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="79aa0-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twinsДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="79aa0-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="79aa0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79aa0-111">EXAMPLES</span></span>

### <span data-ttu-id="79aa0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="79aa0-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="79aa0-113">Возвращает обновленный объект модуля устройства двойной.</span><span class="sxs-lookup"><span data-stu-id="79aa0-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="79aa0-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="79aa0-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="79aa0-115">Возвращает объект двойной модуля устройства с обновленными необходимыми свойствами.</span><span class="sxs-lookup"><span data-stu-id="79aa0-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="79aa0-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="79aa0-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="79aa0-117">Возвращает объект двойной модуля устройства со обновленным свойством Tags.</span><span class="sxs-lookup"><span data-stu-id="79aa0-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="79aa0-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="79aa0-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="79aa0-119">Возвращает заменяющий объект двойной модуля устройства.</span><span class="sxs-lookup"><span data-stu-id="79aa0-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="79aa0-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79aa0-120">PARAMETERS</span></span>

### <span data-ttu-id="79aa0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79aa0-121">-DefaultProfile</span></span>
<span data-ttu-id="79aa0-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79aa0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79aa0-123">-Необходимый</span><span class="sxs-lookup"><span data-stu-id="79aa0-123">-Desired</span></span>
<span data-ttu-id="79aa0-124">Добавьте или обновите нужное свойство в модуле двойной.</span><span class="sxs-lookup"><span data-stu-id="79aa0-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="79aa0-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="79aa0-125">-DeviceId</span></span>
<span data-ttu-id="79aa0-126">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="79aa0-126">Target Device Id.</span></span>

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

### <span data-ttu-id="79aa0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79aa0-127">-InputObject</span></span>
<span data-ttu-id="79aa0-128">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="79aa0-128">IotHub object</span></span>

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

### <span data-ttu-id="79aa0-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="79aa0-129">-IotHubName</span></span>
<span data-ttu-id="79aa0-130">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="79aa0-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="79aa0-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="79aa0-131">-ModuleId</span></span>
<span data-ttu-id="79aa0-132">Идентификатор целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="79aa0-132">Target Module Id.</span></span>

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

### <span data-ttu-id="79aa0-133">-Partial</span><span class="sxs-lookup"><span data-stu-id="79aa0-133">-Partial</span></span>
<span data-ttu-id="79aa0-134">Позволяет только частично обновлять Теги и нужные свойства модуля двойной.</span><span class="sxs-lookup"><span data-stu-id="79aa0-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="79aa0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79aa0-135">-ResourceGroupName</span></span>
<span data-ttu-id="79aa0-136">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="79aa0-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="79aa0-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79aa0-137">-ResourceId</span></span>
<span data-ttu-id="79aa0-138">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="79aa0-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="79aa0-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="79aa0-139">-Tag</span></span>
<span data-ttu-id="79aa0-140">Добавьте или обновите свойство Tags в модуле двойной.</span><span class="sxs-lookup"><span data-stu-id="79aa0-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="79aa0-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79aa0-141">-Confirm</span></span>
<span data-ttu-id="79aa0-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79aa0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79aa0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79aa0-143">-WhatIf</span></span>
<span data-ttu-id="79aa0-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79aa0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79aa0-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79aa0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79aa0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79aa0-146">CommonParameters</span></span>
<span data-ttu-id="79aa0-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79aa0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79aa0-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79aa0-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79aa0-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79aa0-149">INPUTS</span></span>

### <span data-ttu-id="79aa0-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="79aa0-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="79aa0-151">System. String</span><span class="sxs-lookup"><span data-stu-id="79aa0-151">System.String</span></span>

## <span data-ttu-id="79aa0-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79aa0-152">OUTPUTS</span></span>

### <span data-ttu-id="79aa0-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="79aa0-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="79aa0-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="79aa0-154">NOTES</span></span>

## <span data-ttu-id="79aa0-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79aa0-155">RELATED LINKS</span></span>