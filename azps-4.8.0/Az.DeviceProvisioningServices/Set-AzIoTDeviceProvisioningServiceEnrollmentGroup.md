---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: e7b0a5296147408633316ed27f0cba87a65d3a2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078293"
---
# <span data-ttu-id="7a956-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="7a956-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="7a956-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a956-102">SYNOPSIS</span></span>
<span data-ttu-id="7a956-103">Обновите группу регистрации устройств.</span><span class="sxs-lookup"><span data-stu-id="7a956-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="7a956-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a956-104">SYNTAX</span></span>

### <span data-ttu-id="7a956-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a956-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a956-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7a956-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a956-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7a956-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a956-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a956-108">DESCRIPTION</span></span>
<span data-ttu-id="7a956-109">Обновите группу регистрации в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="7a956-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="7a956-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a956-110">EXAMPLES</span></span>

### <span data-ttu-id="7a956-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a956-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="7a956-112">Обновление политики и концентраторов выделения для группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="7a956-112">Update allocation policy and hubs for an enrollment group.</span></span>

## <span data-ttu-id="7a956-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a956-113">PARAMETERS</span></span>

### <span data-ttu-id="7a956-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="7a956-114">-AllocationPolicy</span></span>
<span data-ttu-id="7a956-115">Тип выделения для устройства, назначенного концентратору.</span><span class="sxs-lookup"><span data-stu-id="7a956-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="7a956-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7a956-116">-ApiVersion</span></span>
<span data-ttu-id="7a956-117">Версия API службы подготовки в настраиваемом запросе на выделение.</span><span class="sxs-lookup"><span data-stu-id="7a956-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="7a956-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a956-118">-DefaultProfile</span></span>
<span data-ttu-id="7a956-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a956-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a956-120">-Необходимый</span><span class="sxs-lookup"><span data-stu-id="7a956-120">-Desired</span></span>
<span data-ttu-id="7a956-121">Начальные двойной нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="7a956-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="7a956-122">-DpsName</span><span class="sxs-lookup"><span data-stu-id="7a956-122">-DpsName</span></span>
<span data-ttu-id="7a956-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="7a956-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7a956-124">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="7a956-124">-DpsObject</span></span>
<span data-ttu-id="7a956-125">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="7a956-125">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7a956-126">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="7a956-126">-EdgeEnabled</span></span>
<span data-ttu-id="7a956-127">Флаг, указывающий на включение Edge.</span><span class="sxs-lookup"><span data-stu-id="7a956-127">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="7a956-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="7a956-128">-IotHub</span></span>
<span data-ttu-id="7a956-129">Имя узла целевого центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="7a956-129">Host name of target IoT Hub.</span></span>
<span data-ttu-id="7a956-130">Использование списка с разделителями-запятыми в нескольких центрах Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="7a956-130">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="7a956-131">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="7a956-131">-IotHubHostName</span></span>
<span data-ttu-id="7a956-132">Имя узла целевого центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="7a956-132">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="7a956-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7a956-133">-Name</span></span>
<span data-ttu-id="7a956-134">Имя группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="7a956-134">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="7a956-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="7a956-135">-ProvisioningStatus</span></span>
<span data-ttu-id="7a956-136">Включите или отключите регистрационную запись.</span><span class="sxs-lookup"><span data-stu-id="7a956-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="7a956-137">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="7a956-137">-ReprovisionPolicy</span></span>
<span data-ttu-id="7a956-138">Данные устройства, которые должны быть обработаны при повторной подготовке к разным центрам Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="7a956-138">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="7a956-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a956-139">-ResourceGroupName</span></span>
<span data-ttu-id="7a956-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7a956-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7a956-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a956-141">-ResourceId</span></span>
<span data-ttu-id="7a956-142">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="7a956-142">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7a956-143">-Тег</span><span class="sxs-lookup"><span data-stu-id="7a956-143">-Tag</span></span>
<span data-ttu-id="7a956-144">Начальные Теги двойной.</span><span class="sxs-lookup"><span data-stu-id="7a956-144">Initial twin tags.</span></span>

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

### <span data-ttu-id="7a956-145">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="7a956-145">-WebhookUrl</span></span>
<span data-ttu-id="7a956-146">URL-адрес веб-перехватчика, используемый для настраиваемых запросов на выделение.</span><span class="sxs-lookup"><span data-stu-id="7a956-146">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="7a956-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a956-147">-Confirm</span></span>
<span data-ttu-id="7a956-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a956-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a956-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a956-149">-WhatIf</span></span>
<span data-ttu-id="7a956-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a956-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a956-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a956-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a956-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a956-152">CommonParameters</span></span>
<span data-ttu-id="7a956-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a956-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a956-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a956-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a956-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a956-155">INPUTS</span></span>

### <span data-ttu-id="7a956-156">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="7a956-156">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="7a956-157">System. String</span><span class="sxs-lookup"><span data-stu-id="7a956-157">System.String</span></span>

## <span data-ttu-id="7a956-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a956-158">OUTPUTS</span></span>

### <span data-ttu-id="7a956-159">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="7a956-159">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="7a956-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a956-160">NOTES</span></span>

## <span data-ttu-id="7a956-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a956-161">RELATED LINKS</span></span>
