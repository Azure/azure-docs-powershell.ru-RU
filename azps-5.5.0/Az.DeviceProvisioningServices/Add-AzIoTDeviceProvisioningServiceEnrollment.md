---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: b3c97abdee88615eedb2bb1f4452309326a4ebfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230476"
---
# <span data-ttu-id="38e94-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="38e94-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="38e94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38e94-102">SYNOPSIS</span></span>
<span data-ttu-id="38e94-103">Создайте запись регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="38e94-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="38e94-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="38e94-104">SYNTAX</span></span>

### <span data-ttu-id="38e94-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38e94-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38e94-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="38e94-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38e94-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="38e94-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 -AttestationType <PSAttestationMechanismType> [-DeviceId <String>] [-EndorsementKey <String>]
 [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38e94-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38e94-108">DESCRIPTION</span></span>
<span data-ttu-id="38e94-109">Создайте регистрацию устройства в службе azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="38e94-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="38e94-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="38e94-110">EXAMPLES</span></span>

### <span data-ttu-id="38e94-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="38e94-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="38e94-112">Создание регистрации с типом attestation SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="38e94-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="38e94-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="38e94-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="38e94-114">Создайте регистрацию с помощью проверки TPM.</span><span class="sxs-lookup"><span data-stu-id="38e94-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="38e94-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="38e94-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="38e94-116">Создание регистрации с типом attestation X509</span><span class="sxs-lookup"><span data-stu-id="38e94-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="38e94-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="38e94-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="38e94-118">Создайте регистрацию с типом attestation SymmetricKey и первоначальным состоянием</span><span class="sxs-lookup"><span data-stu-id="38e94-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="38e94-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38e94-119">PARAMETERS</span></span>

### <span data-ttu-id="38e94-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="38e94-120">-AllocationPolicy</span></span>
<span data-ttu-id="38e94-121">Тип выделения для устройства, назначенного Центру.</span><span class="sxs-lookup"><span data-stu-id="38e94-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="38e94-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="38e94-122">-ApiVersion</span></span>
<span data-ttu-id="38e94-123">Версия API службы предварительной настройки в настраиваемом запросе на выделение.</span><span class="sxs-lookup"><span data-stu-id="38e94-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="38e94-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="38e94-124">-AttestationType</span></span>
<span data-ttu-id="38e94-125">Механизм проверки.</span><span class="sxs-lookup"><span data-stu-id="38e94-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="38e94-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38e94-126">-DefaultProfile</span></span>
<span data-ttu-id="38e94-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38e94-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38e94-128">-Desired</span><span class="sxs-lookup"><span data-stu-id="38e94-128">-Desired</span></span>
<span data-ttu-id="38e94-129">Начальное желаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="38e94-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="38e94-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="38e94-130">-DeviceId</span></span>
<span data-ttu-id="38e94-131">IoT Hub Device IoT IoT Device IoT IoT Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="38e94-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="38e94-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="38e94-132">-DpsName</span></span>
<span data-ttu-id="38e94-133">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="38e94-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="38e94-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="38e94-134">-DpsObject</span></span>
<span data-ttu-id="38e94-135">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="38e94-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="38e94-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="38e94-136">-EdgeEnabled</span></span>
<span data-ttu-id="38e94-137">Пометка, указывающая на то, что граница включается.</span><span class="sxs-lookup"><span data-stu-id="38e94-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="38e94-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="38e94-138">-EndorsementKey</span></span>
<span data-ttu-id="38e94-139">Ключ подтверждения TPM для устройства TPM.</span><span class="sxs-lookup"><span data-stu-id="38e94-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="38e94-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="38e94-140">-IotHub</span></span>
<span data-ttu-id="38e94-141">Host name of target IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="38e94-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="38e94-142">Используйте список с разделами между пробелами для нескольких концентраторов IoT.</span><span class="sxs-lookup"><span data-stu-id="38e94-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="38e94-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="38e94-143">-IotHubHostName</span></span>
<span data-ttu-id="38e94-144">Имя целевого концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="38e94-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="38e94-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="38e94-145">-PrimaryCAName</span></span>
<span data-ttu-id="38e94-146">Имя основного корневого сертификата ЦС.</span><span class="sxs-lookup"><span data-stu-id="38e94-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="38e94-147">Если при проверке необходимо использовать корневой сертификат ЦС, необходимо у назвать корневой ЦС.</span><span class="sxs-lookup"><span data-stu-id="38e94-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="38e94-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="38e94-148">-PrimaryCertificate</span></span>
<span data-ttu-id="38e94-149">Путь к файлу, содержащего основной сертификат.</span><span class="sxs-lookup"><span data-stu-id="38e94-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="38e94-150">Представление файла сертификата X509 (cer) или пути к PEM-файлу (Base-64).</span><span class="sxs-lookup"><span data-stu-id="38e94-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="38e94-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="38e94-151">-PrimaryKey</span></span>
<span data-ttu-id="38e94-152">Первичный симметричный ключ общего доступа, сохраненный в формате base64.</span><span class="sxs-lookup"><span data-stu-id="38e94-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="38e94-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="38e94-153">-ProvisioningStatus</span></span>
<span data-ttu-id="38e94-154">Включить или отключить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="38e94-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="38e94-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="38e94-155">-RegistrationId</span></span>
<span data-ttu-id="38e94-156">Индивидуальный регистрационный номер.</span><span class="sxs-lookup"><span data-stu-id="38e94-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="38e94-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="38e94-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="38e94-158">Данные устройств, обрабатываемые при повторной под подготовка к другому центру IOT.</span><span class="sxs-lookup"><span data-stu-id="38e94-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="38e94-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38e94-159">-ResourceGroupName</span></span>
<span data-ttu-id="38e94-160">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="38e94-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="38e94-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38e94-161">-ResourceId</span></span>
<span data-ttu-id="38e94-162">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="38e94-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="38e94-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="38e94-163">-RootCertificate</span></span>
<span data-ttu-id="38e94-164">Позволяет создавать проверки X509attestation с использованием корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="38e94-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="38e94-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="38e94-165">-SecondaryCAName</span></span>
<span data-ttu-id="38e94-166">Имя сертификата дополнительного корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="38e94-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="38e94-167">Если при проверке необходимо использовать корневой сертификат ЦС, необходимо у назвать корневой ЦС.</span><span class="sxs-lookup"><span data-stu-id="38e94-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="38e94-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="38e94-168">-SecondaryCertificate</span></span>
<span data-ttu-id="38e94-169">Путь к файлу, содержащего дополнительный сертификат.</span><span class="sxs-lookup"><span data-stu-id="38e94-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="38e94-170">Представление файла сертификата X509 (cer) или пути к PEM-файлу (Base-64).</span><span class="sxs-lookup"><span data-stu-id="38e94-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="38e94-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="38e94-171">-SecondaryKey</span></span>
<span data-ttu-id="38e94-172">Дополнительный симметричный ключ общего доступа, сохраненный в формате base64.</span><span class="sxs-lookup"><span data-stu-id="38e94-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="38e94-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="38e94-173">-StorageRootKey</span></span>
<span data-ttu-id="38e94-174">Корневой ключ хранилища TPM для устройства TPM.</span><span class="sxs-lookup"><span data-stu-id="38e94-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="38e94-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="38e94-175">-Tag</span></span>
<span data-ttu-id="38e94-176">Первичные теги.</span><span class="sxs-lookup"><span data-stu-id="38e94-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="38e94-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="38e94-177">-WebhookUrl</span></span>
<span data-ttu-id="38e94-178">URL-адрес веб-сайта, используемый для пользовательских запросов на выделение ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38e94-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="38e94-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38e94-179">-Confirm</span></span>
<span data-ttu-id="38e94-180">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38e94-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38e94-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38e94-181">-WhatIf</span></span>
<span data-ttu-id="38e94-182">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38e94-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38e94-183">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="38e94-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38e94-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38e94-184">CommonParameters</span></span>
<span data-ttu-id="38e94-185">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38e94-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38e94-186">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38e94-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38e94-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38e94-187">INPUTS</span></span>

### <span data-ttu-id="38e94-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="38e94-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="38e94-189">System.String</span><span class="sxs-lookup"><span data-stu-id="38e94-189">System.String</span></span>

## <span data-ttu-id="38e94-190">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="38e94-190">OUTPUTS</span></span>

### <span data-ttu-id="38e94-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="38e94-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="38e94-192">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="38e94-192">NOTES</span></span>

## <span data-ttu-id="38e94-193">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38e94-193">RELATED LINKS</span></span>
