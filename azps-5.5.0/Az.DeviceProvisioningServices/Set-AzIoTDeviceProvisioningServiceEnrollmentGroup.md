---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 3982279b8698a84f23bc83aeccd25083d98363f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228545"
---
# <span data-ttu-id="46e7a-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="46e7a-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="46e7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="46e7a-103">Обновив группу регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="46e7a-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="46e7a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46e7a-104">SYNTAX</span></span>

### <span data-ttu-id="46e7a-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46e7a-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46e7a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="46e7a-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46e7a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="46e7a-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46e7a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46e7a-108">DESCRIPTION</span></span>
<span data-ttu-id="46e7a-109">Обновив группу регистрации в службе регистрации устройств на концентраторе Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="46e7a-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="46e7a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46e7a-110">EXAMPLES</span></span>

### <span data-ttu-id="46e7a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46e7a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="46e7a-112">Обновив политику выделения и концентраторы для группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="46e7a-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="46e7a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="46e7a-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="46e7a-114">Обновив начальное состояние группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="46e7a-114">Update an enrollment group's initial twin state.</span></span>

## <span data-ttu-id="46e7a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46e7a-115">PARAMETERS</span></span>

### <span data-ttu-id="46e7a-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="46e7a-116">-AllocationPolicy</span></span>
<span data-ttu-id="46e7a-117">Тип выделения для устройства, назначенного Центру.</span><span class="sxs-lookup"><span data-stu-id="46e7a-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="46e7a-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="46e7a-118">-ApiVersion</span></span>
<span data-ttu-id="46e7a-119">Версия API службы подготовка в настраиваемом запросе на выделение.</span><span class="sxs-lookup"><span data-stu-id="46e7a-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="46e7a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e7a-120">-DefaultProfile</span></span>
<span data-ttu-id="46e7a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46e7a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46e7a-122">-Desired</span><span class="sxs-lookup"><span data-stu-id="46e7a-122">-Desired</span></span>
<span data-ttu-id="46e7a-123">Начальное желаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="46e7a-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="46e7a-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="46e7a-124">-DpsName</span></span>
<span data-ttu-id="46e7a-125">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="46e7a-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="46e7a-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="46e7a-126">-DpsObject</span></span>
<span data-ttu-id="46e7a-127">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="46e7a-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="46e7a-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="46e7a-128">-EdgeEnabled</span></span>
<span data-ttu-id="46e7a-129">Пометка, указывающая на то, что граница включается.</span><span class="sxs-lookup"><span data-stu-id="46e7a-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="46e7a-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="46e7a-130">-IotHub</span></span>
<span data-ttu-id="46e7a-131">Host name of target IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="46e7a-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="46e7a-132">Используйте список с разделами между пробелами для нескольких концентраторов IoT.</span><span class="sxs-lookup"><span data-stu-id="46e7a-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="46e7a-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="46e7a-133">-IotHubHostName</span></span>
<span data-ttu-id="46e7a-134">Имя целевого концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="46e7a-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="46e7a-135">-Name</span><span class="sxs-lookup"><span data-stu-id="46e7a-135">-Name</span></span>
<span data-ttu-id="46e7a-136">Имя группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="46e7a-136">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="46e7a-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="46e7a-137">-ProvisioningStatus</span></span>
<span data-ttu-id="46e7a-138">Включить или отключить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="46e7a-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="46e7a-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="46e7a-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="46e7a-140">Данные устройств, обрабатываемые при повторной под подготовка к другому центру IOT.</span><span class="sxs-lookup"><span data-stu-id="46e7a-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="46e7a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e7a-141">-ResourceGroupName</span></span>
<span data-ttu-id="46e7a-142">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="46e7a-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="46e7a-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46e7a-143">-ResourceId</span></span>
<span data-ttu-id="46e7a-144">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="46e7a-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="46e7a-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="46e7a-145">-Tag</span></span>
<span data-ttu-id="46e7a-146">Первичные теги.</span><span class="sxs-lookup"><span data-stu-id="46e7a-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="46e7a-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="46e7a-147">-WebhookUrl</span></span>
<span data-ttu-id="46e7a-148">URL-адрес веб-сайта, используемый для пользовательских запросов на выделение ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46e7a-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="46e7a-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46e7a-149">-Confirm</span></span>
<span data-ttu-id="46e7a-150">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="46e7a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46e7a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e7a-151">-WhatIf</span></span>
<span data-ttu-id="46e7a-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46e7a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46e7a-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="46e7a-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46e7a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e7a-154">CommonParameters</span></span>
<span data-ttu-id="46e7a-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e7a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e7a-156">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e7a-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e7a-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46e7a-157">INPUTS</span></span>

### <span data-ttu-id="46e7a-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="46e7a-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="46e7a-159">System.String</span><span class="sxs-lookup"><span data-stu-id="46e7a-159">System.String</span></span>

## <span data-ttu-id="46e7a-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46e7a-160">OUTPUTS</span></span>

### <span data-ttu-id="46e7a-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="46e7a-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="46e7a-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46e7a-162">NOTES</span></span>

## <span data-ttu-id="46e7a-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46e7a-163">RELATED LINKS</span></span>
