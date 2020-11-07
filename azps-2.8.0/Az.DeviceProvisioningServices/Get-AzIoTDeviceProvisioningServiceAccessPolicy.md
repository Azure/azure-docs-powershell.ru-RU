---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f978e6c0a496273535551663a442989b2ab1648e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721060"
---
# <span data-ttu-id="4ec08-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4ec08-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="4ec08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ec08-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec08-103">Список всех и отображение сведений о политиках общего доступа в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="4ec08-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="4ec08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ec08-104">SYNTAX</span></span>

### <span data-ttu-id="4ec08-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ec08-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ec08-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ec08-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ec08-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ec08-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ec08-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ec08-108">DESCRIPTION</span></span>
<span data-ttu-id="4ec08-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="4ec08-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="4ec08-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ec08-110">EXAMPLES</span></span>

### <span data-ttu-id="4ec08-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ec08-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="4ec08-112">Перечислите все общие политики доступа в "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="4ec08-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="4ec08-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4ec08-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="4ec08-114">Отображение подробных сведений о политике общего доступа "mypolicy" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="4ec08-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="4ec08-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ec08-115">PARAMETERS</span></span>

### <span data-ttu-id="4ec08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec08-116">-DefaultProfile</span></span>
<span data-ttu-id="4ec08-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ec08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ec08-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4ec08-118">-DpsObject</span></span>
<span data-ttu-id="4ec08-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="4ec08-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4ec08-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4ec08-120">-KeyName</span></span>
<span data-ttu-id="4ec08-121">Имя ключа политики доступа к службе для подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="4ec08-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="4ec08-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ec08-122">-Name</span></span>
<span data-ttu-id="4ec08-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="4ec08-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4ec08-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ec08-124">-ResourceGroupName</span></span>
<span data-ttu-id="4ec08-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4ec08-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4ec08-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ec08-126">-ResourceId</span></span>
<span data-ttu-id="4ec08-127">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="4ec08-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4ec08-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec08-128">CommonParameters</span></span>
<span data-ttu-id="4ec08-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ec08-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec08-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec08-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec08-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ec08-131">INPUTS</span></span>

### <span data-ttu-id="4ec08-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4ec08-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4ec08-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4ec08-133">System.String</span></span>

## <span data-ttu-id="4ec08-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ec08-134">OUTPUTS</span></span>

### <span data-ttu-id="4ec08-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="4ec08-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="4ec08-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ec08-136">NOTES</span></span>

## <span data-ttu-id="4ec08-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ec08-137">RELATED LINKS</span></span>
