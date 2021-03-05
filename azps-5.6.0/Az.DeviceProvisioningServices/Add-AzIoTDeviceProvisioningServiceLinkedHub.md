---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 8b5a42110c99a4572b411d082879f4f2853bac0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983555"
---
# <span data-ttu-id="478d0-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="478d0-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="478d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="478d0-102">SYNOPSIS</span></span>
<span data-ttu-id="478d0-103">Центр, связанный с IoT-концентратором Azure IoT Hub, службой по подготовка устройств.</span><span class="sxs-lookup"><span data-stu-id="478d0-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="478d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="478d0-104">SYNTAX</span></span>

### <span data-ttu-id="478d0-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="478d0-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478d0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="478d0-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478d0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="478d0-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="478d0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="478d0-108">DESCRIPTION</span></span>
<span data-ttu-id="478d0-109">Введение в службу по подготовкам устройств в Azure IoT Hub см. в https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="478d0-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="478d0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="478d0-110">EXAMPLES</span></span>

### <span data-ttu-id="478d0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="478d0-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="478d0-112">Центр, связанный с IoT-концентратором Azure IoT Hub, службой по подготовка устройств.</span><span class="sxs-lookup"><span data-stu-id="478d0-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="478d0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="478d0-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="478d0-114">Центр, связанный с IoT-концентратором Azure, с службой по обслуживанию предварительной оценки устройства в Azure IoT, где задействовать AllocationWeight и ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="478d0-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="478d0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="478d0-115">PARAMETERS</span></span>

### <span data-ttu-id="478d0-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="478d0-116">-AllocationWeight</span></span>
<span data-ttu-id="478d0-117">Вес выделения для концентратора IoT</span><span class="sxs-lookup"><span data-stu-id="478d0-117">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="478d0-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="478d0-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="478d0-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span><span class="sxs-lookup"><span data-stu-id="478d0-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="478d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478d0-120">-DefaultProfile</span></span>
<span data-ttu-id="478d0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="478d0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="478d0-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="478d0-122">-DpsObject</span></span>
<span data-ttu-id="478d0-123">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="478d0-123">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="478d0-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="478d0-124">-IotHubConnectionString</span></span>
<span data-ttu-id="478d0-125">Строка подключения ресурса концентратора IOT.</span><span class="sxs-lookup"><span data-stu-id="478d0-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="478d0-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="478d0-126">-IotHubLocation</span></span>
<span data-ttu-id="478d0-127">Расположение концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="478d0-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478d0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="478d0-128">-Name</span></span>
<span data-ttu-id="478d0-129">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="478d0-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="478d0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="478d0-130">-ResourceGroupName</span></span>
<span data-ttu-id="478d0-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="478d0-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="478d0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="478d0-132">-ResourceId</span></span>
<span data-ttu-id="478d0-133">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="478d0-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="478d0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="478d0-134">-Confirm</span></span>
<span data-ttu-id="478d0-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="478d0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="478d0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="478d0-136">-WhatIf</span></span>
<span data-ttu-id="478d0-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="478d0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="478d0-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="478d0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="478d0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478d0-139">CommonParameters</span></span>
<span data-ttu-id="478d0-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="478d0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478d0-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="478d0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478d0-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="478d0-142">INPUTS</span></span>

### <span data-ttu-id="478d0-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="478d0-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="478d0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="478d0-144">System.String</span></span>

## <span data-ttu-id="478d0-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="478d0-145">OUTPUTS</span></span>

### <span data-ttu-id="478d0-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="478d0-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="478d0-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="478d0-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="478d0-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="478d0-148">NOTES</span></span>

## <span data-ttu-id="478d0-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="478d0-149">RELATED LINKS</span></span>
