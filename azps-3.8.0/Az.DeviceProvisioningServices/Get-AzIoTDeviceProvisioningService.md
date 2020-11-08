---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ab6dd43cff746d670fe05d66d983836433323728
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066814"
---
# <span data-ttu-id="4097a-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="4097a-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="4097a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4097a-102">SYNOPSIS</span></span>
<span data-ttu-id="4097a-103">Список всех и подробных сведений о службах подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="4097a-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="4097a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4097a-104">SYNTAX</span></span>

### <span data-ttu-id="4097a-105">ListIotDpsByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4097a-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4097a-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="4097a-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4097a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4097a-107">DESCRIPTION</span></span>
<span data-ttu-id="4097a-108">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="4097a-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="4097a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4097a-109">EXAMPLES</span></span>

### <span data-ttu-id="4097a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4097a-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="4097a-111">Список всех служб подготовки устройств центра Azure IoT в подписке.</span><span class="sxs-lookup"><span data-stu-id="4097a-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="4097a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4097a-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="4097a-113">Список всех служб подготовки устройств центра Azure IoT в группе ресурсов "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="4097a-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="4097a-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4097a-114">Example 3</span></span>
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

<span data-ttu-id="4097a-115">Показать подробные сведения о службе подготовки устройств-концентраторов Azure IoT "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="4097a-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="4097a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4097a-116">PARAMETERS</span></span>

### <span data-ttu-id="4097a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4097a-117">-DefaultProfile</span></span>
<span data-ttu-id="4097a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4097a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4097a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4097a-119">-Name</span></span>
<span data-ttu-id="4097a-120">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="4097a-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4097a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4097a-121">-ResourceGroupName</span></span>
<span data-ttu-id="4097a-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4097a-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4097a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4097a-123">CommonParameters</span></span>
<span data-ttu-id="4097a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4097a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4097a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4097a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4097a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4097a-126">INPUTS</span></span>

### <span data-ttu-id="4097a-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="4097a-127">None</span></span>

## <span data-ttu-id="4097a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4097a-128">OUTPUTS</span></span>

### <span data-ttu-id="4097a-129">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4097a-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="4097a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="4097a-130">NOTES</span></span>

## <span data-ttu-id="4097a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4097a-131">RELATED LINKS</span></span>
