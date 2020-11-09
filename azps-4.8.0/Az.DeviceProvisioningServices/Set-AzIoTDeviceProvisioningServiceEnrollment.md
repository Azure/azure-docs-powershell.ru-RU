---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8a81df2081420f8d218e094ff43f22e8dd9cc5c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243611"
---
# <span data-ttu-id="9ff39-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="9ff39-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="9ff39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ff39-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff39-103">Обновите запись регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="9ff39-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="9ff39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ff39-104">SYNTAX</span></span>

### <span data-ttu-id="9ff39-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ff39-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ff39-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9ff39-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ff39-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9ff39-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ff39-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ff39-108">DESCRIPTION</span></span>
<span data-ttu-id="9ff39-109">Обновите регистрацию устройства в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="9ff39-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="9ff39-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ff39-110">EXAMPLES</span></span>

### <span data-ttu-id="9ff39-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ff39-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="9ff39-112">Обновление политики и концентраторов выделения для записи регистрации.</span><span class="sxs-lookup"><span data-stu-id="9ff39-112">Update allocation policy and hubs for an enrollment record.</span></span>

## <span data-ttu-id="9ff39-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ff39-113">PARAMETERS</span></span>

### <span data-ttu-id="9ff39-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="9ff39-114">-AllocationPolicy</span></span>
<span data-ttu-id="9ff39-115">Тип выделения для устройства, назначенного концентратору.</span><span class="sxs-lookup"><span data-stu-id="9ff39-115">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff39-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9ff39-116">-ApiVersion</span></span>
<span data-ttu-id="9ff39-117">Версия API службы подготовки в настраиваемом запросе на выделение.</span><span class="sxs-lookup"><span data-stu-id="9ff39-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="9ff39-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff39-118">-DefaultProfile</span></span>
<span data-ttu-id="9ff39-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff39-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ff39-120">-Необходимый</span><span class="sxs-lookup"><span data-stu-id="9ff39-120">-Desired</span></span>
<span data-ttu-id="9ff39-121">Начальные двойной нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="9ff39-121">Initial twin desired properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff39-122">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9ff39-122">-DeviceId</span></span>
<span data-ttu-id="9ff39-123">ИДЕНТИФИКАТОР устройства центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="9ff39-123">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="9ff39-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="9ff39-124">-DpsName</span></span>
<span data-ttu-id="9ff39-125">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="9ff39-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9ff39-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="9ff39-126">-DpsObject</span></span>
<span data-ttu-id="9ff39-127">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="9ff39-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9ff39-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9ff39-128">-EdgeEnabled</span></span>
<span data-ttu-id="9ff39-129">Флаг, указывающий на включение Edge.</span><span class="sxs-lookup"><span data-stu-id="9ff39-129">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff39-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="9ff39-130">-IotHub</span></span>
<span data-ttu-id="9ff39-131">Имя узла целевого центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="9ff39-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="9ff39-132">Использование списка с разделителями-запятыми в нескольких центрах Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="9ff39-132">Use space-separated list for multiple IoT Hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff39-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="9ff39-133">-IotHubHostName</span></span>
<span data-ttu-id="9ff39-134">Имя узла целевого центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="9ff39-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="9ff39-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="9ff39-135">-ProvisioningStatus</span></span>
<span data-ttu-id="9ff39-136">Включите или отключите регистрационную запись.</span><span class="sxs-lookup"><span data-stu-id="9ff39-136">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff39-137">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="9ff39-137">-RegistrationId</span></span>
<span data-ttu-id="9ff39-138">Регистрационный код отдельной регистрации.</span><span class="sxs-lookup"><span data-stu-id="9ff39-138">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="9ff39-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="9ff39-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="9ff39-140">Данные устройства, которые должны быть обработаны при повторной подготовке к разным центрам Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="9ff39-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff39-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff39-141">-ResourceGroupName</span></span>
<span data-ttu-id="9ff39-142">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9ff39-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9ff39-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ff39-143">-ResourceId</span></span>
<span data-ttu-id="9ff39-144">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="9ff39-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9ff39-145">-Тег</span><span class="sxs-lookup"><span data-stu-id="9ff39-145">-Tag</span></span>
<span data-ttu-id="9ff39-146">Начальные Теги двойной.</span><span class="sxs-lookup"><span data-stu-id="9ff39-146">Initial twin tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff39-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="9ff39-147">-WebhookUrl</span></span>
<span data-ttu-id="9ff39-148">URL-адрес веб-перехватчика, используемый для настраиваемых запросов на выделение.</span><span class="sxs-lookup"><span data-stu-id="9ff39-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="9ff39-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ff39-149">-Confirm</span></span>
<span data-ttu-id="9ff39-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9ff39-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ff39-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff39-151">-WhatIf</span></span>
<span data-ttu-id="9ff39-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9ff39-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ff39-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9ff39-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ff39-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff39-154">CommonParameters</span></span>
<span data-ttu-id="9ff39-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ff39-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff39-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff39-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff39-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ff39-157">INPUTS</span></span>

### <span data-ttu-id="9ff39-158">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9ff39-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="9ff39-159">System. String</span><span class="sxs-lookup"><span data-stu-id="9ff39-159">System.String</span></span>

## <span data-ttu-id="9ff39-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ff39-160">OUTPUTS</span></span>

### <span data-ttu-id="9ff39-161">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="9ff39-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="9ff39-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ff39-162">NOTES</span></span>

## <span data-ttu-id="9ff39-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ff39-163">RELATED LINKS</span></span>