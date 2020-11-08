---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 4bf362402ba3db0ba50d9144d6bb9fa79977a998
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078079"
---
# <span data-ttu-id="9c9fb-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="9c9fb-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="9c9fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c9fb-102">SYNOPSIS</span></span>
<span data-ttu-id="9c9fb-103">Создает проверочный код для сертификата центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="9c9fb-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="9c9fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c9fb-104">SYNTAX</span></span>

### <span data-ttu-id="9c9fb-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c9fb-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c9fb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9c9fb-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c9fb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9c9fb-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c9fb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c9fb-108">DESCRIPTION</span></span>
<span data-ttu-id="9c9fb-109">Этот проверочный код используется для завершения этапа проверки подлинности для сертификата.</span><span class="sxs-lookup"><span data-stu-id="9c9fb-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="9c9fb-110">Используйте этот проверочный код в качестве CN нового сертификата, подписанного закрытым ключом корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="9c9fb-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="9c9fb-111">Подробное описание сертификатов ЦС в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="9c9fb-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="9c9fb-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c9fb-112">EXAMPLES</span></span>

### <span data-ttu-id="9c9fb-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9c9fb-113">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="9c9fb-114">Создает проверочный код для MyCertificate</span><span class="sxs-lookup"><span data-stu-id="9c9fb-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="9c9fb-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c9fb-115">PARAMETERS</span></span>

### <span data-ttu-id="9c9fb-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9c9fb-116">-CertificateName</span></span>
<span data-ttu-id="9c9fb-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="9c9fb-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="9c9fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c9fb-118">-DefaultProfile</span></span>
<span data-ttu-id="9c9fb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c9fb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c9fb-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="9c9fb-120">-Etag</span></span>
<span data-ttu-id="9c9fb-121">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="9c9fb-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="9c9fb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c9fb-122">-InputObject</span></span>
<span data-ttu-id="9c9fb-123">Объект сертификата</span><span class="sxs-lookup"><span data-stu-id="9c9fb-123">Certificate Object</span></span>

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

### <span data-ttu-id="9c9fb-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c9fb-124">-Name</span></span>
<span data-ttu-id="9c9fb-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="9c9fb-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9c9fb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c9fb-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c9fb-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9c9fb-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9c9fb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c9fb-128">-ResourceId</span></span>
<span data-ttu-id="9c9fb-129">Идентификатор ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="9c9fb-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="9c9fb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c9fb-130">CommonParameters</span></span>
<span data-ttu-id="9c9fb-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c9fb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c9fb-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c9fb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c9fb-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c9fb-133">INPUTS</span></span>

### <span data-ttu-id="9c9fb-134">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="9c9fb-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="9c9fb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9c9fb-135">System.String</span></span>

## <span data-ttu-id="9c9fb-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c9fb-136">OUTPUTS</span></span>

### <span data-ttu-id="9c9fb-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="9c9fb-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="9c9fb-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c9fb-138">NOTES</span></span>

## <span data-ttu-id="9c9fb-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c9fb-139">RELATED LINKS</span></span>
