---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7000d7cc6922cec022efad9faca2e61e539af0e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398439"
---
# <span data-ttu-id="ff2ac-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="ff2ac-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="ff2ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ff2ac-103">Создайте группу регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="ff2ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff2ac-104">SYNTAX</span></span>

### <span data-ttu-id="ff2ac-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff2ac-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff2ac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ff2ac-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff2ac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ff2ac-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff2ac-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff2ac-108">DESCRIPTION</span></span>
<span data-ttu-id="ff2ac-109">Создайте группу регистрации в службе azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="ff2ac-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff2ac-110">EXAMPLES</span></span>

### <span data-ttu-id="ff2ac-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff2ac-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="ff2ac-112">Создание регистрации с типом attestation SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="ff2ac-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="ff2ac-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ff2ac-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="ff2ac-114">Создание регистрации с типом attestation X509</span><span class="sxs-lookup"><span data-stu-id="ff2ac-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="ff2ac-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ff2ac-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="ff2ac-116">Создайте регистрацию с типом attestation SymmetricKey и первоначальным состоянием</span><span class="sxs-lookup"><span data-stu-id="ff2ac-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="ff2ac-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff2ac-117">PARAMETERS</span></span>

### <span data-ttu-id="ff2ac-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ff2ac-118">-AllocationPolicy</span></span>
<span data-ttu-id="ff2ac-119">Тип выделения для устройства, назначенного Центру.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="ff2ac-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ff2ac-120">-ApiVersion</span></span>
<span data-ttu-id="ff2ac-121">Версия API службы подготовка в настраиваемом запросе на выделение.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="ff2ac-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="ff2ac-122">-AttestationType</span></span>
<span data-ttu-id="ff2ac-123">Механизм проверки.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-123">Attestation Mechanism.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAttestationMechanismType
Parameter Sets: (All)
Aliases:
Accepted values: None, Tpm, X509, SymmetricKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2ac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff2ac-124">-DefaultProfile</span></span>
<span data-ttu-id="ff2ac-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff2ac-126">-Desired</span><span class="sxs-lookup"><span data-stu-id="ff2ac-126">-Desired</span></span>
<span data-ttu-id="ff2ac-127">Начальное желаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="ff2ac-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="ff2ac-128">-DpsName</span></span>
<span data-ttu-id="ff2ac-129">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="ff2ac-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ff2ac-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="ff2ac-130">-DpsObject</span></span>
<span data-ttu-id="ff2ac-131">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="ff2ac-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ff2ac-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="ff2ac-132">-EdgeEnabled</span></span>
<span data-ttu-id="ff2ac-133">Пометка, указывающая на то, что граница включается.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="ff2ac-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="ff2ac-134">-IotHub</span></span>
<span data-ttu-id="ff2ac-135">Host name of target IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="ff2ac-136">Используйте список с разделами между пробелами для нескольких концентраторов IoT.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="ff2ac-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="ff2ac-137">-IotHubHostName</span></span>
<span data-ttu-id="ff2ac-138">Имя целевого концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="ff2ac-139">-Name</span><span class="sxs-lookup"><span data-stu-id="ff2ac-139">-Name</span></span>
<span data-ttu-id="ff2ac-140">Имя группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="ff2ac-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="ff2ac-141">-PrimaryCAName</span></span>
<span data-ttu-id="ff2ac-142">Имя основного корневого сертификата ЦС.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="ff2ac-143">Если при проверке необходимо использовать корневой сертификат ЦС, необходимо у назвать корневой ЦС.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="ff2ac-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="ff2ac-144">-PrimaryCertificate</span></span>
<span data-ttu-id="ff2ac-145">Путь к файлу, содержащего основной сертификат.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="ff2ac-146">Представление файла сертификата X509 (cer) или пути к PEM-файлу (Base-64).</span><span class="sxs-lookup"><span data-stu-id="ff2ac-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="ff2ac-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ff2ac-147">-PrimaryKey</span></span>
<span data-ttu-id="ff2ac-148">Первичный симметричный ключ общего доступа, сохраненный в формате base64.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="ff2ac-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="ff2ac-149">-ProvisioningStatus</span></span>
<span data-ttu-id="ff2ac-150">Включить или отключить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="ff2ac-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff2ac-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="ff2ac-152">Данные устройств, обрабатываемые при повторной под подготовка к другому центру IOT.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="ff2ac-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff2ac-153">-ResourceGroupName</span></span>
<span data-ttu-id="ff2ac-154">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ff2ac-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ff2ac-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff2ac-155">-ResourceId</span></span>
<span data-ttu-id="ff2ac-156">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="ff2ac-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ff2ac-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="ff2ac-157">-RootCertificate</span></span>
<span data-ttu-id="ff2ac-158">Позволяет создавать проверки X509attestation с использованием корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="ff2ac-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="ff2ac-159">-SecondaryCAName</span></span>
<span data-ttu-id="ff2ac-160">Имя сертификата дополнительного корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="ff2ac-161">Если при проверке необходимо использовать корневой сертификат ЦС, необходимо у назвать корневой ЦС.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="ff2ac-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="ff2ac-162">-SecondaryCertificate</span></span>
<span data-ttu-id="ff2ac-163">Путь к файлу, содержащего дополнительный сертификат.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="ff2ac-164">Представление файла сертификата X509 (cer) или пути к PEM-файлу (Base-64).</span><span class="sxs-lookup"><span data-stu-id="ff2ac-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="ff2ac-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ff2ac-165">-SecondaryKey</span></span>
<span data-ttu-id="ff2ac-166">Дополнительный симметричный ключ общего доступа, сохраненный в формате base64.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="ff2ac-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff2ac-167">-Tag</span></span>
<span data-ttu-id="ff2ac-168">Первичные теги.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="ff2ac-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="ff2ac-169">-WebhookUrl</span></span>
<span data-ttu-id="ff2ac-170">URL-адрес веб-сайта, используемый для пользовательских запросов на выделение ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="ff2ac-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff2ac-171">-Confirm</span></span>
<span data-ttu-id="ff2ac-172">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff2ac-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff2ac-173">-WhatIf</span></span>
<span data-ttu-id="ff2ac-174">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff2ac-175">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff2ac-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff2ac-176">CommonParameters</span></span>
<span data-ttu-id="ff2ac-177">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff2ac-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff2ac-178">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff2ac-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff2ac-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff2ac-179">INPUTS</span></span>

### <span data-ttu-id="ff2ac-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ff2ac-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="ff2ac-181">System.String</span><span class="sxs-lookup"><span data-stu-id="ff2ac-181">System.String</span></span>

## <span data-ttu-id="ff2ac-182">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff2ac-182">OUTPUTS</span></span>

### <span data-ttu-id="ff2ac-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="ff2ac-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="ff2ac-184">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff2ac-184">NOTES</span></span>

## <span data-ttu-id="ff2ac-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff2ac-185">RELATED LINKS</span></span>
