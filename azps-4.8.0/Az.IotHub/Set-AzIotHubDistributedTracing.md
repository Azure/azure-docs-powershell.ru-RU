---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079611"
---
# <span data-ttu-id="8bdf2-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="8bdf2-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="8bdf2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8bdf2-102">SYNOPSIS</span></span>
<span data-ttu-id="8bdf2-103">Обновите параметры распределенной трассировки для устройства.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="8bdf2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8bdf2-104">SYNTAX</span></span>

### <span data-ttu-id="8bdf2-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8bdf2-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bdf2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8bdf2-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bdf2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8bdf2-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bdf2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bdf2-108">DESCRIPTION</span></span>
<span data-ttu-id="8bdf2-109">Обновите параметры распределенной трассировки для устройства.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="8bdf2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8bdf2-110">EXAMPLES</span></span>

### <span data-ttu-id="8bdf2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8bdf2-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="8bdf2-112">Обновите параметры распределенной трассировки для устройства.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="8bdf2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8bdf2-113">PARAMETERS</span></span>

### <span data-ttu-id="8bdf2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bdf2-114">-DefaultProfile</span></span>
<span data-ttu-id="8bdf2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bdf2-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8bdf2-116">-DeviceId</span></span>
<span data-ttu-id="8bdf2-117">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-117">Target Device Id.</span></span>

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

### <span data-ttu-id="8bdf2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bdf2-118">-InputObject</span></span>
<span data-ttu-id="8bdf2-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="8bdf2-119">IotHub object</span></span>

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

### <span data-ttu-id="8bdf2-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8bdf2-120">-IotHubName</span></span>
<span data-ttu-id="8bdf2-121">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="8bdf2-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8bdf2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bdf2-122">-ResourceGroupName</span></span>
<span data-ttu-id="8bdf2-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8bdf2-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8bdf2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bdf2-124">-ResourceId</span></span>
<span data-ttu-id="8bdf2-125">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="8bdf2-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8bdf2-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="8bdf2-126">-SamplingMode</span></span>
<span data-ttu-id="8bdf2-127">Включает выборку для распределенной трассировки и отключения.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-127">Turns sampling for distributed tracing enable and disable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDistributedTracingSamplingMode
Parameter Sets: (All)
Aliases: Mode
Accepted values: Disabled, Enabled

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdf2-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="8bdf2-128">-SamplingRate</span></span>
<span data-ttu-id="8bdf2-129">Определяет количество сообщений, выданных для добавления контекста трассировки.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="8bdf2-130">Это значение равно проценту.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-130">This value is a percentage.</span></span>
<span data-ttu-id="8bdf2-131">Разрешены только значения от 0 до 100 (включительно).</span><span class="sxs-lookup"><span data-stu-id="8bdf2-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Rate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdf2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bdf2-132">-Confirm</span></span>
<span data-ttu-id="8bdf2-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bdf2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bdf2-134">-WhatIf</span></span>
<span data-ttu-id="8bdf2-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bdf2-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bdf2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bdf2-137">CommonParameters</span></span>
<span data-ttu-id="8bdf2-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bdf2-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bdf2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bdf2-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8bdf2-140">INPUTS</span></span>

### <span data-ttu-id="8bdf2-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8bdf2-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8bdf2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8bdf2-142">System.String</span></span>

## <span data-ttu-id="8bdf2-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bdf2-143">OUTPUTS</span></span>

### <span data-ttu-id="8bdf2-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="8bdf2-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="8bdf2-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="8bdf2-145">NOTES</span></span>

## <span data-ttu-id="8bdf2-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bdf2-146">RELATED LINKS</span></span>
