---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420463"
---
# <span data-ttu-id="c0030-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="c0030-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="c0030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0030-102">SYNOPSIS</span></span>
<span data-ttu-id="c0030-103">Удаление связанного концентратора IoT в службе по подготовка устройств для Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c0030-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c0030-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c0030-104">SYNTAX</span></span>

### <span data-ttu-id="c0030-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0030-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0030-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c0030-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0030-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c0030-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0030-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0030-108">DESCRIPTION</span></span>
<span data-ttu-id="c0030-109">Введение в службу по подготовкам устройств через Azure IoT см. в https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="c0030-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c0030-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c0030-110">EXAMPLES</span></span>

### <span data-ttu-id="c0030-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0030-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="c0030-112">Удалите связанный центр IoT "myiothub" в службе по подготовка устройств для Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c0030-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="c0030-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c0030-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="c0030-114">Удалите связанный концентратор IoT "myiothub" в службе подготовка устройства в Azure IoT Hub с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="c0030-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="c0030-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0030-115">PARAMETERS</span></span>

### <span data-ttu-id="c0030-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0030-116">-DefaultProfile</span></span>
<span data-ttu-id="c0030-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0030-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0030-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0030-118">-InputObject</span></span>
<span data-ttu-id="c0030-119">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="c0030-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0030-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="c0030-120">-LinkedHubName</span></span>
<span data-ttu-id="c0030-121">Имя узла связанного концентратора IoT</span><span class="sxs-lookup"><span data-stu-id="c0030-121">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0030-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c0030-122">-Name</span></span>
<span data-ttu-id="c0030-123">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="c0030-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c0030-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0030-124">-PassThru</span></span>
<span data-ttu-id="c0030-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c0030-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c0030-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0030-126">-ResourceGroupName</span></span>
<span data-ttu-id="c0030-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c0030-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c0030-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0030-128">-ResourceId</span></span>
<span data-ttu-id="c0030-129">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="c0030-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c0030-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0030-130">-Confirm</span></span>
<span data-ttu-id="c0030-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0030-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0030-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0030-132">-WhatIf</span></span>
<span data-ttu-id="c0030-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0030-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0030-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c0030-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0030-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0030-135">CommonParameters</span></span>
<span data-ttu-id="c0030-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0030-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0030-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0030-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0030-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0030-138">INPUTS</span></span>

### <span data-ttu-id="c0030-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="c0030-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="c0030-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c0030-140">System.String</span></span>

## <span data-ttu-id="c0030-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c0030-141">OUTPUTS</span></span>

### <span data-ttu-id="c0030-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0030-142">System.Boolean</span></span>

## <span data-ttu-id="c0030-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c0030-143">NOTES</span></span>

## <span data-ttu-id="c0030-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0030-144">RELATED LINKS</span></span>
