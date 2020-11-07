---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 64de44e74b5c6ea21d9d49b1911bcd34a74a374a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732946"
---
# <span data-ttu-id="e4b88-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="e4b88-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="e4b88-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4b88-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b88-103">Удаление сертификата службы подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e4b88-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4b88-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4b88-104">SYNTAX</span></span>

### <span data-ttu-id="e4b88-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e4b88-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4b88-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e4b88-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4b88-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e4b88-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4b88-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4b88-108">DESCRIPTION</span></span>
<span data-ttu-id="e4b88-109">Подробное описание сертификатов ЦС в службе подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="e4b88-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="e4b88-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4b88-110">EXAMPLES</span></span>

### <span data-ttu-id="e4b88-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e4b88-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="e4b88-112">Удалите "mycertificate" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e4b88-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="e4b88-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4b88-113">PARAMETERS</span></span>

### <span data-ttu-id="e4b88-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e4b88-114">-CertificateName</span></span>
<span data-ttu-id="e4b88-115">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="e4b88-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="e4b88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b88-116">-DefaultProfile</span></span>
<span data-ttu-id="e4b88-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4b88-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4b88-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="e4b88-118">-Etag</span></span>
<span data-ttu-id="e4b88-119">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="e4b88-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="e4b88-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4b88-120">-InputObject</span></span>
<span data-ttu-id="e4b88-121">Объект сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="e4b88-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="e4b88-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e4b88-122">-Name</span></span>
<span data-ttu-id="e4b88-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="e4b88-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e4b88-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4b88-124">-PassThru</span></span>
<span data-ttu-id="e4b88-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="e4b88-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e4b88-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4b88-126">-ResourceGroupName</span></span>
<span data-ttu-id="e4b88-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e4b88-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e4b88-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4b88-128">-ResourceId</span></span>
<span data-ttu-id="e4b88-129">Идентификатор ресурса сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="e4b88-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="e4b88-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4b88-130">-Confirm</span></span>
<span data-ttu-id="e4b88-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e4b88-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4b88-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4b88-132">-WhatIf</span></span>
<span data-ttu-id="e4b88-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e4b88-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4b88-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e4b88-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4b88-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b88-135">CommonParameters</span></span>
<span data-ttu-id="e4b88-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4b88-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b88-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4b88-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b88-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4b88-138">INPUTS</span></span>

### <span data-ttu-id="e4b88-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="e4b88-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="e4b88-140">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e4b88-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e4b88-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e4b88-141">System.String</span></span>

## <span data-ttu-id="e4b88-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4b88-142">OUTPUTS</span></span>

### <span data-ttu-id="e4b88-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4b88-143">System.Boolean</span></span>

## <span data-ttu-id="e4b88-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4b88-144">NOTES</span></span>

## <span data-ttu-id="e4b88-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4b88-145">RELATED LINKS</span></span>
