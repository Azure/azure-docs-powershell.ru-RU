---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ab6dd43cff746d670fe05d66d983836433323728
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506332"
---
# <span data-ttu-id="c4649-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="c4649-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="c4649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4649-102">SYNOPSIS</span></span>
<span data-ttu-id="c4649-103">Укажите все или откажите подробные сведения о службах по подготовкам устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c4649-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="c4649-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4649-104">SYNTAX</span></span>

### <span data-ttu-id="c4649-105">ListIotDpsByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4649-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4649-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="c4649-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4649-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4649-107">DESCRIPTION</span></span>
<span data-ttu-id="c4649-108">Введение в службу по подготовкам устройств через Azure IoT см. в https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="c4649-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c4649-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4649-109">EXAMPLES</span></span>

### <span data-ttu-id="c4649-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4649-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="c4649-111">Укаймь все службы по обеспечению на устройствах Azure IoT в подписке.</span><span class="sxs-lookup"><span data-stu-id="c4649-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="c4649-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c4649-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="c4649-113">Перечислите все службы по предоставлению устройств Azure IoT Hub в группе ресурсов myresourcegroup.</span><span class="sxs-lookup"><span data-stu-id="c4649-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="c4649-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c4649-114">Example 3</span></span>
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

<span data-ttu-id="c4649-115">Откажитесь от сведений о службе "myiotdps" для устройства в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c4649-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="c4649-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4649-116">PARAMETERS</span></span>

### <span data-ttu-id="c4649-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4649-117">-DefaultProfile</span></span>
<span data-ttu-id="c4649-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4649-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4649-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c4649-119">-Name</span></span>
<span data-ttu-id="c4649-120">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="c4649-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c4649-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4649-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4649-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c4649-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c4649-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4649-123">CommonParameters</span></span>
<span data-ttu-id="c4649-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4649-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4649-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4649-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4649-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4649-126">INPUTS</span></span>

### <span data-ttu-id="c4649-127">Нет</span><span class="sxs-lookup"><span data-stu-id="c4649-127">None</span></span>

## <span data-ttu-id="c4649-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4649-128">OUTPUTS</span></span>

### <span data-ttu-id="c4649-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c4649-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="c4649-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4649-130">NOTES</span></span>

## <span data-ttu-id="c4649-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4649-131">RELATED LINKS</span></span>
