---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
ms.openlocfilehash: a2c4c72f93597f3275e9edb1fecb6139eafbeb50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568538"
---
# <span data-ttu-id="a2b96-101">Get-AzureRmIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="a2b96-101">Get-AzureRmIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="a2b96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2b96-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b96-103">Создает проверочный код для сертификата центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="a2b96-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2b96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2b96-104">SYNTAX</span></span>

### <span data-ttu-id="a2b96-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2b96-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2b96-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a2b96-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2b96-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a2b96-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2b96-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2b96-108">DESCRIPTION</span></span>
<span data-ttu-id="a2b96-109">Этот проверочный код используется для завершения этапа проверки подлинности для сертификата.</span><span class="sxs-lookup"><span data-stu-id="a2b96-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="a2b96-110">Используйте этот проверочный код в качестве CN нового сертификата, подписанного закрытым ключом корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a2b96-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="a2b96-111">Подробное описание сертификатов ЦС в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="a2b96-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="a2b96-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2b96-112">EXAMPLES</span></span>

### <span data-ttu-id="a2b96-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2b96-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
VerificationCode    : 47292AB6260DB02CCD2D07C601B7303DD49858B6
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="a2b96-114">Создает проверочный код для MyCertificate</span><span class="sxs-lookup"><span data-stu-id="a2b96-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="a2b96-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2b96-115">PARAMETERS</span></span>

### <span data-ttu-id="a2b96-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a2b96-116">-CertificateName</span></span>
<span data-ttu-id="a2b96-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="a2b96-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="a2b96-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b96-118">-DefaultProfile</span></span>
<span data-ttu-id="a2b96-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2b96-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2b96-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="a2b96-120">-Etag</span></span>
<span data-ttu-id="a2b96-121">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="a2b96-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="a2b96-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2b96-122">-InputObject</span></span>
<span data-ttu-id="a2b96-123">Объект сертификата</span><span class="sxs-lookup"><span data-stu-id="a2b96-123">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2b96-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a2b96-124">-Name</span></span>
<span data-ttu-id="a2b96-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="a2b96-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2b96-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b96-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2b96-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a2b96-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2b96-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2b96-128">-ResourceId</span></span>
<span data-ttu-id="a2b96-129">Идентификатор ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="a2b96-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="a2b96-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b96-130">CommonParameters</span></span>
<span data-ttu-id="a2b96-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2b96-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b96-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2b96-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b96-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2b96-133">INPUTS</span></span>

### <span data-ttu-id="a2b96-134">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="a2b96-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="a2b96-135">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a2b96-135">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a2b96-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a2b96-136">System.String</span></span>

## <span data-ttu-id="a2b96-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2b96-137">OUTPUTS</span></span>

### <span data-ttu-id="a2b96-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="a2b96-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="a2b96-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2b96-139">NOTES</span></span>

## <span data-ttu-id="a2b96-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2b96-140">RELATED LINKS</span></span>
