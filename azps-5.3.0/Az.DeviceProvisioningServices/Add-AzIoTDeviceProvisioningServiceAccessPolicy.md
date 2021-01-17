---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426255"
---
# <span data-ttu-id="00654-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="00654-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="00654-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00654-102">SYNOPSIS</span></span>
<span data-ttu-id="00654-103">Добавьте новую политику общего доступа в службу по подготовкам устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="00654-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="00654-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="00654-104">SYNTAX</span></span>

### <span data-ttu-id="00654-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00654-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00654-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="00654-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00654-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="00654-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00654-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00654-108">DESCRIPTION</span></span>
<span data-ttu-id="00654-109">Введение в службу по подготовкам устройств в Azure IoT Hub см. в https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="00654-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="00654-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="00654-110">EXAMPLES</span></span>

### <span data-ttu-id="00654-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00654-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="00654-112">Добавьте новую политику общего доступа в службу регистрации устройств в центре IoT Azure с правами enrollmentWrite и ServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="00654-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="00654-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="00654-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="00654-114">Добавьте новую политику общего доступа в службу по регистрации устройств на концентраторе Azure IoT с правой справа на регистрациюRead.</span><span class="sxs-lookup"><span data-stu-id="00654-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="00654-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00654-115">PARAMETERS</span></span>

### <span data-ttu-id="00654-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00654-116">-DefaultProfile</span></span>
<span data-ttu-id="00654-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00654-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00654-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="00654-118">-DpsObject</span></span>
<span data-ttu-id="00654-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="00654-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="00654-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="00654-120">-KeyName</span></span>
<span data-ttu-id="00654-121">Имя ключа политики доступа к службе предварительного доступа к устройствам IoT</span><span class="sxs-lookup"><span data-stu-id="00654-121">IoT Device Provisioning Service access policy key name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00654-122">-Name</span><span class="sxs-lookup"><span data-stu-id="00654-122">-Name</span></span>
<span data-ttu-id="00654-123">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="00654-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="00654-124">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="00654-124">-Permissions</span></span>
<span data-ttu-id="00654-125">Разрешения политики доступа к службе предварительного доступа к устройствам IoT</span><span class="sxs-lookup"><span data-stu-id="00654-125">IoT Device Provisioning Service access policy permissions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ServiceConfig, EnrollmentRead, EnrollmentWrite, DeviceConnect, RegistrationStatusRead, RegistrationStatusWrite

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00654-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00654-126">-ResourceGroupName</span></span>
<span data-ttu-id="00654-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="00654-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="00654-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00654-128">-ResourceId</span></span>
<span data-ttu-id="00654-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="00654-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="00654-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00654-130">-Confirm</span></span>
<span data-ttu-id="00654-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="00654-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00654-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00654-132">-WhatIf</span></span>
<span data-ttu-id="00654-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00654-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00654-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="00654-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00654-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00654-135">CommonParameters</span></span>
<span data-ttu-id="00654-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00654-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00654-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00654-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00654-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00654-138">INPUTS</span></span>

### <span data-ttu-id="00654-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="00654-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="00654-140">System.String</span><span class="sxs-lookup"><span data-stu-id="00654-140">System.String</span></span>

## <span data-ttu-id="00654-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="00654-141">OUTPUTS</span></span>

### <span data-ttu-id="00654-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="00654-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="00654-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="00654-143">NOTES</span></span>

## <span data-ttu-id="00654-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00654-144">RELATED LINKS</span></span>
