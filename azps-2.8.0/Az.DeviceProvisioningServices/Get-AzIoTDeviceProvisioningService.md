---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 264978e5cf66436667434c265a7a3ae0c5a31a5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721061"
---
# <span data-ttu-id="ece8e-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="ece8e-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="ece8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ece8e-102">SYNOPSIS</span></span>
<span data-ttu-id="ece8e-103">Список всех и подробных сведений о службах подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ece8e-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="ece8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ece8e-104">SYNTAX</span></span>

### <span data-ttu-id="ece8e-105">ListIotDpsByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ece8e-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ece8e-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="ece8e-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ece8e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ece8e-107">DESCRIPTION</span></span>
<span data-ttu-id="ece8e-108">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="ece8e-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="ece8e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ece8e-109">EXAMPLES</span></span>

### <span data-ttu-id="ece8e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ece8e-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="ece8e-111">Список всех служб подготовки устройств центра Azure IoT в подписке.</span><span class="sxs-lookup"><span data-stu-id="ece8e-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="ece8e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ece8e-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="ece8e-113">Список всех служб подготовки устройств центра Azure IoT в группе ресурсов "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="ece8e-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="ece8e-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ece8e-114">Example 3</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="ece8e-115">Показать подробные сведения о службе подготовки устройств-концентраторов Azure IoT "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="ece8e-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="ece8e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ece8e-116">PARAMETERS</span></span>

### <span data-ttu-id="ece8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece8e-117">-DefaultProfile</span></span>
<span data-ttu-id="ece8e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ece8e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ece8e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ece8e-119">-Name</span></span>
<span data-ttu-id="ece8e-120">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="ece8e-120">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece8e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece8e-121">-ResourceGroupName</span></span>
<span data-ttu-id="ece8e-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ece8e-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotDpsByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece8e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece8e-123">CommonParameters</span></span>
<span data-ttu-id="ece8e-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ece8e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece8e-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece8e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece8e-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ece8e-126">INPUTS</span></span>

### <span data-ttu-id="ece8e-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="ece8e-127">None</span></span>

## <span data-ttu-id="ece8e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ece8e-128">OUTPUTS</span></span>

### <span data-ttu-id="ece8e-129">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ece8e-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="ece8e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ece8e-130">NOTES</span></span>

## <span data-ttu-id="ece8e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ece8e-131">RELATED LINKS</span></span>
