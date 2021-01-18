---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 3982279b8698a84f23bc83aeccd25083d98363f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506312"
---
# <span data-ttu-id="e665f-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="e665f-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="e665f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e665f-102">SYNOPSIS</span></span>
<span data-ttu-id="e665f-103">Обновив группу регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="e665f-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="e665f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e665f-104">SYNTAX</span></span>

### <span data-ttu-id="e665f-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e665f-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e665f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e665f-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e665f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e665f-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e665f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e665f-108">DESCRIPTION</span></span>
<span data-ttu-id="e665f-109">Обновив группу регистрации в службе регистрации устройств на концентраторе Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e665f-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="e665f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e665f-110">EXAMPLES</span></span>

### <span data-ttu-id="e665f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e665f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="e665f-112">Обновив политику выделения и концентраторы для группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="e665f-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="e665f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e665f-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="e665f-114">Обновив начальное состояние группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="e665f-114">Update an enrollment group's initial twin state.</span></span>

## <span data-ttu-id="e665f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e665f-115">PARAMETERS</span></span>

### <span data-ttu-id="e665f-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="e665f-116">-AllocationPolicy</span></span>
<span data-ttu-id="e665f-117">Тип выделения для устройства, назначенного Центру.</span><span class="sxs-lookup"><span data-stu-id="e665f-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="e665f-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e665f-118">-ApiVersion</span></span>
<span data-ttu-id="e665f-119">Версия API службы подготовка в настраиваемом запросе на выделение.</span><span class="sxs-lookup"><span data-stu-id="e665f-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="e665f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e665f-120">-DefaultProfile</span></span>
<span data-ttu-id="e665f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e665f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e665f-122">-Desired</span><span class="sxs-lookup"><span data-stu-id="e665f-122">-Desired</span></span>
<span data-ttu-id="e665f-123">Начальное желаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e665f-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="e665f-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="e665f-124">-DpsName</span></span>
<span data-ttu-id="e665f-125">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="e665f-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e665f-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="e665f-126">-DpsObject</span></span>
<span data-ttu-id="e665f-127">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="e665f-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="e665f-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="e665f-128">-EdgeEnabled</span></span>
<span data-ttu-id="e665f-129">Пометка, указывающая на то, что граница включается.</span><span class="sxs-lookup"><span data-stu-id="e665f-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="e665f-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="e665f-130">-IotHub</span></span>
<span data-ttu-id="e665f-131">Host name of target IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="e665f-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="e665f-132">Используйте список с разделами между пробелами для нескольких концентраторов IoT.</span><span class="sxs-lookup"><span data-stu-id="e665f-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="e665f-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="e665f-133">-IotHubHostName</span></span>
<span data-ttu-id="e665f-134">Имя целевого концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="e665f-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="e665f-135">-Name</span><span class="sxs-lookup"><span data-stu-id="e665f-135">-Name</span></span>
<span data-ttu-id="e665f-136">Имя группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="e665f-136">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="e665f-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="e665f-137">-ProvisioningStatus</span></span>
<span data-ttu-id="e665f-138">Включить или отключить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="e665f-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="e665f-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="e665f-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="e665f-140">Данные устройств, обрабатываемые при повторной под подготовка к другому центру IOT.</span><span class="sxs-lookup"><span data-stu-id="e665f-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="e665f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e665f-141">-ResourceGroupName</span></span>
<span data-ttu-id="e665f-142">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e665f-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e665f-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e665f-143">-ResourceId</span></span>
<span data-ttu-id="e665f-144">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="e665f-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="e665f-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="e665f-145">-Tag</span></span>
<span data-ttu-id="e665f-146">Первичные теги.</span><span class="sxs-lookup"><span data-stu-id="e665f-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="e665f-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="e665f-147">-WebhookUrl</span></span>
<span data-ttu-id="e665f-148">URL-адрес веб-сайта, используемый для пользовательских запросов на выделение ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e665f-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="e665f-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e665f-149">-Confirm</span></span>
<span data-ttu-id="e665f-150">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e665f-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e665f-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e665f-151">-WhatIf</span></span>
<span data-ttu-id="e665f-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e665f-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e665f-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e665f-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e665f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e665f-154">CommonParameters</span></span>
<span data-ttu-id="e665f-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e665f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e665f-156">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e665f-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e665f-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e665f-157">INPUTS</span></span>

### <span data-ttu-id="e665f-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="e665f-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="e665f-159">System.String</span><span class="sxs-lookup"><span data-stu-id="e665f-159">System.String</span></span>

## <span data-ttu-id="e665f-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e665f-160">OUTPUTS</span></span>

### <span data-ttu-id="e665f-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="e665f-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="e665f-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e665f-162">NOTES</span></span>

## <span data-ttu-id="e665f-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e665f-163">RELATED LINKS</span></span>
