---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328681"
---
# <span data-ttu-id="3db43-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="3db43-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="3db43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3db43-102">SYNOPSIS</span></span>
<span data-ttu-id="3db43-103">Удаление сертификата службы регистрации устройств в Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3db43-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="3db43-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3db43-104">SYNTAX</span></span>

### <span data-ttu-id="3db43-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3db43-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db43-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3db43-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db43-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3db43-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3db43-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3db43-108">DESCRIPTION</span></span>
<span data-ttu-id="3db43-109">Подробное описание сертификатов ЦС в службе регистрации устройств на концентраторе IoT Azure см. в https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="3db43-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="3db43-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3db43-110">EXAMPLES</span></span>

### <span data-ttu-id="3db43-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3db43-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="3db43-112">Удалите mycertificate в службе по подготовкам устройств через Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="3db43-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3db43-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3db43-113">PARAMETERS</span></span>

### <span data-ttu-id="3db43-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="3db43-114">-CertificateName</span></span>
<span data-ttu-id="3db43-115">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="3db43-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="3db43-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db43-116">-DefaultProfile</span></span>
<span data-ttu-id="3db43-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3db43-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3db43-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="3db43-118">-Etag</span></span>
<span data-ttu-id="3db43-119">Etag of the Certificate</span><span class="sxs-lookup"><span data-stu-id="3db43-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="3db43-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3db43-120">-InputObject</span></span>
<span data-ttu-id="3db43-121">Объект сертификата службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="3db43-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="3db43-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3db43-122">-Name</span></span>
<span data-ttu-id="3db43-123">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="3db43-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3db43-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3db43-124">-PassThru</span></span>
<span data-ttu-id="3db43-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3db43-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3db43-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3db43-126">-ResourceGroupName</span></span>
<span data-ttu-id="3db43-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3db43-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3db43-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3db43-128">-ResourceId</span></span>
<span data-ttu-id="3db43-129">IoT Device Provisioning Service Certificate Resource Id</span><span class="sxs-lookup"><span data-stu-id="3db43-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="3db43-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3db43-130">-Confirm</span></span>
<span data-ttu-id="3db43-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3db43-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3db43-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3db43-132">-WhatIf</span></span>
<span data-ttu-id="3db43-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3db43-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3db43-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3db43-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3db43-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db43-135">CommonParameters</span></span>
<span data-ttu-id="3db43-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3db43-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db43-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3db43-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db43-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3db43-138">INPUTS</span></span>

### <span data-ttu-id="3db43-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="3db43-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="3db43-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3db43-140">System.String</span></span>

## <span data-ttu-id="3db43-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3db43-141">OUTPUTS</span></span>

### <span data-ttu-id="3db43-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3db43-142">System.Boolean</span></span>

## <span data-ttu-id="3db43-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3db43-143">NOTES</span></span>

## <span data-ttu-id="3db43-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3db43-144">RELATED LINKS</span></span>
