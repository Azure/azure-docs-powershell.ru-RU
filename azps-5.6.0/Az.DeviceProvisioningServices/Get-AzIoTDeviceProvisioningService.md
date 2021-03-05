---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ee86af7862ad22b34e159f1d5097d5d30a4cba8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015363"
---
# <span data-ttu-id="4e8d7-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="4e8d7-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="4e8d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e8d7-102">SYNOPSIS</span></span>
<span data-ttu-id="4e8d7-103">Укажите все или откажите подробные сведения о службах по подготовкам устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="4e8d7-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="4e8d7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e8d7-104">SYNTAX</span></span>

### <span data-ttu-id="4e8d7-105">ListIotDpsByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e8d7-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e8d7-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="4e8d7-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e8d7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e8d7-107">DESCRIPTION</span></span>
<span data-ttu-id="4e8d7-108">Введение в службу по подготовкам устройств в Azure IoT Hub см. в https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="4e8d7-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="4e8d7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e8d7-109">EXAMPLES</span></span>

### <span data-ttu-id="4e8d7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e8d7-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="4e8d7-111">Перечислите все службы по обеспечению на устройствах Azure IoT в подписке.</span><span class="sxs-lookup"><span data-stu-id="4e8d7-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="4e8d7-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4e8d7-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="4e8d7-113">Перечислите все службы по предоставлению устройств Azure IoT Hub в группе ресурсов myresourcegroup.</span><span class="sxs-lookup"><span data-stu-id="4e8d7-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="4e8d7-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4e8d7-114">Example 3</span></span>
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

<span data-ttu-id="4e8d7-115">Откажитесь от сведений о службе "myiotdps" для устройства в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="4e8d7-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="4e8d7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e8d7-116">PARAMETERS</span></span>

### <span data-ttu-id="4e8d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e8d7-117">-DefaultProfile</span></span>
<span data-ttu-id="4e8d7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e8d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e8d7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4e8d7-119">-Name</span></span>
<span data-ttu-id="4e8d7-120">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="4e8d7-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4e8d7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e8d7-121">-ResourceGroupName</span></span>
<span data-ttu-id="4e8d7-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4e8d7-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4e8d7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e8d7-123">CommonParameters</span></span>
<span data-ttu-id="4e8d7-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e8d7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e8d7-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e8d7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e8d7-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e8d7-126">INPUTS</span></span>

### <span data-ttu-id="4e8d7-127">Нет</span><span class="sxs-lookup"><span data-stu-id="4e8d7-127">None</span></span>

## <span data-ttu-id="4e8d7-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e8d7-128">OUTPUTS</span></span>

### <span data-ttu-id="4e8d7-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4e8d7-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="4e8d7-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e8d7-130">NOTES</span></span>

## <span data-ttu-id="4e8d7-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e8d7-131">RELATED LINKS</span></span>
