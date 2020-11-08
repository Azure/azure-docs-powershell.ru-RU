---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8b16d95d582e29be6f49cac9eaeb00bcda67de0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243609"
---
# <span data-ttu-id="4dec9-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="4dec9-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="4dec9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4dec9-102">SYNOPSIS</span></span>
<span data-ttu-id="4dec9-103">Удаление записи регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="4dec9-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="4dec9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4dec9-104">SYNTAX</span></span>

### <span data-ttu-id="4dec9-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4dec9-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4dec9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4dec9-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4dec9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4dec9-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dec9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dec9-108">DESCRIPTION</span></span>
<span data-ttu-id="4dec9-109">Удалите регистрацию устройства в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="4dec9-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4dec9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4dec9-110">EXAMPLES</span></span>

### <span data-ttu-id="4dec9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4dec9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="4dec9-112">Удаление указанной записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="4dec9-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="4dec9-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4dec9-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="4dec9-114">Удалите все записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="4dec9-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="4dec9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4dec9-115">PARAMETERS</span></span>

### <span data-ttu-id="4dec9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dec9-116">-DefaultProfile</span></span>
<span data-ttu-id="4dec9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4dec9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dec9-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="4dec9-118">-DpsName</span></span>
<span data-ttu-id="4dec9-119">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="4dec9-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4dec9-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4dec9-120">-DpsObject</span></span>
<span data-ttu-id="4dec9-121">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="4dec9-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4dec9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dec9-122">-PassThru</span></span>
<span data-ttu-id="4dec9-123">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="4dec9-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="4dec9-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4dec9-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4dec9-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="4dec9-125">-RegistrationId</span></span>
<span data-ttu-id="4dec9-126">Регистрационный код отдельной регистрации.</span><span class="sxs-lookup"><span data-stu-id="4dec9-126">Individual enrollment registration id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dec9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dec9-127">-ResourceGroupName</span></span>
<span data-ttu-id="4dec9-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4dec9-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4dec9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dec9-129">-ResourceId</span></span>
<span data-ttu-id="4dec9-130">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="4dec9-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4dec9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dec9-131">-Confirm</span></span>
<span data-ttu-id="4dec9-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4dec9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dec9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dec9-133">-WhatIf</span></span>
<span data-ttu-id="4dec9-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4dec9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dec9-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4dec9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dec9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dec9-136">CommonParameters</span></span>
<span data-ttu-id="4dec9-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4dec9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dec9-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dec9-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dec9-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4dec9-139">INPUTS</span></span>

### <span data-ttu-id="4dec9-140">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4dec9-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4dec9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4dec9-141">System.String</span></span>

## <span data-ttu-id="4dec9-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dec9-142">OUTPUTS</span></span>

### <span data-ttu-id="4dec9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4dec9-143">System.Boolean</span></span>

## <span data-ttu-id="4dec9-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="4dec9-144">NOTES</span></span>

## <span data-ttu-id="4dec9-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4dec9-145">RELATED LINKS</span></span>
