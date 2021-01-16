---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 47c5c5119e41f3feeaccda66871d902e631c9ac2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396628"
---
# <span data-ttu-id="4c1ea-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="4c1ea-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="4c1ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c1ea-102">SYNOPSIS</span></span>
<span data-ttu-id="4c1ea-103">Обновив запись регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="4c1ea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4c1ea-104">SYNTAX</span></span>

### <span data-ttu-id="4c1ea-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4c1ea-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c1ea-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4c1ea-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c1ea-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4c1ea-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c1ea-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c1ea-108">DESCRIPTION</span></span>
<span data-ttu-id="4c1ea-109">Обновив регистрацию устройства в службе azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4c1ea-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4c1ea-110">EXAMPLES</span></span>

### <span data-ttu-id="4c1ea-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4c1ea-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="4c1ea-112">Обновив политику выделения и концентраторы для записи о регистрации.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="4c1ea-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4c1ea-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="4c1ea-114">Обновив начальное состояние регистрации.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-114">Update an enrollment's initial twin state.</span></span>

## <span data-ttu-id="4c1ea-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c1ea-115">PARAMETERS</span></span>

### <span data-ttu-id="4c1ea-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="4c1ea-116">-AllocationPolicy</span></span>
<span data-ttu-id="4c1ea-117">Тип выделения для устройства, назначенного Центру.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="4c1ea-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4c1ea-118">-ApiVersion</span></span>
<span data-ttu-id="4c1ea-119">Версия API службы предварительной настройки в настраиваемом запросе на выделение.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="4c1ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c1ea-120">-DefaultProfile</span></span>
<span data-ttu-id="4c1ea-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c1ea-122">-Desired</span><span class="sxs-lookup"><span data-stu-id="4c1ea-122">-Desired</span></span>
<span data-ttu-id="4c1ea-123">Начальное желаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="4c1ea-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4c1ea-124">-DeviceId</span></span>
<span data-ttu-id="4c1ea-125">IoT Hub Device IoT IOT Device IoT IoT.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-125">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="4c1ea-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="4c1ea-126">-DpsName</span></span>
<span data-ttu-id="4c1ea-127">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="4c1ea-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4c1ea-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4c1ea-128">-DpsObject</span></span>
<span data-ttu-id="4c1ea-129">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="4c1ea-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4c1ea-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="4c1ea-130">-EdgeEnabled</span></span>
<span data-ttu-id="4c1ea-131">Пометка, указывающая на то, что граница включается.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="4c1ea-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="4c1ea-132">-IotHub</span></span>
<span data-ttu-id="4c1ea-133">Host name of target IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="4c1ea-134">Используйте список с разделами между пробелами для нескольких концентраторов IoT.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="4c1ea-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="4c1ea-135">-IotHubHostName</span></span>
<span data-ttu-id="4c1ea-136">Имя целевого концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="4c1ea-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="4c1ea-137">-ProvisioningStatus</span></span>
<span data-ttu-id="4c1ea-138">Включить или отключить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="4c1ea-139">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="4c1ea-139">-RegistrationId</span></span>
<span data-ttu-id="4c1ea-140">Индивидуальный регистрационный номер.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-140">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="4c1ea-141">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="4c1ea-141">-ReprovisionPolicy</span></span>
<span data-ttu-id="4c1ea-142">Данные устройств, обрабатываемые при повторной под подготовка к другому центру IOT.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-142">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="4c1ea-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c1ea-143">-ResourceGroupName</span></span>
<span data-ttu-id="4c1ea-144">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4c1ea-144">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4c1ea-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c1ea-145">-ResourceId</span></span>
<span data-ttu-id="4c1ea-146">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="4c1ea-146">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4c1ea-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="4c1ea-147">-Tag</span></span>
<span data-ttu-id="4c1ea-148">Первичные теги.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-148">Initial twin tags.</span></span>

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

### <span data-ttu-id="4c1ea-149">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="4c1ea-149">-WebhookUrl</span></span>
<span data-ttu-id="4c1ea-150">URL-адрес веб-сайта, используемый для пользовательских запросов на выделение ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-150">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="4c1ea-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c1ea-151">-Confirm</span></span>
<span data-ttu-id="4c1ea-152">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c1ea-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c1ea-153">-WhatIf</span></span>
<span data-ttu-id="4c1ea-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c1ea-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c1ea-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c1ea-156">CommonParameters</span></span>
<span data-ttu-id="4c1ea-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c1ea-158">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c1ea-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c1ea-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c1ea-159">INPUTS</span></span>

### <span data-ttu-id="4c1ea-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4c1ea-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4c1ea-161">System.String</span><span class="sxs-lookup"><span data-stu-id="4c1ea-161">System.String</span></span>

## <span data-ttu-id="4c1ea-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4c1ea-162">OUTPUTS</span></span>

### <span data-ttu-id="4c1ea-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="4c1ea-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="4c1ea-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4c1ea-164">NOTES</span></span>

## <span data-ttu-id="4c1ea-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c1ea-165">RELATED LINKS</span></span>