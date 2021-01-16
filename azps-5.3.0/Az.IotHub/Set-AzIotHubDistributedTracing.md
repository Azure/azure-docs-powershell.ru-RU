---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425940"
---
# <span data-ttu-id="0d0ce-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="0d0ce-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="0d0ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="0d0ce-103">Обновив параметры распределенной трасситуры для устройства.</span><span class="sxs-lookup"><span data-stu-id="0d0ce-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="0d0ce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0d0ce-104">SYNTAX</span></span>

### <span data-ttu-id="0d0ce-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d0ce-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d0ce-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0d0ce-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d0ce-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0d0ce-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d0ce-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d0ce-108">DESCRIPTION</span></span>
<span data-ttu-id="0d0ce-109">Обновив параметры распределенной трасситуры для устройства.</span><span class="sxs-lookup"><span data-stu-id="0d0ce-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="0d0ce-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0d0ce-110">EXAMPLES</span></span>

### <span data-ttu-id="0d0ce-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d0ce-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="0d0ce-112">Обновив параметры распределенной трасситуры для устройства.</span><span class="sxs-lookup"><span data-stu-id="0d0ce-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="0d0ce-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d0ce-113">PARAMETERS</span></span>

### <span data-ttu-id="0d0ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d0ce-114">-DefaultProfile</span></span>
<span data-ttu-id="0d0ce-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d0ce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d0ce-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="0d0ce-116">-DeviceId</span></span>
<span data-ttu-id="0d0ce-117">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="0d0ce-117">Target Device Id.</span></span>

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

### <span data-ttu-id="0d0ce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d0ce-118">-InputObject</span></span>
<span data-ttu-id="0d0ce-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="0d0ce-119">IotHub object</span></span>

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

### <span data-ttu-id="0d0ce-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0d0ce-120">-IotHubName</span></span>
<span data-ttu-id="0d0ce-121">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="0d0ce-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0d0ce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d0ce-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d0ce-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0d0ce-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0d0ce-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d0ce-124">-ResourceId</span></span>
<span data-ttu-id="0d0ce-125">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="0d0ce-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0d0ce-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="0d0ce-126">-SamplingMode</span></span>
<span data-ttu-id="0d0ce-127">Включает и отключает выборку для распределенной трасситуры.</span><span class="sxs-lookup"><span data-stu-id="0d0ce-127">Turns sampling for distributed tracing enable and disable.</span></span>

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

### <span data-ttu-id="0d0ce-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="0d0ce-128">-SamplingRate</span></span>
<span data-ttu-id="0d0ce-129">Управляет количеством сообщений, взятых из примера для добавления контекста трассировки.</span><span class="sxs-lookup"><span data-stu-id="0d0ce-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="0d0ce-130">Это значение является процентным значением.</span><span class="sxs-lookup"><span data-stu-id="0d0ce-130">This value is a percentage.</span></span>
<span data-ttu-id="0d0ce-131">Допускается только значение от 0 до 100 (включительно).</span><span class="sxs-lookup"><span data-stu-id="0d0ce-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

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

### <span data-ttu-id="0d0ce-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d0ce-132">-Confirm</span></span>
<span data-ttu-id="0d0ce-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d0ce-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d0ce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d0ce-134">-WhatIf</span></span>
<span data-ttu-id="0d0ce-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d0ce-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d0ce-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0d0ce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d0ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d0ce-137">CommonParameters</span></span>
<span data-ttu-id="0d0ce-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d0ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d0ce-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d0ce-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d0ce-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d0ce-140">INPUTS</span></span>

### <span data-ttu-id="0d0ce-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0d0ce-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0d0ce-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0d0ce-142">System.String</span></span>

## <span data-ttu-id="0d0ce-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0d0ce-143">OUTPUTS</span></span>

### <span data-ttu-id="0d0ce-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="0d0ce-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="0d0ce-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0d0ce-145">NOTES</span></span>

## <span data-ttu-id="0d0ce-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d0ce-146">RELATED LINKS</span></span>
