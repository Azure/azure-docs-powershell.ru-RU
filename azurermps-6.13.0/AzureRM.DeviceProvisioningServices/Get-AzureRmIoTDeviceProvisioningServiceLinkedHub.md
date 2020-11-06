---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: bae363b984f148ff55f34eaa04b1ba85eaad4449
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556659"
---
# <span data-ttu-id="5b2af-101">Get-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="5b2af-101">Get-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="5b2af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b2af-102">SYNOPSIS</span></span>
<span data-ttu-id="5b2af-103">Список всех или отображение сведений о связанных центрах Интернета вещей в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5b2af-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b2af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b2af-104">SYNTAX</span></span>

### <span data-ttu-id="5b2af-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b2af-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b2af-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5b2af-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b2af-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5b2af-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b2af-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b2af-108">DESCRIPTION</span></span>
<span data-ttu-id="5b2af-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5b2af-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5b2af-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b2af-110">EXAMPLES</span></span>

### <span data-ttu-id="5b2af-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b2af-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="5b2af-112">Перечислите все связанные центры Интернета вещей в "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="5b2af-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="5b2af-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5b2af-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="5b2af-114">Показывать сведения о связанном центре Интернета вещей "myiothub1" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5b2af-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5b2af-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b2af-115">PARAMETERS</span></span>

### <span data-ttu-id="5b2af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b2af-116">-DefaultProfile</span></span>
<span data-ttu-id="5b2af-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b2af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b2af-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5b2af-118">-DpsObject</span></span>
<span data-ttu-id="5b2af-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="5b2af-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5b2af-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="5b2af-120">-LinkedHubName</span></span>
<span data-ttu-id="5b2af-121">Имя узла для связанного центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="5b2af-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="5b2af-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b2af-122">-Name</span></span>
<span data-ttu-id="5b2af-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="5b2af-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5b2af-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b2af-124">-ResourceGroupName</span></span>
<span data-ttu-id="5b2af-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5b2af-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5b2af-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b2af-126">-ResourceId</span></span>
<span data-ttu-id="5b2af-127">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="5b2af-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5b2af-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b2af-128">CommonParameters</span></span>
<span data-ttu-id="5b2af-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b2af-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b2af-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b2af-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b2af-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b2af-131">INPUTS</span></span>

### <span data-ttu-id="5b2af-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5b2af-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="5b2af-133">Параметры: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b2af-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="5b2af-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5b2af-134">System.String</span></span>

## <span data-ttu-id="5b2af-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b2af-135">OUTPUTS</span></span>

### <span data-ttu-id="5b2af-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="5b2af-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="5b2af-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="5b2af-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="5b2af-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b2af-138">NOTES</span></span>

## <span data-ttu-id="5b2af-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b2af-139">RELATED LINKS</span></span>
