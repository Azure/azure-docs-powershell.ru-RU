---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: b3c97abdee88615eedb2bb1f4452309326a4ebfa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426247"
---
# <span data-ttu-id="94b78-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="94b78-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="94b78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94b78-102">SYNOPSIS</span></span>
<span data-ttu-id="94b78-103">Создайте запись регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="94b78-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="94b78-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94b78-104">SYNTAX</span></span>

### <span data-ttu-id="94b78-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94b78-105">ResourceSet (Default)</span></span>
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

### <span data-ttu-id="94b78-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="94b78-106">InputObjectSet</span></span>
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

### <span data-ttu-id="94b78-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="94b78-107">ResourceIdSet</span></span>
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

## <span data-ttu-id="94b78-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94b78-108">DESCRIPTION</span></span>
<span data-ttu-id="94b78-109">Создайте регистрацию устройства в службе azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="94b78-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="94b78-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94b78-110">EXAMPLES</span></span>

### <span data-ttu-id="94b78-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94b78-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="94b78-112">Создание регистрации с типом attestation SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="94b78-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="94b78-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="94b78-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="94b78-114">Создайте регистрацию с помощью проверки TPM.</span><span class="sxs-lookup"><span data-stu-id="94b78-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="94b78-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="94b78-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="94b78-116">Создание регистрации с типом attestation X509</span><span class="sxs-lookup"><span data-stu-id="94b78-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="94b78-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="94b78-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="94b78-118">Создайте регистрацию с типом attestation SymmetricKey и первоначальным состоянием</span><span class="sxs-lookup"><span data-stu-id="94b78-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="94b78-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94b78-119">PARAMETERS</span></span>

