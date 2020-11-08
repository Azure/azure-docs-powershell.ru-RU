---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: e02d9c1ca9a5d45f081f168c3d8736d502f52094
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236726"
---
# <span data-ttu-id="79c5c-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="79c5c-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="79c5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="79c5c-103">Создание записи регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="79c5c-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="79c5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79c5c-104">SYNTAX</span></span>

### <span data-ttu-id="79c5c-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79c5c-105">ResourceSet (Default)</span></span>
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

### <span data-ttu-id="79c5c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="79c5c-106">InputObjectSet</span></span>
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

### <span data-ttu-id="79c5c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="79c5c-107">ResourceIdSet</span></span>
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

## <span data-ttu-id="79c5c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79c5c-108">DESCRIPTION</span></span>
<span data-ttu-id="79c5c-109">Создание регистрации устройства в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="79c5c-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="79c5c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79c5c-110">EXAMPLES</span></span>

### <span data-ttu-id="79c5c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="79c5c-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="79c5c-112">Создание регистрации с типом аттестации SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="79c5c-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="79c5c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="79c5c-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="79c5c-114">Создайте регистрацию с помощью аттестации доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="79c5c-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="79c5c-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="79c5c-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="79c5c-116">Создание регистрации с типом аттестации X509</span><span class="sxs-lookup"><span data-stu-id="79c5c-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="79c5c-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="79c5c-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="79c5c-118">Создайте регистрацию с типом подтверждения SymmetricKey и начальным состоянием двойной.</span><span class="sxs-lookup"><span data-stu-id="79c5c-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="79c5c-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79c5c-119">PARAMETERS</span></span>

