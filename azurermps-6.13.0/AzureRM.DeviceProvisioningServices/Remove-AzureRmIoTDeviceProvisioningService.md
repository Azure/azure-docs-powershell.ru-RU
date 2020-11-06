---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: ecc91bb19b3d5d40f8c5aa3e4f25812a9999e45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563043"
---
# <span data-ttu-id="fd2eb-101">Remove-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="fd2eb-101">Remove-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="fd2eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd2eb-102">SYNOPSIS</span></span>
<span data-ttu-id="fd2eb-103">Удалите службу подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="fd2eb-103">Delete an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd2eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd2eb-104">SYNTAX</span></span>

### <span data-ttu-id="fd2eb-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd2eb-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd2eb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd2eb-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd2eb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fd2eb-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd2eb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd2eb-108">DESCRIPTION</span></span>
<span data-ttu-id="fd2eb-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="fd2eb-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="fd2eb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd2eb-110">EXAMPLES</span></span>

### <span data-ttu-id="fd2eb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fd2eb-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="fd2eb-112">Удаление службы подготовки "myiotdps" устройства центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="fd2eb-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="fd2eb-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fd2eb-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzureRmIotDps
```

<span data-ttu-id="fd2eb-114">Удаление службы подготовки устройства ("myiotdps") центра Azure IoT с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="fd2eb-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="fd2eb-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd2eb-115">PARAMETERS</span></span>

### <span data-ttu-id="fd2eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd2eb-116">-DefaultProfile</span></span>
<span data-ttu-id="fd2eb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd2eb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd2eb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd2eb-118">-InputObject</span></span>
<span data-ttu-id="fd2eb-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="fd2eb-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="fd2eb-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fd2eb-120">-Name</span></span>
<span data-ttu-id="fd2eb-121">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="fd2eb-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fd2eb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd2eb-122">-PassThru</span></span>
<span data-ttu-id="fd2eb-123">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="fd2eb-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fd2eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd2eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd2eb-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fd2eb-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fd2eb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd2eb-126">-ResourceId</span></span>
<span data-ttu-id="fd2eb-127">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="fd2eb-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="fd2eb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd2eb-128">-Confirm</span></span>
<span data-ttu-id="fd2eb-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd2eb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd2eb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd2eb-130">-WhatIf</span></span>
<span data-ttu-id="fd2eb-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd2eb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd2eb-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd2eb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd2eb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd2eb-133">CommonParameters</span></span>
<span data-ttu-id="fd2eb-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd2eb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd2eb-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd2eb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd2eb-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd2eb-136">INPUTS</span></span>

### <span data-ttu-id="fd2eb-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="fd2eb-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="fd2eb-138">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd2eb-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="fd2eb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fd2eb-139">System.String</span></span>

## <span data-ttu-id="fd2eb-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd2eb-140">OUTPUTS</span></span>

### <span data-ttu-id="fd2eb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd2eb-141">System.Boolean</span></span>

## <span data-ttu-id="fd2eb-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd2eb-142">NOTES</span></span>

## <span data-ttu-id="fd2eb-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd2eb-143">RELATED LINKS</span></span>
