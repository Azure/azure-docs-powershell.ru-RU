---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: c44e36a0aa08daf7e4a9ae9822f8a4be85db5d57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556667"
---
# <span data-ttu-id="c0a55-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="c0a55-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="c0a55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0a55-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a55-103">Список всех сертификатов или определенного сертификата, содержащегося в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="c0a55-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0a55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0a55-104">SYNTAX</span></span>

### <span data-ttu-id="c0a55-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0a55-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0a55-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c0a55-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0a55-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c0a55-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0a55-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0a55-108">DESCRIPTION</span></span>
<span data-ttu-id="c0a55-109">Подробное описание сертификатов ЦС в службе подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="c0a55-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="c0a55-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0a55-110">EXAMPLES</span></span>

### <span data-ttu-id="c0a55-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0a55-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

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

<span data-ttu-id="c0a55-112">Показать подробные сведения о "mycertificate" в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="c0a55-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="c0a55-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c0a55-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzureRmIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="c0a55-114">Перечислите все сертификаты в "myiotdps" с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="c0a55-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="c0a55-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0a55-115">PARAMETERS</span></span>

### <span data-ttu-id="c0a55-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c0a55-116">-CertificateName</span></span>
<span data-ttu-id="c0a55-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="c0a55-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="c0a55-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a55-118">-DefaultProfile</span></span>
<span data-ttu-id="c0a55-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0a55-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0a55-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c0a55-120">-DpsObject</span></span>
<span data-ttu-id="c0a55-121">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="c0a55-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c0a55-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0a55-122">-Name</span></span>
<span data-ttu-id="c0a55-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="c0a55-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c0a55-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0a55-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0a55-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c0a55-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c0a55-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0a55-126">-ResourceId</span></span>
<span data-ttu-id="c0a55-127">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="c0a55-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c0a55-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a55-128">CommonParameters</span></span>
<span data-ttu-id="c0a55-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0a55-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a55-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0a55-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a55-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0a55-131">INPUTS</span></span>

### <span data-ttu-id="c0a55-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c0a55-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="c0a55-133">Параметры: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c0a55-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="c0a55-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c0a55-134">System.String</span></span>

## <span data-ttu-id="c0a55-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0a55-135">OUTPUTS</span></span>

### <span data-ttu-id="c0a55-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="c0a55-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="c0a55-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0a55-137">NOTES</span></span>

## <span data-ttu-id="c0a55-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0a55-138">RELATED LINKS</span></span>
