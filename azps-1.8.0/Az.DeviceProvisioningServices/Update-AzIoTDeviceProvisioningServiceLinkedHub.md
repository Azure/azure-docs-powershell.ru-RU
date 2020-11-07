---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: d941e59c3d0681b91cdef9d05617c665dcc83177
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730905"
---
# <span data-ttu-id="f4ebf-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="f4ebf-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="f4ebf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ebf-103">Обновите связанный центр Интернета вещей в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="f4ebf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4ebf-104">SYNTAX</span></span>

### <span data-ttu-id="f4ebf-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4ebf-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ebf-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f4ebf-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ebf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f4ebf-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ebf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4ebf-108">DESCRIPTION</span></span>
<span data-ttu-id="f4ebf-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="f4ebf-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="f4ebf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4ebf-110">EXAMPLES</span></span>

### <span data-ttu-id="f4ebf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4ebf-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="f4ebf-112">Обновите связанный центр Интернета вещей "myiothub.azure-devices.net" в службе подготовки устройств центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="f4ebf-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4ebf-113">PARAMETERS</span></span>

### <span data-ttu-id="f4ebf-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="f4ebf-114">-AllocationWeight</span></span>
<span data-ttu-id="f4ebf-115">Плотность выделения для центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="f4ebf-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="f4ebf-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ebf-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="f4ebf-117">Применение политики выделения к концентратору Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="f4ebf-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="f4ebf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ebf-118">-DefaultProfile</span></span>
<span data-ttu-id="f4ebf-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4ebf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4ebf-120">-InputObject</span></span>
<span data-ttu-id="f4ebf-121">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="f4ebf-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="f4ebf-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="f4ebf-122">-LinkedHubName</span></span>
<span data-ttu-id="f4ebf-123">Имя узла для связанного центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="f4ebf-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="f4ebf-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4ebf-124">-Name</span></span>
<span data-ttu-id="f4ebf-125">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="f4ebf-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f4ebf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ebf-126">-ResourceGroupName</span></span>
<span data-ttu-id="f4ebf-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f4ebf-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f4ebf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4ebf-128">-ResourceId</span></span>
<span data-ttu-id="f4ebf-129">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="f4ebf-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f4ebf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4ebf-130">-Confirm</span></span>
<span data-ttu-id="f4ebf-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ebf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ebf-132">-WhatIf</span></span>
<span data-ttu-id="f4ebf-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4ebf-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4ebf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ebf-135">CommonParameters</span></span>
<span data-ttu-id="f4ebf-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4ebf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ebf-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ebf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ebf-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4ebf-138">INPUTS</span></span>

### <span data-ttu-id="f4ebf-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="f4ebf-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="f4ebf-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f4ebf-140">System.String</span></span>

## <span data-ttu-id="f4ebf-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4ebf-141">OUTPUTS</span></span>

### <span data-ttu-id="f4ebf-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="f4ebf-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="f4ebf-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4ebf-143">NOTES</span></span>

## <span data-ttu-id="f4ebf-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4ebf-144">RELATED LINKS</span></span>
