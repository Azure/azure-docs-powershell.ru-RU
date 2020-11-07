---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: e03bb9f8f996c274abe07dd3e1b005760756d632
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730913"
---
# <span data-ttu-id="8bd93-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="8bd93-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="8bd93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8bd93-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd93-103">Удаление сертификата службы подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="8bd93-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="8bd93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8bd93-104">SYNTAX</span></span>

### <span data-ttu-id="8bd93-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8bd93-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bd93-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8bd93-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bd93-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8bd93-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bd93-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bd93-108">DESCRIPTION</span></span>
<span data-ttu-id="8bd93-109">Подробное описание сертификатов ЦС в службе подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="8bd93-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="8bd93-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8bd93-110">EXAMPLES</span></span>

### <span data-ttu-id="8bd93-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8bd93-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="8bd93-112">Удалите "mycertificate" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="8bd93-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="8bd93-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8bd93-113">PARAMETERS</span></span>

### <span data-ttu-id="8bd93-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="8bd93-114">-CertificateName</span></span>
<span data-ttu-id="8bd93-115">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="8bd93-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="8bd93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd93-116">-DefaultProfile</span></span>
<span data-ttu-id="8bd93-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd93-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bd93-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="8bd93-118">-Etag</span></span>
<span data-ttu-id="8bd93-119">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="8bd93-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="8bd93-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bd93-120">-InputObject</span></span>
<span data-ttu-id="8bd93-121">Объект сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="8bd93-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="8bd93-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8bd93-122">-Name</span></span>
<span data-ttu-id="8bd93-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="8bd93-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8bd93-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bd93-124">-PassThru</span></span>
<span data-ttu-id="8bd93-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="8bd93-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8bd93-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bd93-126">-ResourceGroupName</span></span>
<span data-ttu-id="8bd93-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8bd93-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8bd93-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bd93-128">-ResourceId</span></span>
<span data-ttu-id="8bd93-129">Идентификатор ресурса сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="8bd93-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="8bd93-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bd93-130">-Confirm</span></span>
<span data-ttu-id="8bd93-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8bd93-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bd93-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bd93-132">-WhatIf</span></span>
<span data-ttu-id="8bd93-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8bd93-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bd93-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8bd93-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bd93-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd93-135">CommonParameters</span></span>
<span data-ttu-id="8bd93-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8bd93-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd93-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bd93-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd93-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8bd93-138">INPUTS</span></span>

### <span data-ttu-id="8bd93-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="8bd93-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="8bd93-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8bd93-140">System.String</span></span>

## <span data-ttu-id="8bd93-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bd93-141">OUTPUTS</span></span>

### <span data-ttu-id="8bd93-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8bd93-142">System.Boolean</span></span>

## <span data-ttu-id="8bd93-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="8bd93-143">NOTES</span></span>

## <span data-ttu-id="8bd93-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bd93-144">RELATED LINKS</span></span>
