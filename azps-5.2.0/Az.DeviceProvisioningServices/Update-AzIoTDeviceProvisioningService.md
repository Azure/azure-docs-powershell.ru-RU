---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: f533bd07d0c7b123f1d109e7abd933736093cd79
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402535"
---
# <span data-ttu-id="8b9e1-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="8b9e1-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="8b9e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b9e1-102">SYNOPSIS</span></span>
<span data-ttu-id="8b9e1-103">Обновив службу по подготовкам устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="8b9e1-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="8b9e1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b9e1-104">SYNTAX</span></span>

### <span data-ttu-id="8b9e1-105">ResourceUpdateSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b9e1-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b9e1-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="8b9e1-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b9e1-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="8b9e1-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b9e1-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="8b9e1-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b9e1-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="8b9e1-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b9e1-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="8b9e1-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b9e1-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b9e1-111">DESCRIPTION</span></span>
<span data-ttu-id="8b9e1-112">Введение в службу по подготовкам устройств через Azure IoT см. в https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="8b9e1-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="8b9e1-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b9e1-113">EXAMPLES</span></span>

### <span data-ttu-id="8b9e1-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b9e1-114">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : GeoLatency
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="8b9e1-115">Обновив политику выделения на "GeoLatency" службы по подготовкам устройств через Azure IoT Hub "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="8b9e1-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="8b9e1-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8b9e1-116">Example 2</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tag

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="8b9e1-117">Добавьте теги в службу по подготовкам устройств azure IoT Hub "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="8b9e1-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="8b9e1-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8b9e1-118">Example 3</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag $tag -Reset

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAS1dY=
```

<span data-ttu-id="8b9e1-119">Удалите теги и добавьте новые теги в службу по подготовкам устройств Azure IoT Hub "myiotdps" с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="8b9e1-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="8b9e1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b9e1-120">PARAMETERS</span></span>

### <span data-ttu-id="8b9e1-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="8b9e1-121">-AllocationPolicy</span></span>
<span data-ttu-id="8b9e1-122">Политика выделения службы для подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="8b9e1-122">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectCreateUpdateSet, ResourceIdCreateUpdateSet, ResourceCreateUpdateSet
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9e1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b9e1-123">-DefaultProfile</span></span>
<span data-ttu-id="8b9e1-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b9e1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b9e1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b9e1-125">-InputObject</span></span>
<span data-ttu-id="8b9e1-126">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="8b9e1-126">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectUpdateSet, InputObjectCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9e1-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8b9e1-127">-Name</span></span>
<span data-ttu-id="8b9e1-128">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="8b9e1-128">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9e1-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="8b9e1-129">-Reset</span></span>
<span data-ttu-id="8b9e1-130">Сброс тегов службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="8b9e1-130">Reset IoT Device Provisioning Service Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9e1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b9e1-131">-ResourceGroupName</span></span>
<span data-ttu-id="8b9e1-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8b9e1-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9e1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b9e1-133">-ResourceId</span></span>
<span data-ttu-id="8b9e1-134">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="8b9e1-134">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdUpdateSet, ResourceIdCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b9e1-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b9e1-135">-Tag</span></span>
<span data-ttu-id="8b9e1-136">IoT Device Provisioning Service Tag collection</span><span class="sxs-lookup"><span data-stu-id="8b9e1-136">IoT Device Provisioning Service Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9e1-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b9e1-137">-Confirm</span></span>
<span data-ttu-id="8b9e1-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b9e1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b9e1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b9e1-139">-WhatIf</span></span>
<span data-ttu-id="8b9e1-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b9e1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b9e1-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8b9e1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b9e1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b9e1-142">CommonParameters</span></span>
<span data-ttu-id="8b9e1-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b9e1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b9e1-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b9e1-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b9e1-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b9e1-145">INPUTS</span></span>

### <span data-ttu-id="8b9e1-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8b9e1-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="8b9e1-147">System.String</span><span class="sxs-lookup"><span data-stu-id="8b9e1-147">System.String</span></span>

## <span data-ttu-id="8b9e1-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b9e1-148">OUTPUTS</span></span>

### <span data-ttu-id="8b9e1-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8b9e1-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="8b9e1-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b9e1-150">NOTES</span></span>

## <span data-ttu-id="8b9e1-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b9e1-151">RELATED LINKS</span></span>
