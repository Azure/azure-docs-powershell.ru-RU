---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 7bf897cdb3a3967a94dcb932859bad24f496c441
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730921"
---
# <span data-ttu-id="cb89b-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="cb89b-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="cb89b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb89b-102">SYNOPSIS</span></span>
<span data-ttu-id="cb89b-103">Создайте проверочный код для сертификата службы подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="cb89b-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="cb89b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb89b-104">SYNTAX</span></span>

### <span data-ttu-id="cb89b-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb89b-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb89b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cb89b-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb89b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cb89b-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb89b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb89b-108">DESCRIPTION</span></span>
<span data-ttu-id="cb89b-109">Этот проверочный код используется для завершения этапа проверки подлинности для сертификата.</span><span class="sxs-lookup"><span data-stu-id="cb89b-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="cb89b-110">Используйте этот проверочный код в качестве CN нового сертификата, подписанного закрытым ключом корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cb89b-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="cb89b-111">Подробное описание сертификатов ЦС в службе подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="cb89b-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="cb89b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb89b-112">EXAMPLES</span></span>

### <span data-ttu-id="cb89b-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb89b-113">Example 1</span></span>
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

<span data-ttu-id="cb89b-114">Создайте проверочный код для "mycertificate".</span><span class="sxs-lookup"><span data-stu-id="cb89b-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="cb89b-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cb89b-115">Example 2</span></span>
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

<span data-ttu-id="cb89b-116">Создайте проверочный код для "mycertificate" с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="cb89b-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="cb89b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb89b-117">PARAMETERS</span></span>

### <span data-ttu-id="cb89b-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="cb89b-118">-CertificateName</span></span>
<span data-ttu-id="cb89b-119">Имя сертификата службы подготовки устройства IOT</span><span class="sxs-lookup"><span data-stu-id="cb89b-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="cb89b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb89b-120">-DefaultProfile</span></span>
<span data-ttu-id="cb89b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb89b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb89b-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="cb89b-122">-Etag</span></span>
<span data-ttu-id="cb89b-123">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="cb89b-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="cb89b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb89b-124">-InputObject</span></span>
<span data-ttu-id="cb89b-125">Объект сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="cb89b-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="cb89b-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb89b-126">-Name</span></span>
<span data-ttu-id="cb89b-127">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="cb89b-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="cb89b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb89b-128">-ResourceGroupName</span></span>
<span data-ttu-id="cb89b-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cb89b-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cb89b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb89b-130">-ResourceId</span></span>
<span data-ttu-id="cb89b-131">Идентификатор ресурса сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="cb89b-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="cb89b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb89b-132">-Confirm</span></span>
<span data-ttu-id="cb89b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb89b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb89b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb89b-134">-WhatIf</span></span>
<span data-ttu-id="cb89b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb89b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb89b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb89b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb89b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb89b-137">CommonParameters</span></span>
<span data-ttu-id="cb89b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb89b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb89b-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb89b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb89b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb89b-140">INPUTS</span></span>

### <span data-ttu-id="cb89b-141">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="cb89b-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="cb89b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cb89b-142">System.String</span></span>

## <span data-ttu-id="cb89b-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb89b-143">OUTPUTS</span></span>

### <span data-ttu-id="cb89b-144">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="cb89b-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="cb89b-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb89b-145">NOTES</span></span>

## <span data-ttu-id="cb89b-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb89b-146">RELATED LINKS</span></span>
