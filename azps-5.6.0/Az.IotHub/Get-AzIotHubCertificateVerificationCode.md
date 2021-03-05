---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 5cad5da87b15430c33d748250501862dae77a38e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988140"
---
# <span data-ttu-id="86aca-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="86aca-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="86aca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86aca-102">SYNOPSIS</span></span>
<span data-ttu-id="86aca-103">Создает код проверки для сертификата Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="86aca-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="86aca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86aca-104">SYNTAX</span></span>

### <span data-ttu-id="86aca-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86aca-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86aca-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="86aca-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86aca-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="86aca-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86aca-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86aca-108">DESCRIPTION</span></span>
<span data-ttu-id="86aca-109">Этот код проверки используется для завершения процедуры подтверждения сертификата.</span><span class="sxs-lookup"><span data-stu-id="86aca-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="86aca-110">Используйте этот код проверки в качестве CN нового сертификата, подписанного с закрытым ключом корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="86aca-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="86aca-111">Подробное описание сертификатов ЦС в Azure IoT Hub см. в https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="86aca-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="86aca-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86aca-112">EXAMPLES</span></span>

### <span data-ttu-id="86aca-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="86aca-113">Example 1</span></span>
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

<span data-ttu-id="86aca-114">Создает код проверки для MyCertificate.</span><span class="sxs-lookup"><span data-stu-id="86aca-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="86aca-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86aca-115">PARAMETERS</span></span>

### <span data-ttu-id="86aca-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="86aca-116">-CertificateName</span></span>
<span data-ttu-id="86aca-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="86aca-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="86aca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86aca-118">-DefaultProfile</span></span>
<span data-ttu-id="86aca-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86aca-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86aca-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="86aca-120">-Etag</span></span>
<span data-ttu-id="86aca-121">Etag of the Certificate</span><span class="sxs-lookup"><span data-stu-id="86aca-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="86aca-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86aca-122">-InputObject</span></span>
<span data-ttu-id="86aca-123">Объект Certificate</span><span class="sxs-lookup"><span data-stu-id="86aca-123">Certificate Object</span></span>

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

### <span data-ttu-id="86aca-124">-Name</span><span class="sxs-lookup"><span data-stu-id="86aca-124">-Name</span></span>
<span data-ttu-id="86aca-125">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="86aca-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="86aca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86aca-126">-ResourceGroupName</span></span>
<span data-ttu-id="86aca-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="86aca-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="86aca-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86aca-128">-ResourceId</span></span>
<span data-ttu-id="86aca-129">ИД ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="86aca-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="86aca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86aca-130">CommonParameters</span></span>
<span data-ttu-id="86aca-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86aca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86aca-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86aca-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86aca-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86aca-133">INPUTS</span></span>

### <span data-ttu-id="86aca-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="86aca-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="86aca-135">System.String</span><span class="sxs-lookup"><span data-stu-id="86aca-135">System.String</span></span>

## <span data-ttu-id="86aca-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86aca-136">OUTPUTS</span></span>

### <span data-ttu-id="86aca-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="86aca-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="86aca-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86aca-138">NOTES</span></span>

## <span data-ttu-id="86aca-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86aca-139">RELATED LINKS</span></span>
