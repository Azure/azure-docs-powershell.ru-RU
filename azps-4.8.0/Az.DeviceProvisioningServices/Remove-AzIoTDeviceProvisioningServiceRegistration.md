---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: b0fa84887a54eb1f4e9c689c49fb08a1300cd62b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243610"
---
# <span data-ttu-id="c45bd-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="c45bd-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="c45bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c45bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c45bd-103">Удаляет регистрацию устройства.</span><span class="sxs-lookup"><span data-stu-id="c45bd-103">Deletes the device registration.</span></span>

## <span data-ttu-id="c45bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c45bd-104">SYNTAX</span></span>

### <span data-ttu-id="c45bd-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c45bd-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c45bd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c45bd-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c45bd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c45bd-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c45bd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c45bd-108">DESCRIPTION</span></span>
<span data-ttu-id="c45bd-109">Удалите регистрацию устройства в службе подготовки устройств центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="c45bd-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c45bd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c45bd-110">EXAMPLES</span></span>

### <span data-ttu-id="c45bd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c45bd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="c45bd-112">Удалите регистрацию устройства в службе подготовки устройств центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="c45bd-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c45bd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c45bd-113">PARAMETERS</span></span>

### <span data-ttu-id="c45bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c45bd-114">-DefaultProfile</span></span>
<span data-ttu-id="c45bd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c45bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c45bd-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="c45bd-116">-DpsName</span></span>
<span data-ttu-id="c45bd-117">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="c45bd-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c45bd-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c45bd-118">-DpsObject</span></span>
<span data-ttu-id="c45bd-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="c45bd-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c45bd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c45bd-120">-PassThru</span></span>
<span data-ttu-id="c45bd-121">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="c45bd-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="c45bd-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c45bd-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c45bd-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="c45bd-123">-RegistrationId</span></span>
<span data-ttu-id="c45bd-124">ИДЕНТИФИКАТОР регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="c45bd-124">ID of device registration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c45bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c45bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="c45bd-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c45bd-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c45bd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c45bd-127">-ResourceId</span></span>
<span data-ttu-id="c45bd-128">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="c45bd-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c45bd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c45bd-129">-Confirm</span></span>
<span data-ttu-id="c45bd-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c45bd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c45bd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c45bd-131">-WhatIf</span></span>
<span data-ttu-id="c45bd-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c45bd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c45bd-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c45bd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c45bd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c45bd-134">CommonParameters</span></span>
<span data-ttu-id="c45bd-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c45bd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c45bd-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c45bd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c45bd-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c45bd-137">INPUTS</span></span>

### <span data-ttu-id="c45bd-138">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c45bd-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c45bd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c45bd-139">System.String</span></span>

## <span data-ttu-id="c45bd-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c45bd-140">OUTPUTS</span></span>

### <span data-ttu-id="c45bd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c45bd-141">System.Boolean</span></span>

## <span data-ttu-id="c45bd-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="c45bd-142">NOTES</span></span>

## <span data-ttu-id="c45bd-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c45bd-143">RELATED LINKS</span></span>
