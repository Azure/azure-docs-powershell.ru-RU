---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
ms.openlocfilehash: 55cd14216e9a592128c8d600238b49862cb1f20a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564884"
---
# <span data-ttu-id="949b4-101">Get-AzureRmIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="949b4-101">Get-AzureRmIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="949b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="949b4-102">SYNOPSIS</span></span>
<span data-ttu-id="949b4-103">Создает проверочный код для сертификата центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="949b4-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="949b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="949b4-104">SYNTAX</span></span>

### <span data-ttu-id="949b4-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="949b4-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="949b4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="949b4-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="949b4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="949b4-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="949b4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="949b4-108">DESCRIPTION</span></span>
<span data-ttu-id="949b4-109">Этот проверочный код используется для завершения этапа проверки подлинности для сертификата.</span><span class="sxs-lookup"><span data-stu-id="949b4-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="949b4-110">Используйте этот проверочный код в качестве CN нового сертификата, подписанного закрытым ключом корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="949b4-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="949b4-111">Подробное описание сертификатов ЦС в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="949b4-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="949b4-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="949b4-112">EXAMPLES</span></span>

### <span data-ttu-id="949b4-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="949b4-113">Example 1</span></span>
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

<span data-ttu-id="949b4-114">Создает проверочный код для MyCertificate</span><span class="sxs-lookup"><span data-stu-id="949b4-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="949b4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="949b4-115">PARAMETERS</span></span>

### <span data-ttu-id="949b4-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="949b4-116">-CertificateName</span></span>
<span data-ttu-id="949b4-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="949b4-117">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="949b4-118">-DefaultProfile</span></span>
<span data-ttu-id="949b4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="949b4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949b4-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="949b4-120">-Etag</span></span>
<span data-ttu-id="949b4-121">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="949b4-121">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="949b4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="949b4-122">-InputObject</span></span>
<span data-ttu-id="949b4-123">Объект сертификата</span><span class="sxs-lookup"><span data-stu-id="949b4-123">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="949b4-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="949b4-124">-Name</span></span>
<span data-ttu-id="949b4-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="949b4-125">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="949b4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="949b4-126">-ResourceGroupName</span></span>
<span data-ttu-id="949b4-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="949b4-127">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="949b4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="949b4-128">-ResourceId</span></span>
<span data-ttu-id="949b4-129">Идентификатор ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="949b4-129">Certificate Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="949b4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="949b4-130">CommonParameters</span></span>
<span data-ttu-id="949b4-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="949b4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="949b4-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="949b4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="949b4-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="949b4-133">INPUTS</span></span>

### <span data-ttu-id="949b4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="949b4-134">System.String</span></span>

## <span data-ttu-id="949b4-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="949b4-135">OUTPUTS</span></span>

### <span data-ttu-id="949b4-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="949b4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="949b4-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="949b4-137">NOTES</span></span>

## <span data-ttu-id="949b4-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="949b4-138">RELATED LINKS</span></span>

