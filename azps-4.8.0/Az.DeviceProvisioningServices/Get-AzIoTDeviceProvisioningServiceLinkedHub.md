---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 62f9a2d77ce3a5b34b25c98d681bcfba55ae62e4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236722"
---
# <span data-ttu-id="dfb9a-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="dfb9a-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="dfb9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dfb9a-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb9a-103">Список всех или отображение сведений о связанных центрах Интернета вещей в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="dfb9a-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="dfb9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dfb9a-104">SYNTAX</span></span>

### <span data-ttu-id="dfb9a-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dfb9a-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfb9a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dfb9a-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfb9a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dfb9a-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfb9a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfb9a-108">DESCRIPTION</span></span>
<span data-ttu-id="dfb9a-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="dfb9a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="dfb9a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dfb9a-110">EXAMPLES</span></span>

### <span data-ttu-id="dfb9a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dfb9a-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="dfb9a-112">Перечислите все связанные центры Интернета вещей в "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="dfb9a-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="dfb9a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dfb9a-113">Example 2</span></span>
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

<span data-ttu-id="dfb9a-114">Показывать сведения о связанном центре Интернета вещей "myiothub1" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="dfb9a-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="dfb9a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dfb9a-115">PARAMETERS</span></span>

### <span data-ttu-id="dfb9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb9a-116">-DefaultProfile</span></span>
<span data-ttu-id="dfb9a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb9a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfb9a-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="dfb9a-118">-DpsObject</span></span>
<span data-ttu-id="dfb9a-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="dfb9a-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="dfb9a-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="dfb9a-120">-LinkedHubName</span></span>
<span data-ttu-id="dfb9a-121">Имя узла для связанного центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="dfb9a-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="dfb9a-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dfb9a-122">-Name</span></span>
<span data-ttu-id="dfb9a-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="dfb9a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="dfb9a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfb9a-124">-ResourceGroupName</span></span>
<span data-ttu-id="dfb9a-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="dfb9a-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dfb9a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfb9a-126">-ResourceId</span></span>
<span data-ttu-id="dfb9a-127">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="dfb9a-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="dfb9a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb9a-128">CommonParameters</span></span>
<span data-ttu-id="dfb9a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dfb9a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb9a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfb9a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb9a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dfb9a-131">INPUTS</span></span>

### <span data-ttu-id="dfb9a-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="dfb9a-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="dfb9a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dfb9a-133">System.String</span></span>

## <span data-ttu-id="dfb9a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfb9a-134">OUTPUTS</span></span>

### <span data-ttu-id="dfb9a-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="dfb9a-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="dfb9a-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="dfb9a-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="dfb9a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="dfb9a-137">NOTES</span></span>

## <span data-ttu-id="dfb9a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfb9a-138">RELATED LINKS</span></span>
