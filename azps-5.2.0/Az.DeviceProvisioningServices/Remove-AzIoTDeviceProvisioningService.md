---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 4701070ae7810b86ff7567f73b39606909d7fa10
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398420"
---
# <span data-ttu-id="8a689-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="8a689-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="8a689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a689-102">SYNOPSIS</span></span>
<span data-ttu-id="8a689-103">Удалите службу по подготовкам устройств для Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="8a689-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="8a689-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8a689-104">SYNTAX</span></span>

### <span data-ttu-id="8a689-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a689-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a689-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8a689-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a689-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8a689-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a689-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a689-108">DESCRIPTION</span></span>
<span data-ttu-id="8a689-109">Введение в службу по подготовкам устройств через Azure IoT см. в https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="8a689-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="8a689-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8a689-110">EXAMPLES</span></span>

### <span data-ttu-id="8a689-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8a689-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="8a689-112">Удалите службу "myiotdps" для устройства в Центре IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="8a689-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="8a689-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8a689-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="8a689-114">Удалите службу "myiotdps" для устройства в Azure IoT Hub с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="8a689-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="8a689-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a689-115">PARAMETERS</span></span>

### <span data-ttu-id="8a689-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a689-116">-DefaultProfile</span></span>
<span data-ttu-id="8a689-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a689-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a689-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a689-118">-InputObject</span></span>
<span data-ttu-id="8a689-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="8a689-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="8a689-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8a689-120">-Name</span></span>
<span data-ttu-id="8a689-121">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="8a689-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8a689-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a689-122">-PassThru</span></span>
<span data-ttu-id="8a689-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8a689-123">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a689-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a689-124">-ResourceGroupName</span></span>
<span data-ttu-id="8a689-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8a689-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8a689-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a689-126">-ResourceId</span></span>
<span data-ttu-id="8a689-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="8a689-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="8a689-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a689-128">-Confirm</span></span>
<span data-ttu-id="8a689-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a689-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a689-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a689-130">-WhatIf</span></span>
<span data-ttu-id="8a689-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a689-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a689-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8a689-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a689-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a689-133">CommonParameters</span></span>
<span data-ttu-id="8a689-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a689-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a689-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a689-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a689-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a689-136">INPUTS</span></span>

### <span data-ttu-id="8a689-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8a689-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="8a689-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8a689-138">System.String</span></span>

## <span data-ttu-id="8a689-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8a689-139">OUTPUTS</span></span>

### <span data-ttu-id="8a689-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8a689-140">System.Boolean</span></span>

## <span data-ttu-id="8a689-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8a689-141">NOTES</span></span>

## <span data-ttu-id="8a689-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a689-142">RELATED LINKS</span></span>
