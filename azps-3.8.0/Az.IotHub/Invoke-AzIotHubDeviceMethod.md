---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073816"
---
# <span data-ttu-id="a125a-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="a125a-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="a125a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a125a-102">SYNOPSIS</span></span>
<span data-ttu-id="a125a-103">Вызовите прямой метод на устройстве.</span><span class="sxs-lookup"><span data-stu-id="a125a-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="a125a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a125a-104">SYNTAX</span></span>

### <span data-ttu-id="a125a-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a125a-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a125a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a125a-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a125a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a125a-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a125a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a125a-108">DESCRIPTION</span></span>
<span data-ttu-id="a125a-109">Вызовите прямой метод на устройстве.</span><span class="sxs-lookup"><span data-stu-id="a125a-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="a125a-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="a125a-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="a125a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a125a-111">EXAMPLES</span></span>

### <span data-ttu-id="a125a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a125a-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="a125a-113">Вызовите метод устройства.</span><span class="sxs-lookup"><span data-stu-id="a125a-113">Invoke a device method.</span></span>

## <span data-ttu-id="a125a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a125a-114">PARAMETERS</span></span>

### <span data-ttu-id="a125a-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="a125a-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="a125a-116">Время (в секундах), по истечении которого соединение будет установлено.</span><span class="sxs-lookup"><span data-stu-id="a125a-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="a125a-117">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="a125a-117">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a125a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a125a-118">-DefaultProfile</span></span>
<span data-ttu-id="a125a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a125a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a125a-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a125a-120">-DeviceId</span></span>
<span data-ttu-id="a125a-121">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="a125a-121">Target Device Id.</span></span>

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

### <span data-ttu-id="a125a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a125a-122">-InputObject</span></span>
<span data-ttu-id="a125a-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="a125a-123">IotHub object</span></span>

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

### <span data-ttu-id="a125a-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a125a-124">-IotHubName</span></span>
<span data-ttu-id="a125a-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="a125a-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a125a-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a125a-126">-Name</span></span>
<span data-ttu-id="a125a-127">Имя метода, который нужно вызвать на этом устройстве.</span><span class="sxs-lookup"><span data-stu-id="a125a-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="a125a-128">-Полезные данные</span><span class="sxs-lookup"><span data-stu-id="a125a-128">-Payload</span></span>
<span data-ttu-id="a125a-129">Полезные данные для метода, который нужно вызвать на этом устройстве.</span><span class="sxs-lookup"><span data-stu-id="a125a-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="a125a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a125a-130">-ResourceGroupName</span></span>
<span data-ttu-id="a125a-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a125a-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a125a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a125a-132">-ResourceId</span></span>
<span data-ttu-id="a125a-133">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="a125a-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a125a-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="a125a-134">-ResponseTimeOut</span></span>
<span data-ttu-id="a125a-135">Количество секунд, в течение которого ожидается получение результата из прямого метода.</span><span class="sxs-lookup"><span data-stu-id="a125a-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="a125a-136">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="a125a-136">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a125a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a125a-137">-Confirm</span></span>
<span data-ttu-id="a125a-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a125a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a125a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a125a-139">-WhatIf</span></span>
<span data-ttu-id="a125a-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a125a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a125a-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a125a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a125a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a125a-142">CommonParameters</span></span>
<span data-ttu-id="a125a-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a125a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a125a-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a125a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a125a-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a125a-145">INPUTS</span></span>

### <span data-ttu-id="a125a-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a125a-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a125a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a125a-147">System.String</span></span>

## <span data-ttu-id="a125a-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a125a-148">OUTPUTS</span></span>

### <span data-ttu-id="a125a-149">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="a125a-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="a125a-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="a125a-150">NOTES</span></span>

## <span data-ttu-id="a125a-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a125a-151">RELATED LINKS</span></span>
