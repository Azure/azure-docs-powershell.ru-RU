---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245514"
---
# <span data-ttu-id="3e71b-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="3e71b-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="3e71b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e71b-102">SYNOPSIS</span></span>
<span data-ttu-id="3e71b-103">Возвращает состояние регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="3e71b-103">Gets the device registration state.</span></span>

## <span data-ttu-id="3e71b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e71b-104">SYNTAX</span></span>

### <span data-ttu-id="3e71b-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e71b-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e71b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3e71b-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e71b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3e71b-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e71b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e71b-108">DESCRIPTION</span></span>
<span data-ttu-id="3e71b-109">Получите состояние регистрации устройства или состояние регистрации устройств под enrollmentGroup в службе подготовки устройств центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="3e71b-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="3e71b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e71b-110">EXAMPLES</span></span>

### <span data-ttu-id="3e71b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e71b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="3e71b-112">Получение подробных сведений о состоянии регистрации устройства в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="3e71b-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="3e71b-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3e71b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="3e71b-114">Перечислите все состояния регистрации устройств в этом enrollmentGroup.</span><span class="sxs-lookup"><span data-stu-id="3e71b-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="3e71b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e71b-115">PARAMETERS</span></span>

### <span data-ttu-id="3e71b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e71b-116">-DefaultProfile</span></span>
<span data-ttu-id="3e71b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e71b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e71b-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="3e71b-118">-DpsName</span></span>
<span data-ttu-id="3e71b-119">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="3e71b-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3e71b-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="3e71b-120">-DpsObject</span></span>
<span data-ttu-id="3e71b-121">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="3e71b-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="3e71b-122">-A</span><span class="sxs-lookup"><span data-stu-id="3e71b-122">-EnrollmentId</span></span>
<span data-ttu-id="3e71b-123">Идентификатор группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="3e71b-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="3e71b-124">-Query</span><span class="sxs-lookup"><span data-stu-id="3e71b-124">-Query</span></span>
<span data-ttu-id="3e71b-125">Запрос SQL.</span><span class="sxs-lookup"><span data-stu-id="3e71b-125">Sql query.</span></span>

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

### <span data-ttu-id="3e71b-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="3e71b-126">-RegistrationId</span></span>
<span data-ttu-id="3e71b-127">ИДЕНТИФИКАТОР регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="3e71b-127">ID of device registration.</span></span>

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

### <span data-ttu-id="3e71b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e71b-128">-ResourceGroupName</span></span>
<span data-ttu-id="3e71b-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3e71b-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3e71b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e71b-130">-ResourceId</span></span>
<span data-ttu-id="3e71b-131">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="3e71b-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="3e71b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e71b-132">CommonParameters</span></span>
<span data-ttu-id="3e71b-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e71b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e71b-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e71b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e71b-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e71b-135">INPUTS</span></span>

### <span data-ttu-id="3e71b-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3e71b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="3e71b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3e71b-137">System.String</span></span>

## <span data-ttu-id="3e71b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e71b-138">OUTPUTS</span></span>

### <span data-ttu-id="3e71b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="3e71b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="3e71b-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates []</span><span class="sxs-lookup"><span data-stu-id="3e71b-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="3e71b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e71b-141">NOTES</span></span>

## <span data-ttu-id="3e71b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e71b-142">RELATED LINKS</span></span>
