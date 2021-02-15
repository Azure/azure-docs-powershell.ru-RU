---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: d4dcf52a3a705042f994c8106bd931a8b704a049
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230492"
---
# <span data-ttu-id="b38dc-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="b38dc-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="b38dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b38dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b38dc-103">Создание и обновление сертификата службы регистрации устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="b38dc-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="b38dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b38dc-104">SYNTAX</span></span>

### <span data-ttu-id="b38dc-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b38dc-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b38dc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b38dc-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b38dc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b38dc-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b38dc-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b38dc-108">DESCRIPTION</span></span>
<span data-ttu-id="b38dc-109">Отправка нового сертификата или замена существующего сертификата таким же именем.</span><span class="sxs-lookup"><span data-stu-id="b38dc-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="b38dc-110">Подробное описание сертификатов ЦС в службе регистрации устройств на концентраторе IoT Azure см. в https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="b38dc-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="b38dc-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b38dc-111">EXAMPLES</span></span>

### <span data-ttu-id="b38dc-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b38dc-112">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="b38dc-113">Отправка файла CER сертификата ЦС в службу регистрации устройства в Центре IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="b38dc-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="b38dc-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b38dc-114">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="b38dc-115">Обновляет сертификат ЦС в центральной службе по подготовка устройств ioT путем отправки нового файла CER.</span><span class="sxs-lookup"><span data-stu-id="b38dc-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="b38dc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b38dc-116">PARAMETERS</span></span>

### <span data-ttu-id="b38dc-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b38dc-117">-CertificateName</span></span>
<span data-ttu-id="b38dc-118">Имя сертификата службы регистрации устройства IOT</span><span class="sxs-lookup"><span data-stu-id="b38dc-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="b38dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b38dc-119">-DefaultProfile</span></span>
<span data-ttu-id="b38dc-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b38dc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b38dc-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="b38dc-121">-Etag</span></span>
<span data-ttu-id="b38dc-122">Etag of the Certificate</span><span class="sxs-lookup"><span data-stu-id="b38dc-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="b38dc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b38dc-123">-InputObject</span></span>
<span data-ttu-id="b38dc-124">Объект сертификата службы регистрации устройства IoT</span><span class="sxs-lookup"><span data-stu-id="b38dc-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="b38dc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b38dc-125">-Name</span></span>
<span data-ttu-id="b38dc-126">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="b38dc-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b38dc-127">-Path</span><span class="sxs-lookup"><span data-stu-id="b38dc-127">-Path</span></span>
<span data-ttu-id="b38dc-128">Представление файла сертификата X509 (cer) или пути к PEM-файлу (base-64)</span><span class="sxs-lookup"><span data-stu-id="b38dc-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b38dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b38dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="b38dc-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b38dc-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b38dc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b38dc-131">-ResourceId</span></span>
<span data-ttu-id="b38dc-132">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="b38dc-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="b38dc-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b38dc-133">-Confirm</span></span>
<span data-ttu-id="b38dc-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b38dc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b38dc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b38dc-135">-WhatIf</span></span>
<span data-ttu-id="b38dc-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b38dc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b38dc-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b38dc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b38dc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b38dc-138">CommonParameters</span></span>
<span data-ttu-id="b38dc-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b38dc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b38dc-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b38dc-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b38dc-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b38dc-141">INPUTS</span></span>

### <span data-ttu-id="b38dc-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="b38dc-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="b38dc-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b38dc-143">System.String</span></span>

## <span data-ttu-id="b38dc-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b38dc-144">OUTPUTS</span></span>

### <span data-ttu-id="b38dc-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="b38dc-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="b38dc-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b38dc-146">NOTES</span></span>

## <span data-ttu-id="b38dc-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b38dc-147">RELATED LINKS</span></span>