### <span data-ttu-id="94b78-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="94b78-120">-AllocationPolicy</span></span>
<span data-ttu-id="94b78-121">Тип выделения для устройства, назначенного Центру.</span><span class="sxs-lookup"><span data-stu-id="94b78-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="94b78-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="94b78-122">-ApiVersion</span></span>
<span data-ttu-id="94b78-123">Версия API службы предварительной настройки в настраиваемом запросе на выделение.</span><span class="sxs-lookup"><span data-stu-id="94b78-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="94b78-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="94b78-124">-AttestationType</span></span>
<span data-ttu-id="94b78-125">Механизм проверки.</span><span class="sxs-lookup"><span data-stu-id="94b78-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="94b78-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b78-126">-DefaultProfile</span></span>
<span data-ttu-id="94b78-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94b78-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94b78-128">-Desired</span><span class="sxs-lookup"><span data-stu-id="94b78-128">-Desired</span></span>
<span data-ttu-id="94b78-129">Начальное желаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="94b78-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="94b78-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="94b78-130">-DeviceId</span></span>
<span data-ttu-id="94b78-131">IoT Hub Device IoT IOT Device IoT IoT.</span><span class="sxs-lookup"><span data-stu-id="94b78-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="94b78-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="94b78-132">-DpsName</span></span>
<span data-ttu-id="94b78-133">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="94b78-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="94b78-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="94b78-134">-DpsObject</span></span>
<span data-ttu-id="94b78-135">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="94b78-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="94b78-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="94b78-136">-EdgeEnabled</span></span>
<span data-ttu-id="94b78-137">Пометка, указывающая на то, что граница включается.</span><span class="sxs-lookup"><span data-stu-id="94b78-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="94b78-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="94b78-138">-EndorsementKey</span></span>
<span data-ttu-id="94b78-139">Ключ подтверждения TPM для устройства TPM.</span><span class="sxs-lookup"><span data-stu-id="94b78-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="94b78-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="94b78-140">-IotHub</span></span>
<span data-ttu-id="94b78-141">Host name of target IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="94b78-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="94b78-142">Используйте список с разделами между пробелами для нескольких концентраторов IoT.</span><span class="sxs-lookup"><span data-stu-id="94b78-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="94b78-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="94b78-143">-IotHubHostName</span></span>
<span data-ttu-id="94b78-144">Имя целевого концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="94b78-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="94b78-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="94b78-145">-PrimaryCAName</span></span>
<span data-ttu-id="94b78-146">Имя основного корневого сертификата ЦС.</span><span class="sxs-lookup"><span data-stu-id="94b78-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="94b78-147">Если при проверке необходимо использовать корневой сертификат ЦС, необходимо у назвать корневой ЦС.</span><span class="sxs-lookup"><span data-stu-id="94b78-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="94b78-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="94b78-148">-PrimaryCertificate</span></span>
<span data-ttu-id="94b78-149">Путь к файлу, содержащего основной сертификат.</span><span class="sxs-lookup"><span data-stu-id="94b78-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="94b78-150">Представление файла сертификата X509 (CER- или PEM-файла) base-64.</span><span class="sxs-lookup"><span data-stu-id="94b78-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="94b78-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="94b78-151">-PrimaryKey</span></span>
<span data-ttu-id="94b78-152">Первичный симметричный ключ общего доступа, сохраненный в базовом формате 64.</span><span class="sxs-lookup"><span data-stu-id="94b78-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="94b78-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="94b78-153">-ProvisioningStatus</span></span>
<span data-ttu-id="94b78-154">Включить или отключить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="94b78-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="94b78-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="94b78-155">-RegistrationId</span></span>
<span data-ttu-id="94b78-156">Индивидуальный регистрационный номер.</span><span class="sxs-lookup"><span data-stu-id="94b78-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="94b78-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="94b78-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="94b78-158">Данные устройств, обрабатываемые при повторной под подготовка к другому центру IOT.</span><span class="sxs-lookup"><span data-stu-id="94b78-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="94b78-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94b78-159">-ResourceGroupName</span></span>
<span data-ttu-id="94b78-160">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="94b78-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="94b78-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94b78-161">-ResourceId</span></span>
<span data-ttu-id="94b78-162">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="94b78-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="94b78-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="94b78-163">-RootCertificate</span></span>
<span data-ttu-id="94b78-164">Позволяет создавать проверку X509attestation с использованием корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="94b78-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="94b78-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="94b78-165">-SecondaryCAName</span></span>
<span data-ttu-id="94b78-166">Имя сертификата дополнительного корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="94b78-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="94b78-167">Если при проверке необходимо использовать корневой сертификат ЦС, необходимо у назвать корневой ЦС.</span><span class="sxs-lookup"><span data-stu-id="94b78-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="94b78-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="94b78-168">-SecondaryCertificate</span></span>
<span data-ttu-id="94b78-169">Путь к файлу, содержащего дополнительный сертификат.</span><span class="sxs-lookup"><span data-stu-id="94b78-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="94b78-170">Представление файла сертификата X509 (cer) или пути к PEM-файлу (Base-64).</span><span class="sxs-lookup"><span data-stu-id="94b78-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="94b78-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="94b78-171">-SecondaryKey</span></span>
<span data-ttu-id="94b78-172">Дополнительный симметричный ключ общего доступа, сохраненный в формате base64.</span><span class="sxs-lookup"><span data-stu-id="94b78-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="94b78-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="94b78-173">-StorageRootKey</span></span>
<span data-ttu-id="94b78-174">Корневой ключ хранилища TPM для устройства TPM.</span><span class="sxs-lookup"><span data-stu-id="94b78-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="94b78-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="94b78-175">-Tag</span></span>
<span data-ttu-id="94b78-176">Первичные теги.</span><span class="sxs-lookup"><span data-stu-id="94b78-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="94b78-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="94b78-177">-WebhookUrl</span></span>
<span data-ttu-id="94b78-178">URL-адрес веб-сайта, используемый для пользовательских запросов на выделение ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94b78-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="94b78-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94b78-179">-Confirm</span></span>
<span data-ttu-id="94b78-180">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="94b78-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94b78-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94b78-181">-WhatIf</span></span>
<span data-ttu-id="94b78-182">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94b78-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94b78-183">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94b78-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94b78-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b78-184">CommonParameters</span></span>
<span data-ttu-id="94b78-185">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94b78-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b78-186">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94b78-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b78-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94b78-187">INPUTS</span></span>

### <span data-ttu-id="94b78-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="94b78-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="94b78-189">System.String</span><span class="sxs-lookup"><span data-stu-id="94b78-189">System.String</span></span>

## <span data-ttu-id="94b78-190">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94b78-190">OUTPUTS</span></span>

### <span data-ttu-id="94b78-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="94b78-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="94b78-192">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94b78-192">NOTES</span></span>

## <span data-ttu-id="94b78-193">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94b78-193">RELATED LINKS</span></span>
