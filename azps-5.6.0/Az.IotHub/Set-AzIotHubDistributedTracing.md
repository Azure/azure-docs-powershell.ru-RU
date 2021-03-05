---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: b1bdc6b5910f47fdca8e8b66ab99939945547a08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004136"
---
# <span data-ttu-id="55c6b-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="55c6b-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="55c6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="55c6b-103">Обновив параметры распределенной трасситуры для устройства.</span><span class="sxs-lookup"><span data-stu-id="55c6b-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="55c6b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="55c6b-104">SYNTAX</span></span>

### <span data-ttu-id="55c6b-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55c6b-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55c6b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="55c6b-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55c6b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="55c6b-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55c6b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55c6b-108">DESCRIPTION</span></span>
<span data-ttu-id="55c6b-109">Обновив параметры распределенной трасситуры для устройства.</span><span class="sxs-lookup"><span data-stu-id="55c6b-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="55c6b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="55c6b-110">EXAMPLES</span></span>

### <span data-ttu-id="55c6b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55c6b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="55c6b-112">Обновив параметры распределенной трасситуры для устройства.</span><span class="sxs-lookup"><span data-stu-id="55c6b-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="55c6b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55c6b-113">PARAMETERS</span></span>

### <span data-ttu-id="55c6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c6b-114">-DefaultProfile</span></span>
<span data-ttu-id="55c6b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55c6b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55c6b-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="55c6b-116">-DeviceId</span></span>
<span data-ttu-id="55c6b-117">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="55c6b-117">Target Device Id.</span></span>

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

### <span data-ttu-id="55c6b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55c6b-118">-InputObject</span></span>
<span data-ttu-id="55c6b-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="55c6b-119">IotHub object</span></span>

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

### <span data-ttu-id="55c6b-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="55c6b-120">-IotHubName</span></span>
<span data-ttu-id="55c6b-121">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="55c6b-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="55c6b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55c6b-122">-ResourceGroupName</span></span>
<span data-ttu-id="55c6b-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="55c6b-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="55c6b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55c6b-124">-ResourceId</span></span>
<span data-ttu-id="55c6b-125">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="55c6b-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="55c6b-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="55c6b-126">-SamplingMode</span></span>
<span data-ttu-id="55c6b-127">Включает и отключает выборку для распределенной трасситуры.</span><span class="sxs-lookup"><span data-stu-id="55c6b-127">Turns sampling for distributed tracing enable and disable.</span></span>

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

### <span data-ttu-id="55c6b-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="55c6b-128">-SamplingRate</span></span>
<span data-ttu-id="55c6b-129">Управляет количеством сообщений, взятых из примера для добавления контекста трассировки.</span><span class="sxs-lookup"><span data-stu-id="55c6b-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="55c6b-130">Это значение является процентным значением.</span><span class="sxs-lookup"><span data-stu-id="55c6b-130">This value is a percentage.</span></span>
<span data-ttu-id="55c6b-131">Допускается только значение от 0 до 100 (включительно).</span><span class="sxs-lookup"><span data-stu-id="55c6b-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

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

### <span data-ttu-id="55c6b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55c6b-132">-Confirm</span></span>
<span data-ttu-id="55c6b-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c6b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55c6b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55c6b-134">-WhatIf</span></span>
<span data-ttu-id="55c6b-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c6b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55c6b-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="55c6b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55c6b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c6b-137">CommonParameters</span></span>
<span data-ttu-id="55c6b-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55c6b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c6b-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c6b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c6b-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55c6b-140">INPUTS</span></span>

### <span data-ttu-id="55c6b-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="55c6b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="55c6b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="55c6b-142">System.String</span></span>

## <span data-ttu-id="55c6b-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55c6b-143">OUTPUTS</span></span>

### <span data-ttu-id="55c6b-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="55c6b-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="55c6b-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="55c6b-145">NOTES</span></span>

## <span data-ttu-id="55c6b-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55c6b-146">RELATED LINKS</span></span>
