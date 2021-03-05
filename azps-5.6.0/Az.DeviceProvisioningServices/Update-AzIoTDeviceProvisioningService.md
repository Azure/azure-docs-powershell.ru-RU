---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 7e1181ba837f0d2447a46f051765b0430399b123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985071"
---
# <span data-ttu-id="f3d84-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="f3d84-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="f3d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3d84-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d84-103">Обновив службу по подготовкам устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="f3d84-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="f3d84-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f3d84-104">SYNTAX</span></span>

### <span data-ttu-id="f3d84-105">ResourceUpdateSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f3d84-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3d84-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="f3d84-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3d84-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="f3d84-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3d84-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="f3d84-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3d84-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="f3d84-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3d84-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="f3d84-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3d84-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3d84-111">DESCRIPTION</span></span>
<span data-ttu-id="f3d84-112">Введение в службу по подготовкам устройств в Azure IoT Hub см. в https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="f3d84-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="f3d84-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f3d84-113">EXAMPLES</span></span>

### <span data-ttu-id="f3d84-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f3d84-114">Example 1</span></span>
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

<span data-ttu-id="f3d84-115">Обновив политику выделения, задав "GeoLatency" службы "myiotdps" для устройства из Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="f3d84-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="f3d84-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f3d84-116">Example 2</span></span>
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

<span data-ttu-id="f3d84-117">Добавьте теги в службу по подготовкам устройств azure IoT Hub "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="f3d84-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="f3d84-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f3d84-118">Example 3</span></span>
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

<span data-ttu-id="f3d84-119">Удалите теги и добавьте новые теги в службу по подготовкам устройств Azure IoT Hub "myiotdps" с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="f3d84-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="f3d84-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3d84-120">PARAMETERS</span></span>

### <span data-ttu-id="f3d84-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="f3d84-121">-AllocationPolicy</span></span>
<span data-ttu-id="f3d84-122">Политика выделения службы для подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="f3d84-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="f3d84-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d84-123">-DefaultProfile</span></span>
<span data-ttu-id="f3d84-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3d84-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3d84-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3d84-125">-InputObject</span></span>
<span data-ttu-id="f3d84-126">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="f3d84-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="f3d84-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f3d84-127">-Name</span></span>
<span data-ttu-id="f3d84-128">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="f3d84-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f3d84-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="f3d84-129">-Reset</span></span>
<span data-ttu-id="f3d84-130">Сброс тегов службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="f3d84-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="f3d84-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3d84-131">-ResourceGroupName</span></span>
<span data-ttu-id="f3d84-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f3d84-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f3d84-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3d84-133">-ResourceId</span></span>
<span data-ttu-id="f3d84-134">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="f3d84-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f3d84-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f3d84-135">-Tag</span></span>
<span data-ttu-id="f3d84-136">IoT Device Provisioning Service Tag collection</span><span class="sxs-lookup"><span data-stu-id="f3d84-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="f3d84-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3d84-137">-Confirm</span></span>
<span data-ttu-id="f3d84-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3d84-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3d84-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3d84-139">-WhatIf</span></span>
<span data-ttu-id="f3d84-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3d84-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3d84-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f3d84-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3d84-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d84-142">CommonParameters</span></span>
<span data-ttu-id="f3d84-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3d84-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d84-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d84-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d84-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3d84-145">INPUTS</span></span>

### <span data-ttu-id="f3d84-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="f3d84-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="f3d84-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f3d84-147">System.String</span></span>

## <span data-ttu-id="f3d84-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f3d84-148">OUTPUTS</span></span>

### <span data-ttu-id="f3d84-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="f3d84-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="f3d84-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f3d84-150">NOTES</span></span>

## <span data-ttu-id="f3d84-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3d84-151">RELATED LINKS</span></span>
