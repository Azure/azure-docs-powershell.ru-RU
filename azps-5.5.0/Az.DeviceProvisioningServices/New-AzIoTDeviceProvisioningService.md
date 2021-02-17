---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 482acd4f82320bbc14c5bf95c113304a8720019b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220073"
---
# <span data-ttu-id="a5a1c-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="a5a1c-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="a5a1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a1c-103">Создайте службу по созданию службы по созданию устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="a5a1c-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="a5a1c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5a1c-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5a1c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a1c-106">Введение в службу по подготовкам устройств через Azure IoT см. в https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="a5a1c-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="a5a1c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5a1c-107">EXAMPLES</span></span>

### <span data-ttu-id="a5a1c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a5a1c-108">Example 1</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {[key1, value1]}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="a5a1c-109">Создайте службу по созданию устройств Azure IoT Hub со стандартным уровнем цен S1 и тегами в регионе группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a5a1c-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="a5a1c-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a5a1c-110">Example 2</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : eastus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="a5a1c-111">Создайте службу по созданию устройств в Azure IoT Hub со стандартным уровнем цен S1 в регионе "восток".</span><span class="sxs-lookup"><span data-stu-id="a5a1c-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="a5a1c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5a1c-112">PARAMETERS</span></span>

### <span data-ttu-id="a5a1c-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="a5a1c-113">-AllocationPolicy</span></span>
<span data-ttu-id="a5a1c-114">Политика выделения службы для подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="a5a1c-114">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a1c-115">-DefaultProfile</span></span>
<span data-ttu-id="a5a1c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a1c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a1c-117">-Location</span><span class="sxs-lookup"><span data-stu-id="a5a1c-117">-Location</span></span>
<span data-ttu-id="a5a1c-118">Расположение</span><span class="sxs-lookup"><span data-stu-id="a5a1c-118">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a1c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a5a1c-119">-Name</span></span>
<span data-ttu-id="a5a1c-120">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="a5a1c-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a5a1c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a1c-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5a1c-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a5a1c-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a1c-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a5a1c-123">-SkuName</span></span>
<span data-ttu-id="a5a1c-124">SKU</span><span class="sxs-lookup"><span data-stu-id="a5a1c-124">Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a1c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5a1c-125">-Tag</span></span>
<span data-ttu-id="a5a1c-126">Теги экземпляра службы подготовка устройств IoT.</span><span class="sxs-lookup"><span data-stu-id="a5a1c-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="a5a1c-127">Пакет свойств в парах значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="a5a1c-127">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a1c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5a1c-128">-Confirm</span></span>
<span data-ttu-id="a5a1c-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a5a1c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5a1c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a1c-130">-WhatIf</span></span>
<span data-ttu-id="a5a1c-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a1c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5a1c-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a5a1c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5a1c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a1c-133">CommonParameters</span></span>
<span data-ttu-id="a5a1c-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a1c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a1c-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a1c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a1c-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5a1c-136">INPUTS</span></span>

### <span data-ttu-id="a5a1c-137">Нет</span><span class="sxs-lookup"><span data-stu-id="a5a1c-137">None</span></span>

## <span data-ttu-id="a5a1c-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5a1c-138">OUTPUTS</span></span>

### <span data-ttu-id="a5a1c-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a5a1c-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="a5a1c-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5a1c-140">NOTES</span></span>

## <span data-ttu-id="a5a1c-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5a1c-141">RELATED LINKS</span></span>
