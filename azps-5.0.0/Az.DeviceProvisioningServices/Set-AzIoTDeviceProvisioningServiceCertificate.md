---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 9b995a0ed80bf32b770fe6b157a283534d01f743
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245498"
---
# <span data-ttu-id="2a239-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="2a239-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="2a239-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a239-102">SYNOPSIS</span></span>
<span data-ttu-id="2a239-103">Проверьте наличие сертификата службы подготовки устройств центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="2a239-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="2a239-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a239-104">SYNTAX</span></span>

### <span data-ttu-id="2a239-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a239-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a239-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2a239-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a239-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2a239-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a239-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a239-108">DESCRIPTION</span></span>
<span data-ttu-id="2a239-109">Для проверки сертификата можно загрузить сертификат проверки, который содержит проверочный код, полученный путем вызова Generate-Verification-Code.</span><span class="sxs-lookup"><span data-stu-id="2a239-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="2a239-110">Это последний шаг в ходе проверки.</span><span class="sxs-lookup"><span data-stu-id="2a239-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="2a239-111">Подробное описание сертификатов ЦС в службе подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="2a239-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="2a239-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a239-112">EXAMPLES</span></span>

### <span data-ttu-id="2a239-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a239-113">Example 1</span></span>
```
PS C:\> Set-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="2a239-114">Подтвердить владение закрытым ключом "mycertificate".</span><span class="sxs-lookup"><span data-stu-id="2a239-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="2a239-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2a239-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | Set-AzIoTDpsCertificate -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="2a239-116">Подтвердить владение закрытым ключом "mycertificate" с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="2a239-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="2a239-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a239-117">PARAMETERS</span></span>

### <span data-ttu-id="2a239-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2a239-118">-CertificateName</span></span>
<span data-ttu-id="2a239-119">Имя сертификата службы подготовки устройства IOT</span><span class="sxs-lookup"><span data-stu-id="2a239-119">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a239-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a239-120">-DefaultProfile</span></span>
<span data-ttu-id="2a239-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a239-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a239-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="2a239-122">-Etag</span></span>
<span data-ttu-id="2a239-123">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="2a239-123">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a239-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a239-124">-InputObject</span></span>
<span data-ttu-id="2a239-125">Объект сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="2a239-125">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a239-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a239-126">-Name</span></span>
<span data-ttu-id="2a239-127">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="2a239-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2a239-128">-Path</span><span class="sxs-lookup"><span data-stu-id="2a239-128">-Path</span></span>
<span data-ttu-id="2a239-129">базовое представление 64 сертификата X509. cer или PEM-файла.</span><span class="sxs-lookup"><span data-stu-id="2a239-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a239-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a239-130">-ResourceGroupName</span></span>
<span data-ttu-id="2a239-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2a239-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2a239-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a239-132">-ResourceId</span></span>
<span data-ttu-id="2a239-133">Идентификатор ресурса сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="2a239-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="2a239-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a239-134">-Confirm</span></span>
<span data-ttu-id="2a239-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a239-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a239-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a239-136">-WhatIf</span></span>
<span data-ttu-id="2a239-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a239-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a239-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a239-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a239-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a239-139">CommonParameters</span></span>
<span data-ttu-id="2a239-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a239-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a239-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a239-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a239-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a239-142">INPUTS</span></span>

### <span data-ttu-id="2a239-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="2a239-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="2a239-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2a239-144">System.String</span></span>

## <span data-ttu-id="2a239-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a239-145">OUTPUTS</span></span>

### <span data-ttu-id="2a239-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="2a239-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="2a239-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a239-147">NOTES</span></span>

## <span data-ttu-id="2a239-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a239-148">RELATED LINKS</span></span>
