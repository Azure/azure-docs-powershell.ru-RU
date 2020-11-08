---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: 818e973d4d7be9fb03e23a23d7264745920f843f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073819"
---
# <span data-ttu-id="8b872-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="8b872-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="8b872-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b872-102">SYNOPSIS</span></span>
<span data-ttu-id="8b872-103">Вызовите метод Edge Module.</span><span class="sxs-lookup"><span data-stu-id="8b872-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="8b872-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b872-104">SYNTAX</span></span>

### <span data-ttu-id="8b872-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b872-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b872-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8b872-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b872-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8b872-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b872-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b872-108">DESCRIPTION</span></span>
<span data-ttu-id="8b872-109">Вызовите метод Edge Module.</span><span class="sxs-lookup"><span data-stu-id="8b872-109">Invoke an Edge module method.</span></span> <span data-ttu-id="8b872-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="8b872-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="8b872-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b872-111">EXAMPLES</span></span>

### <span data-ttu-id="8b872-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b872-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="8b872-113">Вызовите метод Edge Module.</span><span class="sxs-lookup"><span data-stu-id="8b872-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="8b872-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b872-114">PARAMETERS</span></span>

### <span data-ttu-id="8b872-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="8b872-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="8b872-116">Время (в секундах), по истечении которого соединение будет установлено.</span><span class="sxs-lookup"><span data-stu-id="8b872-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="8b872-117">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="8b872-117">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b872-118">-DefaultProfile</span></span>
<span data-ttu-id="8b872-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b872-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8b872-120">-DeviceId</span></span>
<span data-ttu-id="8b872-121">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="8b872-121">Target Device Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b872-122">-InputObject</span></span>
<span data-ttu-id="8b872-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="8b872-123">IotHub object</span></span>

```yaml
Type: PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8b872-124">-IotHubName</span></span>
<span data-ttu-id="8b872-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="8b872-125">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="8b872-126">-ModuleId</span></span>
<span data-ttu-id="8b872-127">Идентификатор модуля целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="8b872-127">Target device's module id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b872-128">-Name</span></span>
<span data-ttu-id="8b872-129">Имя метода, который нужно вызвать для этого модуля устройства.</span><span class="sxs-lookup"><span data-stu-id="8b872-129">The name of the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-130">-Полезные данные</span><span class="sxs-lookup"><span data-stu-id="8b872-130">-Payload</span></span>
<span data-ttu-id="8b872-131">Полезные данные для метода, который нужно вызвать для этого модуля устройства.</span><span class="sxs-lookup"><span data-stu-id="8b872-131">The payload for the method to invoke on this device module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b872-132">-ResourceGroupName</span></span>
<span data-ttu-id="8b872-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8b872-133">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b872-134">-ResourceId</span></span>
<span data-ttu-id="8b872-135">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="8b872-135">IotHub Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="8b872-136">-ResponseTimeOut</span></span>
<span data-ttu-id="8b872-137">Количество секунд, в течение которого ожидается получение результата из прямого метода.</span><span class="sxs-lookup"><span data-stu-id="8b872-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="8b872-138">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="8b872-138">Default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b872-139">-Confirm</span></span>
<span data-ttu-id="8b872-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b872-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b872-141">-WhatIf</span></span>
<span data-ttu-id="8b872-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b872-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b872-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b872-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b872-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b872-144">CommonParameters</span></span>
<span data-ttu-id="8b872-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b872-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8b872-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b872-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b872-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b872-147">INPUTS</span></span>

### <span data-ttu-id="8b872-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8b872-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8b872-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8b872-149">System.String</span></span>

## <span data-ttu-id="8b872-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b872-150">OUTPUTS</span></span>

### <span data-ttu-id="8b872-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="8b872-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="8b872-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b872-152">NOTES</span></span>

## <span data-ttu-id="8b872-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b872-153">RELATED LINKS</span></span>
