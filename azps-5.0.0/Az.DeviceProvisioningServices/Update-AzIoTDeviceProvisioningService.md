---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 411d4594c94fe1eb031f60d6abbff35f5060d4e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245487"
---
# <span data-ttu-id="9d180-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="9d180-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="9d180-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d180-102">SYNOPSIS</span></span>
<span data-ttu-id="9d180-103">Обновите службу подготовки устройств центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="9d180-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="9d180-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d180-104">SYNTAX</span></span>

### <span data-ttu-id="9d180-105">ResourceUpdateSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d180-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d180-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="9d180-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d180-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="9d180-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d180-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="9d180-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d180-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="9d180-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d180-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="9d180-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d180-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d180-111">DESCRIPTION</span></span>
<span data-ttu-id="9d180-112">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="9d180-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="9d180-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d180-113">EXAMPLES</span></span>

### <span data-ttu-id="9d180-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9d180-114">Example 1</span></span>
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

<span data-ttu-id="9d180-115">Обновите политику выделения на "геозадержка" службы подготовки устройств центра Azure IoT ("myiotdps").</span><span class="sxs-lookup"><span data-stu-id="9d180-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="9d180-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9d180-116">Example 2</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

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

<span data-ttu-id="9d180-117">Добавьте " @tags " в тег службы подготовки устройств центра Azure IOT "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="9d180-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="9d180-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9d180-118">Example 3</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag @tags -Reset

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

<span data-ttu-id="9d180-119">Удалите тег и добавьте новый " @tags " в тег "myiotdps" службы подготовки устройств центра Azure IOT с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="9d180-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="9d180-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d180-120">PARAMETERS</span></span>

### <span data-ttu-id="9d180-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="9d180-121">-AllocationPolicy</span></span>
<span data-ttu-id="9d180-122">Политика выделения услуг для службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="9d180-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="9d180-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d180-123">-DefaultProfile</span></span>
<span data-ttu-id="9d180-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d180-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d180-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d180-125">-InputObject</span></span>
<span data-ttu-id="9d180-126">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="9d180-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9d180-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9d180-127">-Name</span></span>
<span data-ttu-id="9d180-128">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="9d180-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9d180-129">-Reset (Сброс)</span><span class="sxs-lookup"><span data-stu-id="9d180-129">-Reset</span></span>
<span data-ttu-id="9d180-130">Сброс тегов службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="9d180-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="9d180-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d180-131">-ResourceGroupName</span></span>
<span data-ttu-id="9d180-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9d180-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9d180-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d180-133">-ResourceId</span></span>
<span data-ttu-id="9d180-134">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="9d180-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9d180-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="9d180-135">-Tag</span></span>
<span data-ttu-id="9d180-136">Коллекция тегов служб для подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="9d180-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="9d180-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d180-137">-Confirm</span></span>
<span data-ttu-id="9d180-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9d180-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d180-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d180-139">-WhatIf</span></span>
<span data-ttu-id="9d180-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9d180-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d180-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9d180-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d180-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d180-142">CommonParameters</span></span>
<span data-ttu-id="9d180-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d180-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d180-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d180-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d180-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d180-145">INPUTS</span></span>

### <span data-ttu-id="9d180-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9d180-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="9d180-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9d180-147">System.String</span></span>

## <span data-ttu-id="9d180-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d180-148">OUTPUTS</span></span>

### <span data-ttu-id="9d180-149">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9d180-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="9d180-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d180-150">NOTES</span></span>

## <span data-ttu-id="9d180-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d180-151">RELATED LINKS</span></span>