### <span data-ttu-id="79c5c-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="79c5c-120">-AllocationPolicy</span></span>
<span data-ttu-id="79c5c-121">Тип выделения для устройства, назначенного концентратору.</span><span class="sxs-lookup"><span data-stu-id="79c5c-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="79c5c-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="79c5c-122">-ApiVersion</span></span>
<span data-ttu-id="79c5c-123">Версия API службы подготовки в настраиваемом запросе на выделение.</span><span class="sxs-lookup"><span data-stu-id="79c5c-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="79c5c-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="79c5c-124">-AttestationType</span></span>
<span data-ttu-id="79c5c-125">Механизм аттестации.</span><span class="sxs-lookup"><span data-stu-id="79c5c-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="79c5c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c5c-126">-DefaultProfile</span></span>
<span data-ttu-id="79c5c-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79c5c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79c5c-128">-Необходимый</span><span class="sxs-lookup"><span data-stu-id="79c5c-128">-Desired</span></span>
<span data-ttu-id="79c5c-129">Начальные двойной нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="79c5c-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="79c5c-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="79c5c-130">-DeviceId</span></span>
<span data-ttu-id="79c5c-131">ИДЕНТИФИКАТОР устройства центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="79c5c-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="79c5c-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="79c5c-132">-DpsName</span></span>
<span data-ttu-id="79c5c-133">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="79c5c-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="79c5c-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="79c5c-134">-DpsObject</span></span>
<span data-ttu-id="79c5c-135">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="79c5c-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="79c5c-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="79c5c-136">-EdgeEnabled</span></span>
<span data-ttu-id="79c5c-137">Флаг, указывающий на включение Edge.</span><span class="sxs-lookup"><span data-stu-id="79c5c-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="79c5c-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="79c5c-138">-EndorsementKey</span></span>
<span data-ttu-id="79c5c-139">Ключ подтверждения доверенного платформенного модуля для устройства доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="79c5c-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="79c5c-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="79c5c-140">-IotHub</span></span>
<span data-ttu-id="79c5c-141">Имя узла целевого центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="79c5c-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="79c5c-142">Использование списка с разделителями-запятыми в нескольких центрах Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="79c5c-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="79c5c-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="79c5c-143">-IotHubHostName</span></span>
<span data-ttu-id="79c5c-144">Имя узла целевого центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="79c5c-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="79c5c-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="79c5c-145">-PrimaryCAName</span></span>
<span data-ttu-id="79c5c-146">Имя сертификата основного корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="79c5c-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="79c5c-147">Если требуется подтверждение с сертификатом корневого ЦС, необходимо указать имя корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="79c5c-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="79c5c-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="79c5c-148">-PrimaryCertificate</span></span>
<span data-ttu-id="79c5c-149">Путь к файлу, содержащему основной сертификат.</span><span class="sxs-lookup"><span data-stu-id="79c5c-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="79c5c-150">Base-64. путь к файлу, который является файлом сертификата X509. cer или. PEM.</span><span class="sxs-lookup"><span data-stu-id="79c5c-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="79c5c-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="79c5c-151">-PrimaryKey</span></span>
<span data-ttu-id="79c5c-152">Основной симметричный ключ доступа, хранящийся в формате Base64.</span><span class="sxs-lookup"><span data-stu-id="79c5c-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="79c5c-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="79c5c-153">-ProvisioningStatus</span></span>
<span data-ttu-id="79c5c-154">Включите или отключите регистрационную запись.</span><span class="sxs-lookup"><span data-stu-id="79c5c-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="79c5c-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="79c5c-155">-RegistrationId</span></span>
<span data-ttu-id="79c5c-156">Регистрационный код отдельной регистрации.</span><span class="sxs-lookup"><span data-stu-id="79c5c-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="79c5c-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="79c5c-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="79c5c-158">Данные устройства, которые должны быть обработаны при повторной подготовке к разным центрам Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="79c5c-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="79c5c-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c5c-159">-ResourceGroupName</span></span>
<span data-ttu-id="79c5c-160">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="79c5c-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="79c5c-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79c5c-161">-ResourceId</span></span>
<span data-ttu-id="79c5c-162">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="79c5c-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="79c5c-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="79c5c-163">-RootCertificate</span></span>
<span data-ttu-id="79c5c-164">Позволяет создавать X509attestation с помощью корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="79c5c-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="79c5c-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="79c5c-165">-SecondaryCAName</span></span>
<span data-ttu-id="79c5c-166">Имя сертификата вторичного корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="79c5c-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="79c5c-167">Если требуется подтверждение с сертификатом корневого ЦС, необходимо указать имя корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="79c5c-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="79c5c-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="79c5c-168">-SecondaryCertificate</span></span>
<span data-ttu-id="79c5c-169">Путь к файлу, содержащему дополнительный сертификат.</span><span class="sxs-lookup"><span data-stu-id="79c5c-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="79c5c-170">Base-64. путь к файлу, который является файлом сертификата X509. cer или. PEM.</span><span class="sxs-lookup"><span data-stu-id="79c5c-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="79c5c-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="79c5c-171">-SecondaryKey</span></span>
<span data-ttu-id="79c5c-172">Вторичный симметричный ключ доступа, хранящийся в формате Base64.</span><span class="sxs-lookup"><span data-stu-id="79c5c-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="79c5c-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="79c5c-173">-StorageRootKey</span></span>
<span data-ttu-id="79c5c-174">Корневой ключ хранилища доверенного платформенного модуля для устройства доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="79c5c-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="79c5c-175">-Тег</span><span class="sxs-lookup"><span data-stu-id="79c5c-175">-Tag</span></span>
<span data-ttu-id="79c5c-176">Начальные Теги двойной.</span><span class="sxs-lookup"><span data-stu-id="79c5c-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="79c5c-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="79c5c-177">-WebhookUrl</span></span>
<span data-ttu-id="79c5c-178">URL-адрес веб-перехватчика, используемый для настраиваемых запросов на выделение.</span><span class="sxs-lookup"><span data-stu-id="79c5c-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="79c5c-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79c5c-179">-Confirm</span></span>
<span data-ttu-id="79c5c-180">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79c5c-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79c5c-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c5c-181">-WhatIf</span></span>
<span data-ttu-id="79c5c-182">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79c5c-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79c5c-183">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79c5c-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79c5c-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c5c-184">CommonParameters</span></span>
<span data-ttu-id="79c5c-185">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79c5c-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c5c-186">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c5c-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c5c-187">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79c5c-187">INPUTS</span></span>

### <span data-ttu-id="79c5c-188">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="79c5c-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="79c5c-189">System. String</span><span class="sxs-lookup"><span data-stu-id="79c5c-189">System.String</span></span>

## <span data-ttu-id="79c5c-190">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79c5c-190">OUTPUTS</span></span>

### <span data-ttu-id="79c5c-191">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="79c5c-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="79c5c-192">Пуск</span><span class="sxs-lookup"><span data-stu-id="79c5c-192">NOTES</span></span>

## <span data-ttu-id="79c5c-193">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79c5c-193">RELATED LINKS</span></span>
