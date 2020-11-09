---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7c5c2f747b5de24e1ccf3a4cf047930746c0d863
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245529"
---
# <span data-ttu-id="8fc30-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="8fc30-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="8fc30-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8fc30-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc30-103">Создание группы регистрации устройств.</span><span class="sxs-lookup"><span data-stu-id="8fc30-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="8fc30-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8fc30-104">SYNTAX</span></span>

### <span data-ttu-id="8fc30-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8fc30-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc30-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8fc30-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc30-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8fc30-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fc30-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fc30-108">DESCRIPTION</span></span>
<span data-ttu-id="8fc30-109">Создайте группу регистрации в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="8fc30-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="8fc30-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8fc30-110">EXAMPLES</span></span>

### <span data-ttu-id="8fc30-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8fc30-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="8fc30-112">Создание регистрации с типом аттестации SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="8fc30-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="8fc30-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8fc30-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="8fc30-114">Создание регистрации с типом аттестации X509</span><span class="sxs-lookup"><span data-stu-id="8fc30-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="8fc30-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8fc30-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="8fc30-116">Создайте регистрацию с типом подтверждения SymmetricKey и начальным состоянием двойной.</span><span class="sxs-lookup"><span data-stu-id="8fc30-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="8fc30-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8fc30-117">PARAMETERS</span></span>

