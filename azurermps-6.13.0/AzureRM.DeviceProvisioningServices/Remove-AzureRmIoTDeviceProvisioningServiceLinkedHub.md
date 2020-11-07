---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: f50c0955d56b42c341b6a1a6b64b1993ee66175e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734659"
---
# <span data-ttu-id="7649a-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="7649a-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="7649a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7649a-102">SYNOPSIS</span></span>
<span data-ttu-id="7649a-103">Удаление связанного центра Интернета вещей в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="7649a-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7649a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7649a-104">SYNTAX</span></span>

### <span data-ttu-id="7649a-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7649a-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7649a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7649a-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7649a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7649a-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7649a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7649a-108">DESCRIPTION</span></span>
<span data-ttu-id="7649a-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="7649a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="7649a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7649a-110">EXAMPLES</span></span>

### <span data-ttu-id="7649a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7649a-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="7649a-112">Удаление связанного центра Интернета вещей "myiothub" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="7649a-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="7649a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7649a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzureRmIoTDpsHub
```

<span data-ttu-id="7649a-114">Удаление связанного центра Интернета вещей "myiothub" в службе подготовки устройств центра для Azure IoT с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="7649a-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="7649a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7649a-115">PARAMETERS</span></span>

### <span data-ttu-id="7649a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7649a-116">-DefaultProfile</span></span>
<span data-ttu-id="7649a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7649a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7649a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7649a-118">-InputObject</span></span>
<span data-ttu-id="7649a-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="7649a-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7649a-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="7649a-120">-LinkedHubName</span></span>
<span data-ttu-id="7649a-121">Имя узла для связанного центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="7649a-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="7649a-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7649a-122">-Name</span></span>
<span data-ttu-id="7649a-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="7649a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7649a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7649a-124">-PassThru</span></span>
<span data-ttu-id="7649a-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="7649a-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7649a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7649a-126">-ResourceGroupName</span></span>
<span data-ttu-id="7649a-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7649a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7649a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7649a-128">-ResourceId</span></span>
<span data-ttu-id="7649a-129">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="7649a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7649a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7649a-130">-Confirm</span></span>
<span data-ttu-id="7649a-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7649a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7649a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7649a-132">-WhatIf</span></span>
<span data-ttu-id="7649a-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7649a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7649a-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7649a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7649a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7649a-135">CommonParameters</span></span>
<span data-ttu-id="7649a-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7649a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7649a-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7649a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7649a-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7649a-138">INPUTS</span></span>

### <span data-ttu-id="7649a-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="7649a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>
<span data-ttu-id="7649a-140">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7649a-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7649a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7649a-141">System.String</span></span>

## <span data-ttu-id="7649a-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7649a-142">OUTPUTS</span></span>

### <span data-ttu-id="7649a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7649a-143">System.Boolean</span></span>

## <span data-ttu-id="7649a-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="7649a-144">NOTES</span></span>

## <span data-ttu-id="7649a-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7649a-145">RELATED LINKS</span></span>
