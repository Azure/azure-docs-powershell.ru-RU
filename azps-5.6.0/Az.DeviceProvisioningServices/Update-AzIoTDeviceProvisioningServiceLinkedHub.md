---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 4065e44d9ec0ed2512438356231176a1de10e7aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985057"
---
# <span data-ttu-id="5fe53-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="5fe53-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="5fe53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fe53-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe53-103">Обновление связанного концентратора IoT в службе по подготовка устройств для Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="5fe53-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5fe53-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5fe53-104">SYNTAX</span></span>

### <span data-ttu-id="5fe53-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5fe53-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fe53-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5fe53-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fe53-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5fe53-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fe53-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fe53-108">DESCRIPTION</span></span>
<span data-ttu-id="5fe53-109">Введение в службу по подготовкам устройств через Azure IoT см. в https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5fe53-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5fe53-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5fe53-110">EXAMPLES</span></span>

### <span data-ttu-id="5fe53-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5fe53-111">Example 1</span></span>
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

<span data-ttu-id="5fe53-112">Обновление связанного концентратора IoT "myiothub.azure-devices.net" в службе по подготовкам устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="5fe53-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5fe53-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fe53-113">PARAMETERS</span></span>

### <span data-ttu-id="5fe53-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="5fe53-114">-AllocationWeight</span></span>
<span data-ttu-id="5fe53-115">Вес выделения для концентратора IoT</span><span class="sxs-lookup"><span data-stu-id="5fe53-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="5fe53-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="5fe53-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="5fe53-117">Применение политики выделения к центру IoT</span><span class="sxs-lookup"><span data-stu-id="5fe53-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="5fe53-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe53-118">-DefaultProfile</span></span>
<span data-ttu-id="5fe53-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe53-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fe53-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fe53-120">-InputObject</span></span>
<span data-ttu-id="5fe53-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="5fe53-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5fe53-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="5fe53-122">-LinkedHubName</span></span>
<span data-ttu-id="5fe53-123">Host name of linked IoT Hub</span><span class="sxs-lookup"><span data-stu-id="5fe53-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="5fe53-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5fe53-124">-Name</span></span>
<span data-ttu-id="5fe53-125">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="5fe53-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5fe53-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe53-126">-ResourceGroupName</span></span>
<span data-ttu-id="5fe53-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5fe53-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5fe53-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fe53-128">-ResourceId</span></span>
<span data-ttu-id="5fe53-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="5fe53-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5fe53-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fe53-130">-Confirm</span></span>
<span data-ttu-id="5fe53-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5fe53-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fe53-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fe53-132">-WhatIf</span></span>
<span data-ttu-id="5fe53-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fe53-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fe53-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5fe53-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fe53-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe53-135">CommonParameters</span></span>
<span data-ttu-id="5fe53-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe53-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe53-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fe53-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe53-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fe53-138">INPUTS</span></span>

### <span data-ttu-id="5fe53-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="5fe53-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="5fe53-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5fe53-140">System.String</span></span>

## <span data-ttu-id="5fe53-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5fe53-141">OUTPUTS</span></span>

### <span data-ttu-id="5fe53-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="5fe53-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="5fe53-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5fe53-143">NOTES</span></span>

## <span data-ttu-id="5fe53-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fe53-144">RELATED LINKS</span></span>