### <span data-ttu-id="8fc30-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="8fc30-118">-AllocationPolicy</span></span>
<span data-ttu-id="8fc30-119">Тип выделения для устройства, назначенного концентратору.</span><span class="sxs-lookup"><span data-stu-id="8fc30-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="8fc30-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8fc30-120">-ApiVersion</span></span>
<span data-ttu-id="8fc30-121">Версия API службы подготовки в настраиваемом запросе на выделение.</span><span class="sxs-lookup"><span data-stu-id="8fc30-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="8fc30-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="8fc30-122">-AttestationType</span></span>
<span data-ttu-id="8fc30-123">Механизм аттестации.</span><span class="sxs-lookup"><span data-stu-id="8fc30-123">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="8fc30-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc30-124">-DefaultProfile</span></span>
<span data-ttu-id="8fc30-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8fc30-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fc30-126">-Необходимый</span><span class="sxs-lookup"><span data-stu-id="8fc30-126">-Desired</span></span>
<span data-ttu-id="8fc30-127">Начальные двойной нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="8fc30-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="8fc30-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="8fc30-128">-DpsName</span></span>
<span data-ttu-id="8fc30-129">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="8fc30-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8fc30-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="8fc30-130">-DpsObject</span></span>
<span data-ttu-id="8fc30-131">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="8fc30-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="8fc30-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="8fc30-132">-EdgeEnabled</span></span>
<span data-ttu-id="8fc30-133">Флаг, указывающий на включение Edge.</span><span class="sxs-lookup"><span data-stu-id="8fc30-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="8fc30-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="8fc30-134">-IotHub</span></span>
<span data-ttu-id="8fc30-135">Имя узла целевого центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="8fc30-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="8fc30-136">Использование списка с разделителями-запятыми в нескольких центрах Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="8fc30-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="8fc30-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="8fc30-137">-IotHubHostName</span></span>
<span data-ttu-id="8fc30-138">Имя узла целевого центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="8fc30-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="8fc30-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8fc30-139">-Name</span></span>
<span data-ttu-id="8fc30-140">Имя группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="8fc30-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="8fc30-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="8fc30-141">-PrimaryCAName</span></span>
<span data-ttu-id="8fc30-142">Имя сертификата основного корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="8fc30-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="8fc30-143">Если требуется подтверждение с сертификатом корневого ЦС, необходимо указать имя корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="8fc30-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="8fc30-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="8fc30-144">-PrimaryCertificate</span></span>
<span data-ttu-id="8fc30-145">Путь к файлу, содержащему основной сертификат.</span><span class="sxs-lookup"><span data-stu-id="8fc30-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="8fc30-146">Base-64. путь к файлу, который является файлом сертификата X509. cer или. PEM.</span><span class="sxs-lookup"><span data-stu-id="8fc30-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="8fc30-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="8fc30-147">-PrimaryKey</span></span>
<span data-ttu-id="8fc30-148">Основной симметричный ключ доступа, хранящийся в формате Base64.</span><span class="sxs-lookup"><span data-stu-id="8fc30-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="8fc30-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="8fc30-149">-ProvisioningStatus</span></span>
<span data-ttu-id="8fc30-150">Включите или отключите регистрационную запись.</span><span class="sxs-lookup"><span data-stu-id="8fc30-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="8fc30-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="8fc30-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="8fc30-152">Данные устройства, которые должны быть обработаны при повторной подготовке к разным центрам Интернет вещей.</span><span class="sxs-lookup"><span data-stu-id="8fc30-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="8fc30-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc30-153">-ResourceGroupName</span></span>
<span data-ttu-id="8fc30-154">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8fc30-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8fc30-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fc30-155">-ResourceId</span></span>
<span data-ttu-id="8fc30-156">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="8fc30-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="8fc30-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="8fc30-157">-RootCertificate</span></span>
<span data-ttu-id="8fc30-158">Позволяет создавать X509attestation с помощью корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="8fc30-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="8fc30-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="8fc30-159">-SecondaryCAName</span></span>
<span data-ttu-id="8fc30-160">Имя сертификата вторичного корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="8fc30-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="8fc30-161">Если требуется подтверждение с сертификатом корневого ЦС, необходимо указать имя корневого ЦС.</span><span class="sxs-lookup"><span data-stu-id="8fc30-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="8fc30-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="8fc30-162">-SecondaryCertificate</span></span>
<span data-ttu-id="8fc30-163">Путь к файлу, содержащему дополнительный сертификат.</span><span class="sxs-lookup"><span data-stu-id="8fc30-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="8fc30-164">Base-64. путь к файлу, который является файлом сертификата X509. cer или. PEM.</span><span class="sxs-lookup"><span data-stu-id="8fc30-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="8fc30-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="8fc30-165">-SecondaryKey</span></span>
<span data-ttu-id="8fc30-166">Вторичный симметричный ключ доступа, хранящийся в формате Base64.</span><span class="sxs-lookup"><span data-stu-id="8fc30-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="8fc30-167">-Тег</span><span class="sxs-lookup"><span data-stu-id="8fc30-167">-Tag</span></span>
<span data-ttu-id="8fc30-168">Начальные Теги двойной.</span><span class="sxs-lookup"><span data-stu-id="8fc30-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="8fc30-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="8fc30-169">-WebhookUrl</span></span>
<span data-ttu-id="8fc30-170">URL-адрес веб-перехватчика, используемый для настраиваемых запросов на выделение.</span><span class="sxs-lookup"><span data-stu-id="8fc30-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="8fc30-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fc30-171">-Confirm</span></span>
<span data-ttu-id="8fc30-172">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8fc30-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fc30-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc30-173">-WhatIf</span></span>
<span data-ttu-id="8fc30-174">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8fc30-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fc30-175">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8fc30-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fc30-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc30-176">CommonParameters</span></span>
<span data-ttu-id="8fc30-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8fc30-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc30-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fc30-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc30-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8fc30-179">INPUTS</span></span>

### <span data-ttu-id="8fc30-180">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8fc30-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="8fc30-181">System. String</span><span class="sxs-lookup"><span data-stu-id="8fc30-181">System.String</span></span>

## <span data-ttu-id="8fc30-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fc30-182">OUTPUTS</span></span>

### <span data-ttu-id="8fc30-183">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="8fc30-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="8fc30-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="8fc30-184">NOTES</span></span>

## <span data-ttu-id="8fc30-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8fc30-185">RELATED LINKS</span></span>