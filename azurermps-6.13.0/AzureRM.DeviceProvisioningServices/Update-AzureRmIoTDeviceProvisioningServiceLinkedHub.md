---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b3cd05b286ddfef69228b8aae12e222e5fffd4d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564560"
---
# <span data-ttu-id="f88dc-101">Update-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="f88dc-101">Update-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="f88dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f88dc-102">SYNOPSIS</span></span>
<span data-ttu-id="f88dc-103">Обновите связанный центр Интернета вещей в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="f88dc-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f88dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f88dc-104">SYNTAX</span></span>

### <span data-ttu-id="f88dc-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f88dc-105">ResourceSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f88dc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f88dc-106">InputObjectSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f88dc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f88dc-107">ResourceIdSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f88dc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f88dc-108">DESCRIPTION</span></span>
<span data-ttu-id="f88dc-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="f88dc-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="f88dc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f88dc-110">EXAMPLES</span></span>

### <span data-ttu-id="f88dc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f88dc-111">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="f88dc-112">Обновите связанный центр Интернета вещей "myiothub.azure-devices.net" в службе подготовки устройств центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="f88dc-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="f88dc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f88dc-113">PARAMETERS</span></span>

### <span data-ttu-id="f88dc-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="f88dc-114">-AllocationWeight</span></span>
<span data-ttu-id="f88dc-115">Плотность выделения для центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="f88dc-115">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88dc-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="f88dc-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="f88dc-117">Применение политики выделения к концентратору Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="f88dc-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="f88dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88dc-118">-DefaultProfile</span></span>
<span data-ttu-id="f88dc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f88dc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88dc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f88dc-120">-InputObject</span></span>
<span data-ttu-id="f88dc-121">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="f88dc-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f88dc-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="f88dc-122">-LinkedHubName</span></span>
<span data-ttu-id="f88dc-123">Имя узла для связанного центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="f88dc-123">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f88dc-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f88dc-124">-Name</span></span>
<span data-ttu-id="f88dc-125">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="f88dc-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f88dc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f88dc-126">-ResourceGroupName</span></span>
<span data-ttu-id="f88dc-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f88dc-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f88dc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f88dc-128">-ResourceId</span></span>
<span data-ttu-id="f88dc-129">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="f88dc-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f88dc-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f88dc-130">-Confirm</span></span>
<span data-ttu-id="f88dc-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f88dc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f88dc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f88dc-132">-WhatIf</span></span>
<span data-ttu-id="f88dc-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f88dc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f88dc-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f88dc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f88dc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88dc-135">CommonParameters</span></span>
<span data-ttu-id="f88dc-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f88dc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88dc-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f88dc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88dc-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f88dc-138">INPUTS</span></span>

### <span data-ttu-id="f88dc-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="f88dc-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>
<span data-ttu-id="f88dc-140">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f88dc-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f88dc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f88dc-141">System.String</span></span>

## <span data-ttu-id="f88dc-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f88dc-142">OUTPUTS</span></span>

### <span data-ttu-id="f88dc-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="f88dc-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="f88dc-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="f88dc-144">NOTES</span></span>

## <span data-ttu-id="f88dc-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f88dc-145">RELATED LINKS</span></span>
