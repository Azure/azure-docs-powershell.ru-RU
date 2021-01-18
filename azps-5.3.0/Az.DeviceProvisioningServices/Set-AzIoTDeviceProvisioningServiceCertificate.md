---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 9b995a0ed80bf32b770fe6b157a283534d01f743
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506316"
---
# <span data-ttu-id="715f0-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="715f0-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="715f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="715f0-102">SYNOPSIS</span></span>
<span data-ttu-id="715f0-103">Проверка сертификата службы регистрации устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="715f0-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="715f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="715f0-104">SYNTAX</span></span>

### <span data-ttu-id="715f0-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="715f0-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="715f0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="715f0-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="715f0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="715f0-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="715f0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="715f0-108">DESCRIPTION</span></span>
<span data-ttu-id="715f0-109">Проверьте сертификат, загрузив сертификат проверки с кодом проверки, полученным с помощью звонка с кодом проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="715f0-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="715f0-110">Это последний шаг в процессе проверки связи.</span><span class="sxs-lookup"><span data-stu-id="715f0-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="715f0-111">Подробное описание сертификатов ЦС в службе azure IoT Hub Device Provisioning Service см. в https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="715f0-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="715f0-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="715f0-112">EXAMPLES</span></span>

### <span data-ttu-id="715f0-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="715f0-113">Example 1</span></span>
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

<span data-ttu-id="715f0-114">Проверьте право собственности на закрытый ключ mycertificate.</span><span class="sxs-lookup"><span data-stu-id="715f0-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="715f0-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="715f0-115">Example 2</span></span>
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

<span data-ttu-id="715f0-116">Проверьте право собственности на закрытый ключ mycertificate с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="715f0-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="715f0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="715f0-117">PARAMETERS</span></span>

### <span data-ttu-id="715f0-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="715f0-118">-CertificateName</span></span>
<span data-ttu-id="715f0-119">Имя сертификата службы регистрации IOT-устройства</span><span class="sxs-lookup"><span data-stu-id="715f0-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="715f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="715f0-120">-DefaultProfile</span></span>
<span data-ttu-id="715f0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="715f0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="715f0-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="715f0-122">-Etag</span></span>
<span data-ttu-id="715f0-123">Etag of the Certificate</span><span class="sxs-lookup"><span data-stu-id="715f0-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="715f0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="715f0-124">-InputObject</span></span>
<span data-ttu-id="715f0-125">Объект сертификата службы регистрации устройства IoT</span><span class="sxs-lookup"><span data-stu-id="715f0-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="715f0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="715f0-126">-Name</span></span>
<span data-ttu-id="715f0-127">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="715f0-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="715f0-128">-Path</span><span class="sxs-lookup"><span data-stu-id="715f0-128">-Path</span></span>
<span data-ttu-id="715f0-129">Представление файла сертификата X509 (cer) или пути к PEM-файлу (base-64)</span><span class="sxs-lookup"><span data-stu-id="715f0-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="715f0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="715f0-130">-ResourceGroupName</span></span>
<span data-ttu-id="715f0-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="715f0-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="715f0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="715f0-132">-ResourceId</span></span>
<span data-ttu-id="715f0-133">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="715f0-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="715f0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="715f0-134">-Confirm</span></span>
<span data-ttu-id="715f0-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="715f0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="715f0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="715f0-136">-WhatIf</span></span>
<span data-ttu-id="715f0-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="715f0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="715f0-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="715f0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="715f0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715f0-139">CommonParameters</span></span>
<span data-ttu-id="715f0-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="715f0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715f0-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="715f0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715f0-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="715f0-142">INPUTS</span></span>

### <span data-ttu-id="715f0-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="715f0-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="715f0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="715f0-144">System.String</span></span>

## <span data-ttu-id="715f0-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="715f0-145">OUTPUTS</span></span>

### <span data-ttu-id="715f0-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="715f0-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="715f0-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="715f0-147">NOTES</span></span>

## <span data-ttu-id="715f0-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="715f0-148">RELATED LINKS</span></span>
