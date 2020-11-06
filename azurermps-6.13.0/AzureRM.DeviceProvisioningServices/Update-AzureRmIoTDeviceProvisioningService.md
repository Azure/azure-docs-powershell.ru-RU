---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: 80032ab2a677683ff876aca499f7e0ee682e6fd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566466"
---
# <span data-ttu-id="822cc-101">Update-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="822cc-101">Update-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="822cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="822cc-102">SYNOPSIS</span></span>
<span data-ttu-id="822cc-103">Обновите службу подготовки устройств центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="822cc-103">Update an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="822cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="822cc-104">SYNTAX</span></span>

### <span data-ttu-id="822cc-105">ResourceUpdateSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="822cc-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="822cc-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="822cc-106">InputObjectUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="822cc-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="822cc-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="822cc-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="822cc-108">ResourceIdUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="822cc-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="822cc-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="822cc-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="822cc-110">ResourceCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="822cc-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="822cc-111">DESCRIPTION</span></span>
<span data-ttu-id="822cc-112">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="822cc-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="822cc-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="822cc-113">EXAMPLES</span></span>

### <span data-ttu-id="822cc-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="822cc-114">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

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

<span data-ttu-id="822cc-115">Обновите политику выделения на "геозадержка" службы подготовки устройств центра Azure IoT ("myiotdps").</span><span class="sxs-lookup"><span data-stu-id="822cc-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="822cc-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="822cc-116">Example 2</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

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

<span data-ttu-id="822cc-117">Добавьте " @tags " в тег службы подготовки устройств центра Azure IOT "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="822cc-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="822cc-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="822cc-118">Example 3</span></span>
```
PS C:\> Get-AzureRmIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzureRmIoTDps -Tag @tags -Reset

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

<span data-ttu-id="822cc-119">Удалите тег и добавьте новый " @tags " в тег "myiotdps" службы подготовки устройств центра Azure IOT с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="822cc-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="822cc-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="822cc-120">PARAMETERS</span></span>

### <span data-ttu-id="822cc-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="822cc-121">-AllocationPolicy</span></span>
<span data-ttu-id="822cc-122">Политика выделения услуг для службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="822cc-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="822cc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822cc-123">-DefaultProfile</span></span>
<span data-ttu-id="822cc-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="822cc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="822cc-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="822cc-125">-InputObject</span></span>
<span data-ttu-id="822cc-126">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="822cc-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="822cc-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="822cc-127">-Name</span></span>
<span data-ttu-id="822cc-128">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="822cc-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="822cc-129">-Reset (Сброс)</span><span class="sxs-lookup"><span data-stu-id="822cc-129">-Reset</span></span>
<span data-ttu-id="822cc-130">Сброс тегов службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="822cc-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="822cc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="822cc-131">-ResourceGroupName</span></span>
<span data-ttu-id="822cc-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="822cc-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="822cc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="822cc-133">-ResourceId</span></span>
<span data-ttu-id="822cc-134">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="822cc-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="822cc-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="822cc-135">-Tag</span></span>
<span data-ttu-id="822cc-136">Коллекция тегов служб для подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="822cc-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="822cc-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="822cc-137">-Confirm</span></span>
<span data-ttu-id="822cc-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="822cc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="822cc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="822cc-139">-WhatIf</span></span>
<span data-ttu-id="822cc-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="822cc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="822cc-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="822cc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="822cc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822cc-142">CommonParameters</span></span>
<span data-ttu-id="822cc-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="822cc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822cc-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="822cc-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822cc-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="822cc-145">INPUTS</span></span>

### <span data-ttu-id="822cc-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="822cc-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="822cc-147">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="822cc-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="822cc-148">System. String</span><span class="sxs-lookup"><span data-stu-id="822cc-148">System.String</span></span>

## <span data-ttu-id="822cc-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="822cc-149">OUTPUTS</span></span>

### <span data-ttu-id="822cc-150">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="822cc-150">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="822cc-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="822cc-151">NOTES</span></span>

## <span data-ttu-id="822cc-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="822cc-152">RELATED LINKS</span></span>
