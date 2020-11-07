---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ac9d9423bf0098f0f6cf7abba958eb2b08404778
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721053"
---
# <span data-ttu-id="ebaa3-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="ebaa3-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="ebaa3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebaa3-102">SYNOPSIS</span></span>
<span data-ttu-id="ebaa3-103">Создайте службу подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ebaa3-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="ebaa3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebaa3-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebaa3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebaa3-105">DESCRIPTION</span></span>
<span data-ttu-id="ebaa3-106">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="ebaa3-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="ebaa3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebaa3-107">EXAMPLES</span></span>

### <span data-ttu-id="ebaa3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ebaa3-108">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="ebaa3-109">Создание службы подготовки устройств в центре Azure IoT с помощью стандартной ценовой категории S1 в регионе группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ebaa3-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="ebaa3-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ebaa3-110">Example 2</span></span>
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

<span data-ttu-id="ebaa3-111">Создание службы подготовки устройств центра для Azure IoT с помощью стандартной ценовой категории S1 в регионе "eastus".</span><span class="sxs-lookup"><span data-stu-id="ebaa3-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="ebaa3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebaa3-112">PARAMETERS</span></span>

### <span data-ttu-id="ebaa3-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ebaa3-113">-AllocationPolicy</span></span>
<span data-ttu-id="ebaa3-114">Политика выделения услуг для службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="ebaa3-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="ebaa3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebaa3-115">-DefaultProfile</span></span>
<span data-ttu-id="ebaa3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebaa3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebaa3-117">-Location</span><span class="sxs-lookup"><span data-stu-id="ebaa3-117">-Location</span></span>
<span data-ttu-id="ebaa3-118">Поиска</span><span class="sxs-lookup"><span data-stu-id="ebaa3-118">Location</span></span>

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

### <span data-ttu-id="ebaa3-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ebaa3-119">-Name</span></span>
<span data-ttu-id="ebaa3-120">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="ebaa3-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ebaa3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebaa3-121">-ResourceGroupName</span></span>
<span data-ttu-id="ebaa3-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ebaa3-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ebaa3-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ebaa3-123">-SkuName</span></span>
<span data-ttu-id="ebaa3-124">Кратки</span><span class="sxs-lookup"><span data-stu-id="ebaa3-124">Sku</span></span>

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

### <span data-ttu-id="ebaa3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebaa3-125">-Confirm</span></span>
<span data-ttu-id="ebaa3-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebaa3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebaa3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebaa3-127">-WhatIf</span></span>
<span data-ttu-id="ebaa3-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebaa3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebaa3-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebaa3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebaa3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebaa3-130">CommonParameters</span></span>
<span data-ttu-id="ebaa3-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebaa3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebaa3-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebaa3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebaa3-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebaa3-133">INPUTS</span></span>

### <span data-ttu-id="ebaa3-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="ebaa3-134">None</span></span>

## <span data-ttu-id="ebaa3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebaa3-135">OUTPUTS</span></span>

### <span data-ttu-id="ebaa3-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ebaa3-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="ebaa3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebaa3-137">NOTES</span></span>

## <span data-ttu-id="ebaa3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebaa3-138">RELATED LINKS</span></span>
