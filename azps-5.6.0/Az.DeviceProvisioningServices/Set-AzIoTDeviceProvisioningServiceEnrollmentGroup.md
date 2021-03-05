---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 511d0445f7c27acf7ace059852f6e4a8b23655b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985074"
---
# <span data-ttu-id="7b3d5-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="7b3d5-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="7b3d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b3d5-102">SYNOPSIS</span></span>
<span data-ttu-id="7b3d5-103">Обновив группу регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="7b3d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7b3d5-104">SYNTAX</span></span>

### <span data-ttu-id="7b3d5-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b3d5-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b3d5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7b3d5-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b3d5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7b3d5-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b3d5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b3d5-108">DESCRIPTION</span></span>
<span data-ttu-id="7b3d5-109">Обновив группу регистрации в службе регистрации устройств на концентраторе Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="7b3d5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7b3d5-110">EXAMPLES</span></span>

### <span data-ttu-id="7b3d5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b3d5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="7b3d5-112">Обновив политику выделения и концентраторы для группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="7b3d5-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7b3d5-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="7b3d5-114">Обновив начальное состояние группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-114">Update an enrollment group's initial twin state.</span></span>

### <span data-ttu-id="7b3d5-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7b3d5-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -PrimaryKey "newPrimaryKey" -SecondaryKey "newSecondaryKey"
```

<span data-ttu-id="7b3d5-116">Обновление первичных и дополнительных ключей группы симметричных ключей</span><span class="sxs-lookup"><span data-stu-id="7b3d5-116">Update a symmetric key enrollment group's primary and secondary keys</span></span>

## <span data-ttu-id="7b3d5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b3d5-117">PARAMETERS</span></span>

### <span data-ttu-id="7b3d5-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="7b3d5-118">-AllocationPolicy</span></span>
<span data-ttu-id="7b3d5-119">Тип выделения для устройства, назначенного Центру.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="7b3d5-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7b3d5-120">-ApiVersion</span></span>
<span data-ttu-id="7b3d5-121">Версия API службы подготовка в настраиваемом запросе на выделение.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="7b3d5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b3d5-122">-DefaultProfile</span></span>
<span data-ttu-id="7b3d5-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b3d5-124">-Desired</span><span class="sxs-lookup"><span data-stu-id="7b3d5-124">-Desired</span></span>
<span data-ttu-id="7b3d5-125">Начальное желаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="7b3d5-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="7b3d5-126">-DpsName</span></span>
<span data-ttu-id="7b3d5-127">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="7b3d5-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7b3d5-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="7b3d5-128">-DpsObject</span></span>
<span data-ttu-id="7b3d5-129">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="7b3d5-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7b3d5-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="7b3d5-130">-EdgeEnabled</span></span>
<span data-ttu-id="7b3d5-131">Пометка, указывающая на то, что граница включается.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="7b3d5-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="7b3d5-132">-IotHub</span></span>
<span data-ttu-id="7b3d5-133">Host name of target IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="7b3d5-134">Используйте список с разделами между пробелами для нескольких концентраторов IoT.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="7b3d5-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="7b3d5-135">-IotHubHostName</span></span>
<span data-ttu-id="7b3d5-136">Имя целевого концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="7b3d5-137">-Name</span><span class="sxs-lookup"><span data-stu-id="7b3d5-137">-Name</span></span>
<span data-ttu-id="7b3d5-138">Имя группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-138">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="7b3d5-139">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="7b3d5-139">-PrimaryCAName</span></span>
<span data-ttu-id="7b3d5-140">Имя основного корневого сертификата ЦС.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-140">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="7b3d5-141">Если при проверке необходимо использовать корневой сертификат ЦС, необходимо у назвать корневой ЦС.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-141">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="7b3d5-142">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="7b3d5-142">-PrimaryCertificate</span></span>
<span data-ttu-id="7b3d5-143">Путь к файлу, содержащего основной сертификат.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-143">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="7b3d5-144">Представление файла сертификата X509 (cer) или пути к PEM-файлу (Base-64).</span><span class="sxs-lookup"><span data-stu-id="7b3d5-144">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="7b3d5-145">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7b3d5-145">-PrimaryKey</span></span>
<span data-ttu-id="7b3d5-146">Первичный симметричный ключ общего доступа, сохраненный в формате base64.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-146">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="7b3d5-147">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="7b3d5-147">-ProvisioningStatus</span></span>
<span data-ttu-id="7b3d5-148">Включить или отключить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-148">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="7b3d5-149">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b3d5-149">-ReprovisionPolicy</span></span>
<span data-ttu-id="7b3d5-150">Данные устройств, обрабатываемые при повторной под подготовка к другому центру IOT.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-150">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="7b3d5-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b3d5-151">-ResourceGroupName</span></span>
<span data-ttu-id="7b3d5-152">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7b3d5-152">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7b3d5-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b3d5-153">-ResourceId</span></span>
<span data-ttu-id="7b3d5-154">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="7b3d5-154">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7b3d5-155">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="7b3d5-155">-RootCertificate</span></span>
<span data-ttu-id="7b3d5-156">Позволяет создавать проверку X509attestation с использованием корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-156">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="7b3d5-157">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="7b3d5-157">-SecondaryCAName</span></span>
<span data-ttu-id="7b3d5-158">Имя сертификата дополнительного корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-158">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="7b3d5-159">Если при проверке необходимо использовать корневой сертификат ЦС, необходимо у назвать корневой ЦС.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-159">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="7b3d5-160">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="7b3d5-160">-SecondaryCertificate</span></span>
<span data-ttu-id="7b3d5-161">Путь к файлу, содержащего дополнительный сертификат.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-161">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="7b3d5-162">Представление файла сертификата X509 (cer) или пути к PEM-файлу (Base-64).</span><span class="sxs-lookup"><span data-stu-id="7b3d5-162">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="7b3d5-163">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7b3d5-163">-SecondaryKey</span></span>
<span data-ttu-id="7b3d5-164">Дополнительный симметричный ключ общего доступа, сохраненный в формате base64.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-164">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="7b3d5-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b3d5-165">-Tag</span></span>
<span data-ttu-id="7b3d5-166">Первичные теги.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-166">Initial twin tags.</span></span>

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

### <span data-ttu-id="7b3d5-167">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="7b3d5-167">-WebhookUrl</span></span>
<span data-ttu-id="7b3d5-168">URL-адрес веб-сайта, используемый для пользовательских запросов на выделение ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-168">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="7b3d5-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b3d5-169">-Confirm</span></span>
<span data-ttu-id="7b3d5-170">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b3d5-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b3d5-171">-WhatIf</span></span>
<span data-ttu-id="7b3d5-172">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b3d5-173">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b3d5-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b3d5-174">CommonParameters</span></span>
<span data-ttu-id="7b3d5-175">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b3d5-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b3d5-176">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b3d5-176">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b3d5-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b3d5-177">INPUTS</span></span>

### <span data-ttu-id="7b3d5-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="7b3d5-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="7b3d5-179">System.String</span><span class="sxs-lookup"><span data-stu-id="7b3d5-179">System.String</span></span>

## <span data-ttu-id="7b3d5-180">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7b3d5-180">OUTPUTS</span></span>

### <span data-ttu-id="7b3d5-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="7b3d5-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="7b3d5-182">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7b3d5-182">NOTES</span></span>

## <span data-ttu-id="7b3d5-183">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b3d5-183">RELATED LINKS</span></span>
