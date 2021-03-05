---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 4087cb324f55d6445458fce2a8b79f5c39308b69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985085"
---
# <span data-ttu-id="9da2d-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="9da2d-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="9da2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9da2d-102">SYNOPSIS</span></span>
<span data-ttu-id="9da2d-103">Обновив запись регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="9da2d-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="9da2d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9da2d-104">SYNTAX</span></span>

### <span data-ttu-id="9da2d-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9da2d-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9da2d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9da2d-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9da2d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9da2d-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9da2d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9da2d-108">DESCRIPTION</span></span>
<span data-ttu-id="9da2d-109">Обновив регистрацию устройства в службе регистрации устройств на концентраторе Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="9da2d-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="9da2d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9da2d-110">EXAMPLES</span></span>

### <span data-ttu-id="9da2d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9da2d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="9da2d-112">Обновив политику выделения и концентраторы для записи о регистрации.</span><span class="sxs-lookup"><span data-stu-id="9da2d-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="9da2d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9da2d-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="9da2d-114">Обновив начальное состояние регистрации.</span><span class="sxs-lookup"><span data-stu-id="9da2d-114">Update an enrollment's initial twin state.</span></span>

### <span data-ttu-id="9da2d-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9da2d-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -PrimaryCertificate ".\primaryCertificate.cer" -SecondaryCertificate ".\secondaryCertificate.cer"
```

<span data-ttu-id="9da2d-116">Обновление основных и дополнительных сертификатов симметричного ключа</span><span class="sxs-lookup"><span data-stu-id="9da2d-116">Update a symmetric key enrollment's primary and secondary certificates</span></span>

## <span data-ttu-id="9da2d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9da2d-117">PARAMETERS</span></span>

### <span data-ttu-id="9da2d-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="9da2d-118">-AllocationPolicy</span></span>
<span data-ttu-id="9da2d-119">Тип выделения для устройства, назначенного Центру.</span><span class="sxs-lookup"><span data-stu-id="9da2d-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="9da2d-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9da2d-120">-ApiVersion</span></span>
<span data-ttu-id="9da2d-121">Версия API службы подготовка в настраиваемом запросе на выделение.</span><span class="sxs-lookup"><span data-stu-id="9da2d-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="9da2d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da2d-122">-DefaultProfile</span></span>
<span data-ttu-id="9da2d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9da2d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9da2d-124">-Desired</span><span class="sxs-lookup"><span data-stu-id="9da2d-124">-Desired</span></span>
<span data-ttu-id="9da2d-125">Начальное желаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9da2d-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="9da2d-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9da2d-126">-DeviceId</span></span>
<span data-ttu-id="9da2d-127">IoT Hub Device IoT IoT Device IoT IoT Hub IOT.</span><span class="sxs-lookup"><span data-stu-id="9da2d-127">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="9da2d-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="9da2d-128">-DpsName</span></span>
<span data-ttu-id="9da2d-129">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="9da2d-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9da2d-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="9da2d-130">-DpsObject</span></span>
<span data-ttu-id="9da2d-131">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="9da2d-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9da2d-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9da2d-132">-EdgeEnabled</span></span>
<span data-ttu-id="9da2d-133">Пометка, указывающая на то, что граница включается.</span><span class="sxs-lookup"><span data-stu-id="9da2d-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="9da2d-134">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="9da2d-134">-EndorsementKey</span></span>
<span data-ttu-id="9da2d-135">Ключ подтверждения TPM для устройства TPM.</span><span class="sxs-lookup"><span data-stu-id="9da2d-135">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="9da2d-136">-IotHub</span><span class="sxs-lookup"><span data-stu-id="9da2d-136">-IotHub</span></span>
<span data-ttu-id="9da2d-137">Host name of target IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="9da2d-137">Host name of target IoT Hub.</span></span>
<span data-ttu-id="9da2d-138">Используйте список с разделами между пробелами для нескольких концентраторов IoT.</span><span class="sxs-lookup"><span data-stu-id="9da2d-138">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="9da2d-139">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="9da2d-139">-IotHubHostName</span></span>
<span data-ttu-id="9da2d-140">Имя целевого концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="9da2d-140">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="9da2d-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="9da2d-141">-PrimaryCAName</span></span>
<span data-ttu-id="9da2d-142">Имя основного корневого сертификата ЦС.</span><span class="sxs-lookup"><span data-stu-id="9da2d-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="9da2d-143">Если при проверке необходимо использовать корневой сертификат ЦС, необходимо у назвать корневой ЦС.</span><span class="sxs-lookup"><span data-stu-id="9da2d-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="9da2d-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="9da2d-144">-PrimaryCertificate</span></span>
<span data-ttu-id="9da2d-145">Путь к файлу, содержащего основной сертификат.</span><span class="sxs-lookup"><span data-stu-id="9da2d-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="9da2d-146">Представление файла сертификата X509 (CER- или PEM-файла) base-64.</span><span class="sxs-lookup"><span data-stu-id="9da2d-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="9da2d-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9da2d-147">-PrimaryKey</span></span>
<span data-ttu-id="9da2d-148">Первичный симметричный ключ общего доступа, сохраненный в формате base64.</span><span class="sxs-lookup"><span data-stu-id="9da2d-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="9da2d-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="9da2d-149">-ProvisioningStatus</span></span>
<span data-ttu-id="9da2d-150">Включить или отключить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="9da2d-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="9da2d-151">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="9da2d-151">-RegistrationId</span></span>
<span data-ttu-id="9da2d-152">Индивидуальный регистрационный номер.</span><span class="sxs-lookup"><span data-stu-id="9da2d-152">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="9da2d-153">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="9da2d-153">-ReprovisionPolicy</span></span>
<span data-ttu-id="9da2d-154">Данные устройств, обрабатываемые при повторной под подготовка к другому центру IOT.</span><span class="sxs-lookup"><span data-stu-id="9da2d-154">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="9da2d-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da2d-155">-ResourceGroupName</span></span>
<span data-ttu-id="9da2d-156">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9da2d-156">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9da2d-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9da2d-157">-ResourceId</span></span>
<span data-ttu-id="9da2d-158">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="9da2d-158">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9da2d-159">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="9da2d-159">-RootCertificate</span></span>
<span data-ttu-id="9da2d-160">Переключение на обновление проверки X509attestation с помощью корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="9da2d-160">Switch to update X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="9da2d-161">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="9da2d-161">-SecondaryCAName</span></span>
<span data-ttu-id="9da2d-162">Имя сертификата дополнительного корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="9da2d-162">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="9da2d-163">Если при проверке необходимо использовать корневой сертификат ЦС, необходимо у назвать корневой ЦС.</span><span class="sxs-lookup"><span data-stu-id="9da2d-163">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="9da2d-164">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="9da2d-164">-SecondaryCertificate</span></span>
<span data-ttu-id="9da2d-165">Путь к файлу, содержащего дополнительный сертификат.</span><span class="sxs-lookup"><span data-stu-id="9da2d-165">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="9da2d-166">Представление файла сертификата X509 (CER- или PEM-файла) base-64.</span><span class="sxs-lookup"><span data-stu-id="9da2d-166">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="9da2d-167">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="9da2d-167">-SecondaryKey</span></span>
<span data-ttu-id="9da2d-168">Дополнительный симметричный ключ общего доступа, сохраненный в формате base64.</span><span class="sxs-lookup"><span data-stu-id="9da2d-168">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="9da2d-169">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="9da2d-169">-StorageRootKey</span></span>
<span data-ttu-id="9da2d-170">Корневой ключ хранилища TPM для устройства TPM.</span><span class="sxs-lookup"><span data-stu-id="9da2d-170">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="9da2d-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="9da2d-171">-Tag</span></span>
<span data-ttu-id="9da2d-172">Первичные теги.</span><span class="sxs-lookup"><span data-stu-id="9da2d-172">Initial twin tags.</span></span>

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

### <span data-ttu-id="9da2d-173">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="9da2d-173">-WebhookUrl</span></span>
<span data-ttu-id="9da2d-174">URL-адрес веб-сайта, используемый для пользовательских запросов на выделение ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9da2d-174">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="9da2d-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9da2d-175">-Confirm</span></span>
<span data-ttu-id="9da2d-176">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9da2d-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9da2d-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9da2d-177">-WhatIf</span></span>
<span data-ttu-id="9da2d-178">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9da2d-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9da2d-179">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9da2d-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9da2d-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da2d-180">CommonParameters</span></span>
<span data-ttu-id="9da2d-181">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da2d-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da2d-182">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da2d-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da2d-183">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9da2d-183">INPUTS</span></span>

### <span data-ttu-id="9da2d-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9da2d-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="9da2d-185">System.String</span><span class="sxs-lookup"><span data-stu-id="9da2d-185">System.String</span></span>

## <span data-ttu-id="9da2d-186">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9da2d-186">OUTPUTS</span></span>

### <span data-ttu-id="9da2d-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="9da2d-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="9da2d-188">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9da2d-188">NOTES</span></span>

## <span data-ttu-id="9da2d-189">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9da2d-189">RELATED LINKS</span></span>
