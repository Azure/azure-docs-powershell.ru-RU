---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: a2700c1872e53234d97e82c41a93ef6e9e328391
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721050"
---
# <span data-ttu-id="0fc2c-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="0fc2c-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="0fc2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fc2c-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc2c-103">Удалите службу подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="0fc2c-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0fc2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fc2c-104">SYNTAX</span></span>

### <span data-ttu-id="0fc2c-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0fc2c-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fc2c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0fc2c-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fc2c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0fc2c-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fc2c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fc2c-108">DESCRIPTION</span></span>
<span data-ttu-id="0fc2c-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0fc2c-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0fc2c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fc2c-110">EXAMPLES</span></span>

### <span data-ttu-id="0fc2c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0fc2c-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="0fc2c-112">Удаление службы подготовки "myiotdps" устройства центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="0fc2c-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="0fc2c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0fc2c-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="0fc2c-114">Удаление службы подготовки устройства ("myiotdps") центра Azure IoT с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="0fc2c-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="0fc2c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fc2c-115">PARAMETERS</span></span>

### <span data-ttu-id="0fc2c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc2c-116">-DefaultProfile</span></span>
<span data-ttu-id="0fc2c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fc2c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc2c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fc2c-118">-InputObject</span></span>
<span data-ttu-id="0fc2c-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="0fc2c-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0fc2c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0fc2c-120">-Name</span></span>
<span data-ttu-id="0fc2c-121">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="0fc2c-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0fc2c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fc2c-122">-PassThru</span></span>
<span data-ttu-id="0fc2c-123">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="0fc2c-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0fc2c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc2c-124">-ResourceGroupName</span></span>
<span data-ttu-id="0fc2c-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0fc2c-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0fc2c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fc2c-126">-ResourceId</span></span>
<span data-ttu-id="0fc2c-127">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="0fc2c-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0fc2c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fc2c-128">-Confirm</span></span>
<span data-ttu-id="0fc2c-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0fc2c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fc2c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fc2c-130">-WhatIf</span></span>
<span data-ttu-id="0fc2c-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0fc2c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fc2c-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0fc2c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fc2c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc2c-133">CommonParameters</span></span>
<span data-ttu-id="0fc2c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fc2c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc2c-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fc2c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc2c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fc2c-136">INPUTS</span></span>

### <span data-ttu-id="0fc2c-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0fc2c-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="0fc2c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0fc2c-138">System.String</span></span>

## <span data-ttu-id="0fc2c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fc2c-139">OUTPUTS</span></span>

### <span data-ttu-id="0fc2c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0fc2c-140">System.Boolean</span></span>

## <span data-ttu-id="0fc2c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fc2c-141">NOTES</span></span>

## <span data-ttu-id="0fc2c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fc2c-142">RELATED LINKS</span></span>
