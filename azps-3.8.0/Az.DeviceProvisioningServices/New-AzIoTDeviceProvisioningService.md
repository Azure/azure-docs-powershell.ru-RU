---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 3102cafabecb5df8daea15a40eb179405c6c0ea8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066388"
---
# <span data-ttu-id="20ddc-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="20ddc-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="20ddc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="20ddc-103">Создайте службу подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="20ddc-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="20ddc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20ddc-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20ddc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20ddc-105">DESCRIPTION</span></span>
<span data-ttu-id="20ddc-106">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="20ddc-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="20ddc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20ddc-107">EXAMPLES</span></span>

### <span data-ttu-id="20ddc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="20ddc-108">Example 1</span></span>
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

<span data-ttu-id="20ddc-109">Создание службы подготовки устройств в центре Azure IoT с помощью стандартной ценовой категории S1 в регионе группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20ddc-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="20ddc-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="20ddc-110">Example 2</span></span>
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

<span data-ttu-id="20ddc-111">Создание службы подготовки устройств центра для Azure IoT с помощью стандартной ценовой категории S1 в регионе "eastus".</span><span class="sxs-lookup"><span data-stu-id="20ddc-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="20ddc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20ddc-112">PARAMETERS</span></span>

### <span data-ttu-id="20ddc-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="20ddc-113">-AllocationPolicy</span></span>
<span data-ttu-id="20ddc-114">Политика выделения услуг для службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="20ddc-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="20ddc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ddc-115">-DefaultProfile</span></span>
<span data-ttu-id="20ddc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20ddc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20ddc-117">-Location</span><span class="sxs-lookup"><span data-stu-id="20ddc-117">-Location</span></span>
<span data-ttu-id="20ddc-118">Поиска</span><span class="sxs-lookup"><span data-stu-id="20ddc-118">Location</span></span>

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

### <span data-ttu-id="20ddc-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="20ddc-119">-Name</span></span>
<span data-ttu-id="20ddc-120">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="20ddc-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="20ddc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20ddc-121">-ResourceGroupName</span></span>
<span data-ttu-id="20ddc-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="20ddc-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="20ddc-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="20ddc-123">-SkuName</span></span>
<span data-ttu-id="20ddc-124">Кратки</span><span class="sxs-lookup"><span data-stu-id="20ddc-124">Sku</span></span>

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

### <span data-ttu-id="20ddc-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20ddc-125">-Confirm</span></span>
<span data-ttu-id="20ddc-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="20ddc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20ddc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20ddc-127">-WhatIf</span></span>
<span data-ttu-id="20ddc-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="20ddc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20ddc-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20ddc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20ddc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ddc-130">CommonParameters</span></span>
<span data-ttu-id="20ddc-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20ddc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ddc-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20ddc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ddc-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20ddc-133">INPUTS</span></span>

### <span data-ttu-id="20ddc-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="20ddc-134">None</span></span>

## <span data-ttu-id="20ddc-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20ddc-135">OUTPUTS</span></span>

### <span data-ttu-id="20ddc-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="20ddc-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="20ddc-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="20ddc-137">NOTES</span></span>

## <span data-ttu-id="20ddc-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20ddc-138">RELATED LINKS</span></span>
