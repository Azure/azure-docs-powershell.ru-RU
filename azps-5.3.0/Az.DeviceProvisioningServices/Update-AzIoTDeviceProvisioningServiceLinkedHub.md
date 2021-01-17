---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: cc8d2ec0602213bdbfd50ac89e5199952cea424c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420436"
---
# <span data-ttu-id="92c9c-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="92c9c-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="92c9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="92c9c-103">Обновление связанного концентратора IoT в службе по подготовка устройств для Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="92c9c-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="92c9c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92c9c-104">SYNTAX</span></span>

### <span data-ttu-id="92c9c-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92c9c-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92c9c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="92c9c-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92c9c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="92c9c-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92c9c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92c9c-108">DESCRIPTION</span></span>
<span data-ttu-id="92c9c-109">Введение в службу по подготовкам устройств через Azure IoT см. в https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="92c9c-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="92c9c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92c9c-110">EXAMPLES</span></span>

### <span data-ttu-id="92c9c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92c9c-111">Example 1</span></span>
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

<span data-ttu-id="92c9c-112">Обновление связанного концентратора IoT "myiothub.azure-devices.net" в службе по подготовкам устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="92c9c-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="92c9c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92c9c-113">PARAMETERS</span></span>

### <span data-ttu-id="92c9c-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="92c9c-114">-AllocationWeight</span></span>
<span data-ttu-id="92c9c-115">Вес выделения для концентратора IoT</span><span class="sxs-lookup"><span data-stu-id="92c9c-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="92c9c-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="92c9c-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="92c9c-117">Применение политики выделения к центру IoT</span><span class="sxs-lookup"><span data-stu-id="92c9c-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="92c9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92c9c-118">-DefaultProfile</span></span>
<span data-ttu-id="92c9c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92c9c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92c9c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92c9c-120">-InputObject</span></span>
<span data-ttu-id="92c9c-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="92c9c-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="92c9c-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="92c9c-122">-LinkedHubName</span></span>
<span data-ttu-id="92c9c-123">Host name of linked IoT Hub</span><span class="sxs-lookup"><span data-stu-id="92c9c-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="92c9c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="92c9c-124">-Name</span></span>
<span data-ttu-id="92c9c-125">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="92c9c-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="92c9c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92c9c-126">-ResourceGroupName</span></span>
<span data-ttu-id="92c9c-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="92c9c-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="92c9c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92c9c-128">-ResourceId</span></span>
<span data-ttu-id="92c9c-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="92c9c-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="92c9c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92c9c-130">-Confirm</span></span>
<span data-ttu-id="92c9c-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="92c9c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92c9c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92c9c-132">-WhatIf</span></span>
<span data-ttu-id="92c9c-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92c9c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92c9c-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="92c9c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92c9c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92c9c-135">CommonParameters</span></span>
<span data-ttu-id="92c9c-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92c9c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92c9c-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92c9c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92c9c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92c9c-138">INPUTS</span></span>

### <span data-ttu-id="92c9c-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="92c9c-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="92c9c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="92c9c-140">System.String</span></span>

## <span data-ttu-id="92c9c-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92c9c-141">OUTPUTS</span></span>

### <span data-ttu-id="92c9c-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="92c9c-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="92c9c-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92c9c-143">NOTES</span></span>

## <span data-ttu-id="92c9c-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92c9c-144">RELATED LINKS</span></span>
