---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 87c6bdd72229baec8e65c40d4e2e4309bde59aba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066815"
---
# <span data-ttu-id="c0d81-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c0d81-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="c0d81-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0d81-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d81-103">Список всех и отображение сведений о политиках общего доступа в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="c0d81-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c0d81-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0d81-104">SYNTAX</span></span>

### <span data-ttu-id="c0d81-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0d81-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0d81-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c0d81-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0d81-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c0d81-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0d81-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0d81-108">DESCRIPTION</span></span>
<span data-ttu-id="c0d81-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="c0d81-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c0d81-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0d81-110">EXAMPLES</span></span>

### <span data-ttu-id="c0d81-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0d81-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="c0d81-112">Перечислите все общие политики доступа в "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="c0d81-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="c0d81-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c0d81-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="c0d81-114">Отображение подробных сведений о политике общего доступа "mypolicy" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="c0d81-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c0d81-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0d81-115">PARAMETERS</span></span>

### <span data-ttu-id="c0d81-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d81-116">-DefaultProfile</span></span>
<span data-ttu-id="c0d81-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d81-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0d81-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c0d81-118">-DpsObject</span></span>
<span data-ttu-id="c0d81-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="c0d81-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c0d81-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c0d81-120">-KeyName</span></span>
<span data-ttu-id="c0d81-121">Имя ключа политики доступа к службе для подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="c0d81-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="c0d81-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0d81-122">-Name</span></span>
<span data-ttu-id="c0d81-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="c0d81-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c0d81-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d81-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0d81-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c0d81-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c0d81-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0d81-126">-ResourceId</span></span>
<span data-ttu-id="c0d81-127">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="c0d81-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c0d81-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d81-128">CommonParameters</span></span>
<span data-ttu-id="c0d81-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0d81-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d81-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0d81-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d81-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0d81-131">INPUTS</span></span>

### <span data-ttu-id="c0d81-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c0d81-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c0d81-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c0d81-133">System.String</span></span>

## <span data-ttu-id="c0d81-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0d81-134">OUTPUTS</span></span>

### <span data-ttu-id="c0d81-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="c0d81-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="c0d81-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0d81-136">NOTES</span></span>

## <span data-ttu-id="c0d81-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0d81-137">RELATED LINKS</span></span>
