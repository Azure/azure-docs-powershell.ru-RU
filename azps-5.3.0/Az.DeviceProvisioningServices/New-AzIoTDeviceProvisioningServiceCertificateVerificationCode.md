---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506315"
---
# <span data-ttu-id="0bc03-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="0bc03-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="0bc03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bc03-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc03-103">Создать код проверки для сертификата службы регистрации устройства на узл-узл Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="0bc03-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="0bc03-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0bc03-104">SYNTAX</span></span>

### <span data-ttu-id="0bc03-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0bc03-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bc03-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0bc03-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bc03-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0bc03-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bc03-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bc03-108">DESCRIPTION</span></span>
<span data-ttu-id="0bc03-109">Этот код проверки используется для завершения процедуры подтверждения сертификата.</span><span class="sxs-lookup"><span data-stu-id="0bc03-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="0bc03-110">Используйте этот код проверки в качестве CN нового сертификата, подписанного с закрытым ключом корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="0bc03-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="0bc03-111">Подробное описание сертификатов ЦС в службе azure IoT Hub Device Provisioning Service см. в https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="0bc03-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="0bc03-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0bc03-112">EXAMPLES</span></span>

### <span data-ttu-id="0bc03-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0bc03-113">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="0bc03-114">Создание кода проверки для mycertificate.</span><span class="sxs-lookup"><span data-stu-id="0bc03-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="0bc03-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0bc03-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzIoTDpsCVC

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="0bc03-116">Создание проверочных кодов для mycertificate с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="0bc03-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="0bc03-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bc03-117">PARAMETERS</span></span>

### <span data-ttu-id="0bc03-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="0bc03-118">-CertificateName</span></span>
<span data-ttu-id="0bc03-119">Имя сертификата службы регистрации устройства IOT</span><span class="sxs-lookup"><span data-stu-id="0bc03-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="0bc03-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc03-120">-DefaultProfile</span></span>
<span data-ttu-id="0bc03-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0bc03-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bc03-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="0bc03-122">-Etag</span></span>
<span data-ttu-id="0bc03-123">Etag of the Certificate</span><span class="sxs-lookup"><span data-stu-id="0bc03-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="0bc03-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bc03-124">-InputObject</span></span>
<span data-ttu-id="0bc03-125">Объект сертификата службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="0bc03-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="0bc03-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0bc03-126">-Name</span></span>
<span data-ttu-id="0bc03-127">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="0bc03-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0bc03-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bc03-128">-ResourceGroupName</span></span>
<span data-ttu-id="0bc03-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0bc03-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0bc03-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bc03-130">-ResourceId</span></span>
<span data-ttu-id="0bc03-131">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="0bc03-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="0bc03-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0bc03-132">-Confirm</span></span>
<span data-ttu-id="0bc03-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0bc03-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bc03-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bc03-134">-WhatIf</span></span>
<span data-ttu-id="0bc03-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bc03-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bc03-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0bc03-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bc03-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc03-137">CommonParameters</span></span>
<span data-ttu-id="0bc03-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bc03-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc03-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bc03-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc03-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0bc03-140">INPUTS</span></span>

### <span data-ttu-id="0bc03-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="0bc03-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="0bc03-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0bc03-142">System.String</span></span>

## <span data-ttu-id="0bc03-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0bc03-143">OUTPUTS</span></span>

### <span data-ttu-id="0bc03-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="0bc03-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="0bc03-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0bc03-145">NOTES</span></span>

## <span data-ttu-id="0bc03-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0bc03-146">RELATED LINKS</span></span>
