---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245328"
---
# <span data-ttu-id="f793b-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="f793b-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="f793b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f793b-102">SYNOPSIS</span></span>
<span data-ttu-id="f793b-103">Удаление устройства центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f793b-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="f793b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f793b-104">SYNTAX</span></span>

### <span data-ttu-id="f793b-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f793b-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f793b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f793b-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f793b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f793b-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f793b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f793b-108">DESCRIPTION</span></span>
<span data-ttu-id="f793b-109">Удаление всех устройств или определенного устройства из центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f793b-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="f793b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f793b-110">EXAMPLES</span></span>

### <span data-ttu-id="f793b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f793b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="f793b-112">Удалите все устройства центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f793b-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="f793b-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f793b-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="f793b-114">Удаление устройства центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="f793b-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="f793b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f793b-115">PARAMETERS</span></span>

### <span data-ttu-id="f793b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f793b-116">-DefaultProfile</span></span>
<span data-ttu-id="f793b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f793b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f793b-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f793b-118">-DeviceId</span></span>
<span data-ttu-id="f793b-119">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="f793b-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f793b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f793b-120">-InputObject</span></span>
<span data-ttu-id="f793b-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="f793b-121">IotHub object</span></span>

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

### <span data-ttu-id="f793b-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f793b-122">-IotHubName</span></span>
<span data-ttu-id="f793b-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="f793b-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f793b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f793b-124">-PassThru</span></span>
<span data-ttu-id="f793b-125">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="f793b-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="f793b-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f793b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f793b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f793b-127">-ResourceGroupName</span></span>
<span data-ttu-id="f793b-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f793b-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f793b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f793b-129">-ResourceId</span></span>
<span data-ttu-id="f793b-130">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="f793b-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f793b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f793b-131">-Confirm</span></span>
<span data-ttu-id="f793b-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f793b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f793b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f793b-133">-WhatIf</span></span>
<span data-ttu-id="f793b-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f793b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f793b-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f793b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f793b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f793b-136">CommonParameters</span></span>
<span data-ttu-id="f793b-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f793b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f793b-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f793b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f793b-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f793b-139">INPUTS</span></span>

### <span data-ttu-id="f793b-140">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f793b-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f793b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f793b-141">System.String</span></span>

## <span data-ttu-id="f793b-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f793b-142">OUTPUTS</span></span>

### <span data-ttu-id="f793b-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f793b-143">System.Boolean</span></span>

## <span data-ttu-id="f793b-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="f793b-144">NOTES</span></span>

## <span data-ttu-id="f793b-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f793b-145">RELATED LINKS</span></span>
