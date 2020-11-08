---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243612"
---
# <span data-ttu-id="cdb38-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="cdb38-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="cdb38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cdb38-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb38-103">Удаление связанного центра Интернета вещей в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="cdb38-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="cdb38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cdb38-104">SYNTAX</span></span>

### <span data-ttu-id="cdb38-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cdb38-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdb38-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cdb38-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb38-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cdb38-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdb38-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdb38-108">DESCRIPTION</span></span>
<span data-ttu-id="cdb38-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="cdb38-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="cdb38-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cdb38-110">EXAMPLES</span></span>

### <span data-ttu-id="cdb38-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cdb38-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="cdb38-112">Удаление связанного центра Интернета вещей "myiothub" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="cdb38-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="cdb38-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cdb38-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="cdb38-114">Удаление связанного центра Интернета вещей "myiothub" в службе подготовки устройств центра для Azure IoT с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="cdb38-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="cdb38-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cdb38-115">PARAMETERS</span></span>

### <span data-ttu-id="cdb38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb38-116">-DefaultProfile</span></span>
<span data-ttu-id="cdb38-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdb38-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdb38-118">-InputObject</span></span>
<span data-ttu-id="cdb38-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="cdb38-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="cdb38-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="cdb38-120">-LinkedHubName</span></span>
<span data-ttu-id="cdb38-121">Имя узла для связанного центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="cdb38-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="cdb38-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cdb38-122">-Name</span></span>
<span data-ttu-id="cdb38-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="cdb38-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="cdb38-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdb38-124">-PassThru</span></span>
<span data-ttu-id="cdb38-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="cdb38-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cdb38-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb38-126">-ResourceGroupName</span></span>
<span data-ttu-id="cdb38-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cdb38-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cdb38-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb38-128">-ResourceId</span></span>
<span data-ttu-id="cdb38-129">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="cdb38-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="cdb38-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdb38-130">-Confirm</span></span>
<span data-ttu-id="cdb38-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cdb38-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb38-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb38-132">-WhatIf</span></span>
<span data-ttu-id="cdb38-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cdb38-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdb38-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cdb38-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb38-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb38-135">CommonParameters</span></span>
<span data-ttu-id="cdb38-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cdb38-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb38-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb38-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb38-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cdb38-138">INPUTS</span></span>

### <span data-ttu-id="cdb38-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="cdb38-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="cdb38-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cdb38-140">System.String</span></span>

## <span data-ttu-id="cdb38-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdb38-141">OUTPUTS</span></span>

### <span data-ttu-id="cdb38-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdb38-142">System.Boolean</span></span>

## <span data-ttu-id="cdb38-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="cdb38-143">NOTES</span></span>

## <span data-ttu-id="cdb38-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cdb38-144">RELATED LINKS</span></span>
