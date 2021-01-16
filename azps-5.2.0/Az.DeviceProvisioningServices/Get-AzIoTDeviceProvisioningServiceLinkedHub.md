---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 62f9a2d77ce3a5b34b25c98d681bcfba55ae62e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396639"
---
# <span data-ttu-id="3a69e-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="3a69e-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="3a69e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a69e-102">SYNOPSIS</span></span>
<span data-ttu-id="3a69e-103">Укажите все или откажите сведения о связанных концентраторах IoT в службе по их подготовкам в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3a69e-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3a69e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3a69e-104">SYNTAX</span></span>

### <span data-ttu-id="3a69e-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a69e-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a69e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3a69e-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a69e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3a69e-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a69e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a69e-108">DESCRIPTION</span></span>
<span data-ttu-id="3a69e-109">Введение в службу по подготовкам устройств через Azure IoT см. в https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="3a69e-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="3a69e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3a69e-110">EXAMPLES</span></span>

### <span data-ttu-id="3a69e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3a69e-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="3a69e-112">Перечислите все связанные концентраторы IoT в списке myiotdps.</span><span class="sxs-lookup"><span data-stu-id="3a69e-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="3a69e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3a69e-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="3a69e-114">Откажите сведения о связанном центре IoT "myiothub1" в службе по подготовка устройств для Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3a69e-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3a69e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a69e-115">PARAMETERS</span></span>

### <span data-ttu-id="3a69e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a69e-116">-DefaultProfile</span></span>
<span data-ttu-id="3a69e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a69e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a69e-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="3a69e-118">-DpsObject</span></span>
<span data-ttu-id="3a69e-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="3a69e-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a69e-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="3a69e-120">-LinkedHubName</span></span>
<span data-ttu-id="3a69e-121">Имя узла связанного концентратора IoT</span><span class="sxs-lookup"><span data-stu-id="3a69e-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="3a69e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3a69e-122">-Name</span></span>
<span data-ttu-id="3a69e-123">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="3a69e-123">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a69e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a69e-124">-ResourceGroupName</span></span>
<span data-ttu-id="3a69e-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3a69e-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a69e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a69e-126">-ResourceId</span></span>
<span data-ttu-id="3a69e-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="3a69e-127">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a69e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a69e-128">CommonParameters</span></span>
<span data-ttu-id="3a69e-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a69e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a69e-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a69e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a69e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a69e-131">INPUTS</span></span>

### <span data-ttu-id="3a69e-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3a69e-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="3a69e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3a69e-133">System.String</span></span>

## <span data-ttu-id="3a69e-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3a69e-134">OUTPUTS</span></span>

### <span data-ttu-id="3a69e-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="3a69e-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="3a69e-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="3a69e-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="3a69e-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3a69e-137">NOTES</span></span>

## <span data-ttu-id="3a69e-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a69e-138">RELATED LINKS</span></span>
