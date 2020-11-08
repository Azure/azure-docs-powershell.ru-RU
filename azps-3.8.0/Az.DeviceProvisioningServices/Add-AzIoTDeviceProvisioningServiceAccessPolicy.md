---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066852"
---
# <span data-ttu-id="fa7fa-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fa7fa-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="fa7fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa7fa-102">SYNOPSIS</span></span>
<span data-ttu-id="fa7fa-103">Добавьте новую политику общего доступа в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="fa7fa-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="fa7fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa7fa-104">SYNTAX</span></span>

### <span data-ttu-id="fa7fa-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa7fa-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa7fa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa7fa-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa7fa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fa7fa-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa7fa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa7fa-108">DESCRIPTION</span></span>
<span data-ttu-id="fa7fa-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="fa7fa-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="fa7fa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa7fa-110">EXAMPLES</span></span>

### <span data-ttu-id="fa7fa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa7fa-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="fa7fa-112">Добавьте новую политику общего доступа в службе подготовки устройств центра для Azure IoT с EnrollmentWrite и ServiceConfig правами.</span><span class="sxs-lookup"><span data-stu-id="fa7fa-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="fa7fa-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fa7fa-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="fa7fa-114">Добавьте новую политику общего доступа в службе подготовки устройств центра для Azure IoT с EnrollmentRead right.</span><span class="sxs-lookup"><span data-stu-id="fa7fa-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="fa7fa-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa7fa-115">PARAMETERS</span></span>

### <span data-ttu-id="fa7fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa7fa-116">-DefaultProfile</span></span>
<span data-ttu-id="fa7fa-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa7fa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa7fa-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="fa7fa-118">-DpsObject</span></span>
<span data-ttu-id="fa7fa-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="fa7fa-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="fa7fa-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fa7fa-120">-KeyName</span></span>
<span data-ttu-id="fa7fa-121">Имя ключа политики доступа к службе для подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="fa7fa-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="fa7fa-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fa7fa-122">-Name</span></span>
<span data-ttu-id="fa7fa-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="fa7fa-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fa7fa-124">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="fa7fa-124">-Permissions</span></span>
<span data-ttu-id="fa7fa-125">Разрешения для политики доступа к службам для устройства IoT</span><span class="sxs-lookup"><span data-stu-id="fa7fa-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="fa7fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa7fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="fa7fa-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fa7fa-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fa7fa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa7fa-128">-ResourceId</span></span>
<span data-ttu-id="fa7fa-129">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="fa7fa-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="fa7fa-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa7fa-130">-Confirm</span></span>
<span data-ttu-id="fa7fa-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fa7fa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa7fa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa7fa-132">-WhatIf</span></span>
<span data-ttu-id="fa7fa-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fa7fa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa7fa-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fa7fa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa7fa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa7fa-135">CommonParameters</span></span>
<span data-ttu-id="fa7fa-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa7fa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa7fa-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa7fa-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa7fa-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa7fa-138">INPUTS</span></span>

### <span data-ttu-id="fa7fa-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="fa7fa-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="fa7fa-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fa7fa-140">System.String</span></span>

## <span data-ttu-id="fa7fa-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa7fa-141">OUTPUTS</span></span>

### <span data-ttu-id="fa7fa-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="fa7fa-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="fa7fa-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa7fa-143">NOTES</span></span>

## <span data-ttu-id="fa7fa-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa7fa-144">RELATED LINKS</span></span>
