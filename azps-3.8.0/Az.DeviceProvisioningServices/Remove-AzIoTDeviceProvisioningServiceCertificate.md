---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066383"
---
# <span data-ttu-id="ca2e5-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="ca2e5-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="ca2e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca2e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca2e5-103">Удаление сертификата службы подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ca2e5-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="ca2e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca2e5-104">SYNTAX</span></span>

### <span data-ttu-id="ca2e5-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca2e5-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca2e5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca2e5-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca2e5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca2e5-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca2e5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca2e5-108">DESCRIPTION</span></span>
<span data-ttu-id="ca2e5-109">Подробное описание сертификатов ЦС в службе подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="ca2e5-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="ca2e5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca2e5-110">EXAMPLES</span></span>

### <span data-ttu-id="ca2e5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ca2e5-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="ca2e5-112">Удалите "mycertificate" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ca2e5-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="ca2e5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca2e5-113">PARAMETERS</span></span>

### <span data-ttu-id="ca2e5-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ca2e5-114">-CertificateName</span></span>
<span data-ttu-id="ca2e5-115">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="ca2e5-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="ca2e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca2e5-116">-DefaultProfile</span></span>
<span data-ttu-id="ca2e5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca2e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca2e5-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="ca2e5-118">-Etag</span></span>
<span data-ttu-id="ca2e5-119">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="ca2e5-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="ca2e5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca2e5-120">-InputObject</span></span>
<span data-ttu-id="ca2e5-121">Объект сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="ca2e5-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="ca2e5-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca2e5-122">-Name</span></span>
<span data-ttu-id="ca2e5-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="ca2e5-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ca2e5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca2e5-124">-PassThru</span></span>
<span data-ttu-id="ca2e5-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="ca2e5-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ca2e5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca2e5-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca2e5-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ca2e5-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ca2e5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca2e5-128">-ResourceId</span></span>
<span data-ttu-id="ca2e5-129">Идентификатор ресурса сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="ca2e5-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="ca2e5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca2e5-130">-Confirm</span></span>
<span data-ttu-id="ca2e5-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ca2e5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca2e5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca2e5-132">-WhatIf</span></span>
<span data-ttu-id="ca2e5-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ca2e5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca2e5-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ca2e5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca2e5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca2e5-135">CommonParameters</span></span>
<span data-ttu-id="ca2e5-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca2e5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca2e5-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca2e5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca2e5-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca2e5-138">INPUTS</span></span>

### <span data-ttu-id="ca2e5-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="ca2e5-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="ca2e5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ca2e5-140">System.String</span></span>

## <span data-ttu-id="ca2e5-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca2e5-141">OUTPUTS</span></span>

### <span data-ttu-id="ca2e5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca2e5-142">System.Boolean</span></span>

## <span data-ttu-id="ca2e5-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca2e5-143">NOTES</span></span>

## <span data-ttu-id="ca2e5-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca2e5-144">RELATED LINKS</span></span>
