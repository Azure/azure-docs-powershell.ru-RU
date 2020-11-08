---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: aa51001163e4559dd0d3ef7edfb48abd3448c0b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245520"
---
# <span data-ttu-id="59e95-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="59e95-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="59e95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59e95-102">SYNOPSIS</span></span>
<span data-ttu-id="59e95-103">Список всех сертификатов или определенного сертификата, содержащегося в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="59e95-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="59e95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59e95-104">SYNTAX</span></span>

### <span data-ttu-id="59e95-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59e95-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59e95-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="59e95-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59e95-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="59e95-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59e95-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59e95-108">DESCRIPTION</span></span>
<span data-ttu-id="59e95-109">Подробное описание сертификатов ЦС в службе подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="59e95-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="59e95-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59e95-110">EXAMPLES</span></span>

### <span data-ttu-id="59e95-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59e95-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

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

<span data-ttu-id="59e95-112">Показать подробные сведения о "mycertificate" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="59e95-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="59e95-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="59e95-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="59e95-114">Перечислите все сертификаты в "myiotdps" с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="59e95-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="59e95-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59e95-115">PARAMETERS</span></span>

### <span data-ttu-id="59e95-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="59e95-116">-CertificateName</span></span>
<span data-ttu-id="59e95-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="59e95-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="59e95-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e95-118">-DefaultProfile</span></span>
<span data-ttu-id="59e95-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59e95-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59e95-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="59e95-120">-DpsObject</span></span>
<span data-ttu-id="59e95-121">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="59e95-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59e95-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59e95-122">-Name</span></span>
<span data-ttu-id="59e95-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="59e95-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="59e95-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59e95-124">-ResourceGroupName</span></span>
<span data-ttu-id="59e95-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="59e95-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="59e95-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59e95-126">-ResourceId</span></span>
<span data-ttu-id="59e95-127">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="59e95-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="59e95-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e95-128">CommonParameters</span></span>
<span data-ttu-id="59e95-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59e95-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e95-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59e95-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e95-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59e95-131">INPUTS</span></span>

### <span data-ttu-id="59e95-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="59e95-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="59e95-133">System. String</span><span class="sxs-lookup"><span data-stu-id="59e95-133">System.String</span></span>

## <span data-ttu-id="59e95-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59e95-134">OUTPUTS</span></span>

### <span data-ttu-id="59e95-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="59e95-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="59e95-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="59e95-136">NOTES</span></span>

## <span data-ttu-id="59e95-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59e95-137">RELATED LINKS</span></span>
