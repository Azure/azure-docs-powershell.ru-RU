---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: d4dcf52a3a705042f994c8106bd931a8b704a049
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078305"
---
# <span data-ttu-id="42cef-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="42cef-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="42cef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42cef-102">SYNOPSIS</span></span>
<span data-ttu-id="42cef-103">Создание или обновление сертификата службы подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="42cef-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="42cef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42cef-104">SYNTAX</span></span>

### <span data-ttu-id="42cef-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42cef-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42cef-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="42cef-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42cef-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="42cef-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42cef-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42cef-108">DESCRIPTION</span></span>
<span data-ttu-id="42cef-109">Выгружает новый сертификат или заменяет существующий сертификат с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="42cef-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="42cef-110">Подробное описание сертификатов ЦС в службе подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="42cef-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="42cef-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42cef-111">EXAMPLES</span></span>

### <span data-ttu-id="42cef-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42cef-112">Example 1</span></span>
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

<span data-ttu-id="42cef-113">Добавьте CER-файл сертификата ЦС в службу подготовки устройств центра Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="42cef-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="42cef-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="42cef-114">Example 2</span></span>
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

<span data-ttu-id="42cef-115">Обновляет сертификат ЦС в службе подготовки устройств центра Интернета вещей, загружая новый файл CER.</span><span class="sxs-lookup"><span data-stu-id="42cef-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="42cef-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42cef-116">PARAMETERS</span></span>

### <span data-ttu-id="42cef-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="42cef-117">-CertificateName</span></span>
<span data-ttu-id="42cef-118">Имя сертификата службы подготовки устройства IOT</span><span class="sxs-lookup"><span data-stu-id="42cef-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="42cef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42cef-119">-DefaultProfile</span></span>
<span data-ttu-id="42cef-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42cef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42cef-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="42cef-121">-Etag</span></span>
<span data-ttu-id="42cef-122">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="42cef-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="42cef-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42cef-123">-InputObject</span></span>
<span data-ttu-id="42cef-124">Объект сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="42cef-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="42cef-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42cef-125">-Name</span></span>
<span data-ttu-id="42cef-126">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="42cef-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="42cef-127">-Path</span><span class="sxs-lookup"><span data-stu-id="42cef-127">-Path</span></span>
<span data-ttu-id="42cef-128">базовое представление 64 сертификата X509. cer или PEM-файла.</span><span class="sxs-lookup"><span data-stu-id="42cef-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="42cef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42cef-129">-ResourceGroupName</span></span>
<span data-ttu-id="42cef-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="42cef-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="42cef-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42cef-131">-ResourceId</span></span>
<span data-ttu-id="42cef-132">Идентификатор ресурса сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="42cef-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="42cef-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42cef-133">-Confirm</span></span>
<span data-ttu-id="42cef-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42cef-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42cef-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42cef-135">-WhatIf</span></span>
<span data-ttu-id="42cef-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42cef-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42cef-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42cef-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42cef-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42cef-138">CommonParameters</span></span>
<span data-ttu-id="42cef-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42cef-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42cef-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42cef-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42cef-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42cef-141">INPUTS</span></span>

### <span data-ttu-id="42cef-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="42cef-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="42cef-143">System. String</span><span class="sxs-lookup"><span data-stu-id="42cef-143">System.String</span></span>

## <span data-ttu-id="42cef-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42cef-144">OUTPUTS</span></span>

### <span data-ttu-id="42cef-145">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="42cef-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="42cef-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="42cef-146">NOTES</span></span>

## <span data-ttu-id="42cef-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42cef-147">RELATED LINKS</span></span>
