---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328750"
---
# <span data-ttu-id="54a13-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="54a13-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="54a13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54a13-102">SYNOPSIS</span></span>
<span data-ttu-id="54a13-103">Получает состояние регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="54a13-103">Gets the device registration state.</span></span>

## <span data-ttu-id="54a13-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54a13-104">SYNTAX</span></span>

### <span data-ttu-id="54a13-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54a13-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54a13-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="54a13-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54a13-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="54a13-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54a13-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54a13-108">DESCRIPTION</span></span>
<span data-ttu-id="54a13-109">Получить состояние регистрации устройства или состояние регистрации устройств в группе регистрации в службе регистрации устройств Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="54a13-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="54a13-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54a13-110">EXAMPLES</span></span>

### <span data-ttu-id="54a13-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54a13-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="54a13-112">Получите сведения об состояниях регистрации устройства в службе регистрации устройств в центре IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="54a13-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="54a13-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="54a13-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="54a13-114">Перечислить все состояния регистрации устройств в этой группе регистрации.</span><span class="sxs-lookup"><span data-stu-id="54a13-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="54a13-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54a13-115">PARAMETERS</span></span>

### <span data-ttu-id="54a13-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a13-116">-DefaultProfile</span></span>
<span data-ttu-id="54a13-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54a13-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54a13-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="54a13-118">-DpsName</span></span>
<span data-ttu-id="54a13-119">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="54a13-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="54a13-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="54a13-120">-DpsObject</span></span>
<span data-ttu-id="54a13-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="54a13-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="54a13-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="54a13-122">-EnrollmentId</span></span>
<span data-ttu-id="54a13-123">ИД группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="54a13-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="54a13-124">-Query</span><span class="sxs-lookup"><span data-stu-id="54a13-124">-Query</span></span>
<span data-ttu-id="54a13-125">SQL-запрос.</span><span class="sxs-lookup"><span data-stu-id="54a13-125">Sql query.</span></span>

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

### <span data-ttu-id="54a13-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="54a13-126">-RegistrationId</span></span>
<span data-ttu-id="54a13-127">ИД регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="54a13-127">ID of device registration.</span></span>

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

### <span data-ttu-id="54a13-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54a13-128">-ResourceGroupName</span></span>
<span data-ttu-id="54a13-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="54a13-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="54a13-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54a13-130">-ResourceId</span></span>
<span data-ttu-id="54a13-131">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="54a13-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="54a13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a13-132">CommonParameters</span></span>
<span data-ttu-id="54a13-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54a13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a13-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54a13-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a13-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54a13-135">INPUTS</span></span>

### <span data-ttu-id="54a13-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="54a13-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="54a13-137">System.String</span><span class="sxs-lookup"><span data-stu-id="54a13-137">System.String</span></span>

## <span data-ttu-id="54a13-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54a13-138">OUTPUTS</span></span>

### <span data-ttu-id="54a13-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="54a13-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="54a13-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span><span class="sxs-lookup"><span data-stu-id="54a13-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="54a13-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54a13-141">NOTES</span></span>

## <span data-ttu-id="54a13-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54a13-142">RELATED LINKS</span></span>
