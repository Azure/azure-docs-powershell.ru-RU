---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 16c3ab31959268aa998d50290180d4d8b3231ccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312410"
---
# <span data-ttu-id="d80e6-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="d80e6-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="d80e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d80e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d80e6-103">Обновляет Теги и нужные свойства двойной устройства.</span><span class="sxs-lookup"><span data-stu-id="d80e6-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="d80e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d80e6-104">SYNTAX</span></span>

### <span data-ttu-id="d80e6-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d80e6-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d80e6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d80e6-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d80e6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d80e6-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d80e6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d80e6-108">DESCRIPTION</span></span>
<span data-ttu-id="d80e6-109">Обновляет или заменяет двойной устройства.</span><span class="sxs-lookup"><span data-stu-id="d80e6-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="d80e6-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twinsДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="d80e6-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="d80e6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d80e6-111">EXAMPLES</span></span>

### <span data-ttu-id="d80e6-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d80e6-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="d80e6-113">Возвращает обновленный объект устройства двойной.</span><span class="sxs-lookup"><span data-stu-id="d80e6-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="d80e6-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d80e6-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="d80e6-115">Возвращает объект Device двойной с обновленными необходимыми свойствами.</span><span class="sxs-lookup"><span data-stu-id="d80e6-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="d80e6-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d80e6-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="d80e6-117">Возвращает объект Device двойной с обновленным свойством Tags.</span><span class="sxs-lookup"><span data-stu-id="d80e6-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="d80e6-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d80e6-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="d80e6-119">Возвращает замененный объект устройства двойной.</span><span class="sxs-lookup"><span data-stu-id="d80e6-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="d80e6-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d80e6-120">PARAMETERS</span></span>

### <span data-ttu-id="d80e6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80e6-121">-DefaultProfile</span></span>
<span data-ttu-id="d80e6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d80e6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d80e6-123">-Необходимый</span><span class="sxs-lookup"><span data-stu-id="d80e6-123">-Desired</span></span>
<span data-ttu-id="d80e6-124">Добавьте или обновите нужное свойство в двойной устройства.</span><span class="sxs-lookup"><span data-stu-id="d80e6-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="d80e6-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d80e6-125">-DeviceId</span></span>
<span data-ttu-id="d80e6-126">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="d80e6-126">Target Device Id.</span></span>

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

### <span data-ttu-id="d80e6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d80e6-127">-InputObject</span></span>
<span data-ttu-id="d80e6-128">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="d80e6-128">IotHub object</span></span>

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

### <span data-ttu-id="d80e6-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d80e6-129">-IotHubName</span></span>
<span data-ttu-id="d80e6-130">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="d80e6-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d80e6-131">-Partial</span><span class="sxs-lookup"><span data-stu-id="d80e6-131">-Partial</span></span>
<span data-ttu-id="d80e6-132">Позволяет только частично обновлять Теги и нужные свойства двойной устройства.</span><span class="sxs-lookup"><span data-stu-id="d80e6-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="d80e6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d80e6-133">-ResourceGroupName</span></span>
<span data-ttu-id="d80e6-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d80e6-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d80e6-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d80e6-135">-ResourceId</span></span>
<span data-ttu-id="d80e6-136">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="d80e6-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d80e6-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="d80e6-137">-Tag</span></span>
<span data-ttu-id="d80e6-138">Добавьте или обновите свойство Tags в двойнойе устройства.</span><span class="sxs-lookup"><span data-stu-id="d80e6-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="d80e6-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d80e6-139">-Confirm</span></span>
<span data-ttu-id="d80e6-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d80e6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d80e6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d80e6-141">-WhatIf</span></span>
<span data-ttu-id="d80e6-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d80e6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d80e6-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d80e6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d80e6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80e6-144">CommonParameters</span></span>
<span data-ttu-id="d80e6-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d80e6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80e6-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d80e6-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80e6-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d80e6-147">INPUTS</span></span>

### <span data-ttu-id="d80e6-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d80e6-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d80e6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d80e6-149">System.String</span></span>

## <span data-ttu-id="d80e6-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d80e6-150">OUTPUTS</span></span>

### <span data-ttu-id="d80e6-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d80e6-151">System.String</span></span>

## <span data-ttu-id="d80e6-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="d80e6-152">NOTES</span></span>

## <span data-ttu-id="d80e6-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d80e6-153">RELATED LINKS</span></span>
