---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: d4dcf52a3a705042f994c8106bd931a8b704a049
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398436"
---
# <span data-ttu-id="8d477-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="8d477-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="8d477-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d477-102">SYNOPSIS</span></span>
<span data-ttu-id="8d477-103">Создание и обновление сертификата службы регистрации устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="8d477-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="8d477-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d477-104">SYNTAX</span></span>

### <span data-ttu-id="8d477-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d477-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d477-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8d477-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d477-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8d477-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d477-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d477-108">DESCRIPTION</span></span>
<span data-ttu-id="8d477-109">Отправка нового сертификата или замена существующего сертификата таким же именем.</span><span class="sxs-lookup"><span data-stu-id="8d477-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="8d477-110">Подробное описание сертификатов ЦС в службе azure IoT Hub Device Provisioning Service см. в https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="8d477-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="8d477-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d477-111">EXAMPLES</span></span>

### <span data-ttu-id="8d477-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8d477-112">Example 1</span></span>
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

<span data-ttu-id="8d477-113">Отправка файла CER сертификата ЦС в службу регистрации устройства в Центре IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="8d477-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="8d477-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8d477-114">Example 2</span></span>
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

<span data-ttu-id="8d477-115">Обновляет сертификат ЦС в центральной службе по подготовка устройств ioT путем отправки нового файла CER.</span><span class="sxs-lookup"><span data-stu-id="8d477-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="8d477-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d477-116">PARAMETERS</span></span>

### <span data-ttu-id="8d477-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="8d477-117">-CertificateName</span></span>
<span data-ttu-id="8d477-118">Имя сертификата службы регистрации устройства IOT</span><span class="sxs-lookup"><span data-stu-id="8d477-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="8d477-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d477-119">-DefaultProfile</span></span>
<span data-ttu-id="8d477-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d477-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d477-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="8d477-121">-Etag</span></span>
<span data-ttu-id="8d477-122">Etag of the Certificate</span><span class="sxs-lookup"><span data-stu-id="8d477-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="8d477-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d477-123">-InputObject</span></span>
<span data-ttu-id="8d477-124">Объект сертификата службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="8d477-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="8d477-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8d477-125">-Name</span></span>
<span data-ttu-id="8d477-126">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="8d477-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8d477-127">-Path</span><span class="sxs-lookup"><span data-stu-id="8d477-127">-Path</span></span>
<span data-ttu-id="8d477-128">Представление файла сертификата X509 (cer) или пути к PEM-файлу (base-64)</span><span class="sxs-lookup"><span data-stu-id="8d477-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="8d477-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d477-129">-ResourceGroupName</span></span>
<span data-ttu-id="8d477-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8d477-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8d477-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d477-131">-ResourceId</span></span>
<span data-ttu-id="8d477-132">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="8d477-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="8d477-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d477-133">-Confirm</span></span>
<span data-ttu-id="8d477-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d477-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d477-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d477-135">-WhatIf</span></span>
<span data-ttu-id="8d477-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d477-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d477-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8d477-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d477-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d477-138">CommonParameters</span></span>
<span data-ttu-id="8d477-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d477-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d477-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d477-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d477-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d477-141">INPUTS</span></span>

### <span data-ttu-id="8d477-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="8d477-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="8d477-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8d477-143">System.String</span></span>

## <span data-ttu-id="8d477-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d477-144">OUTPUTS</span></span>

### <span data-ttu-id="8d477-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="8d477-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="8d477-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d477-146">NOTES</span></span>

## <span data-ttu-id="8d477-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d477-147">RELATED LINKS</span></span>
