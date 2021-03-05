---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f34816ca77955c86f68b421efa221eab57e552cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010515"
---
# <span data-ttu-id="a2115-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a2115-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="a2115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2115-102">SYNOPSIS</span></span>
<span data-ttu-id="a2115-103">Добавьте новую политику общего доступа в службу по подготовкам устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="a2115-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="a2115-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2115-104">SYNTAX</span></span>

### <span data-ttu-id="a2115-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2115-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2115-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a2115-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2115-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a2115-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2115-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2115-108">DESCRIPTION</span></span>
<span data-ttu-id="a2115-109">Введение в службу по подготовкам устройств через Azure IoT см. в https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="a2115-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="a2115-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2115-110">EXAMPLES</span></span>

### <span data-ttu-id="a2115-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2115-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="a2115-112">Добавьте новую политику общего доступа в службу регистрации устройств в центре IoT Azure с правами enrollmentWrite и ServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="a2115-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="a2115-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a2115-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="a2115-114">Добавьте новую политику общего доступа в службу по регистрации устройств на концентраторе Azure IoT с правой справа на регистрациюRead.</span><span class="sxs-lookup"><span data-stu-id="a2115-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="a2115-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2115-115">PARAMETERS</span></span>

### <span data-ttu-id="a2115-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2115-116">-DefaultProfile</span></span>
<span data-ttu-id="a2115-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2115-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2115-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a2115-118">-DpsObject</span></span>
<span data-ttu-id="a2115-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="a2115-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a2115-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a2115-120">-KeyName</span></span>
<span data-ttu-id="a2115-121">Имя ключа политики доступа к службе предварительного доступа к устройствам IoT</span><span class="sxs-lookup"><span data-stu-id="a2115-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="a2115-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a2115-122">-Name</span></span>
<span data-ttu-id="a2115-123">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="a2115-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a2115-124">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="a2115-124">-Permissions</span></span>
<span data-ttu-id="a2115-125">Разрешения политики доступа к службе предварительного доступа к устройствам IoT</span><span class="sxs-lookup"><span data-stu-id="a2115-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="a2115-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2115-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2115-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a2115-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a2115-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2115-128">-ResourceId</span></span>
<span data-ttu-id="a2115-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="a2115-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a2115-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2115-130">-Confirm</span></span>
<span data-ttu-id="a2115-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a2115-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2115-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2115-132">-WhatIf</span></span>
<span data-ttu-id="a2115-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2115-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2115-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a2115-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2115-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2115-135">CommonParameters</span></span>
<span data-ttu-id="a2115-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2115-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2115-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2115-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2115-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2115-138">INPUTS</span></span>

### <span data-ttu-id="a2115-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a2115-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="a2115-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a2115-140">System.String</span></span>

## <span data-ttu-id="a2115-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2115-141">OUTPUTS</span></span>

### <span data-ttu-id="a2115-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="a2115-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="a2115-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2115-143">NOTES</span></span>

## <span data-ttu-id="a2115-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2115-144">RELATED LINKS</span></span>
