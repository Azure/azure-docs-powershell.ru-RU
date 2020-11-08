---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245517"
---
# <span data-ttu-id="1a401-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="1a401-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="1a401-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a401-102">SYNOPSIS</span></span>
<span data-ttu-id="1a401-103">Получить запись регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="1a401-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="1a401-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a401-104">SYNTAX</span></span>

### <span data-ttu-id="1a401-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a401-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a401-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1a401-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a401-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1a401-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a401-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a401-108">DESCRIPTION</span></span>
<span data-ttu-id="1a401-109">Получение подробных сведений о регистрации устройств или получение списка регистраций устройств в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="1a401-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="1a401-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a401-110">EXAMPLES</span></span>

### <span data-ttu-id="1a401-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1a401-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="1a401-112">Получение подробных сведений о регистрации устройства в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="1a401-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="1a401-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1a401-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="1a401-114">Перечислите регистрацию устройств в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="1a401-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="1a401-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a401-115">PARAMETERS</span></span>

### <span data-ttu-id="1a401-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a401-116">-DefaultProfile</span></span>
<span data-ttu-id="1a401-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a401-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a401-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="1a401-118">-DpsName</span></span>
<span data-ttu-id="1a401-119">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="1a401-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1a401-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="1a401-120">-DpsObject</span></span>
<span data-ttu-id="1a401-121">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="1a401-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="1a401-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="1a401-122">-RegistrationId</span></span>
<span data-ttu-id="1a401-123">Регистрационный код отдельной регистрации.</span><span class="sxs-lookup"><span data-stu-id="1a401-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="1a401-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a401-124">-ResourceGroupName</span></span>
<span data-ttu-id="1a401-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1a401-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1a401-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a401-126">-ResourceId</span></span>
<span data-ttu-id="1a401-127">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="1a401-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1a401-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a401-128">CommonParameters</span></span>
<span data-ttu-id="1a401-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a401-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a401-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a401-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a401-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a401-131">INPUTS</span></span>

### <span data-ttu-id="1a401-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1a401-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="1a401-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1a401-133">System.String</span></span>

## <span data-ttu-id="1a401-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a401-134">OUTPUTS</span></span>

### <span data-ttu-id="1a401-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="1a401-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="1a401-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollments []</span><span class="sxs-lookup"><span data-stu-id="1a401-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="1a401-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a401-137">NOTES</span></span>

## <span data-ttu-id="1a401-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a401-138">RELATED LINKS</span></span>
