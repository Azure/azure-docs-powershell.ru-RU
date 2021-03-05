---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 5e887dc2f608dd7e26c05e3b7ca73036efe2595a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004099"
---
# <span data-ttu-id="a7a36-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="a7a36-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="a7a36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7a36-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a36-103">Проверяет сертификат Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="a7a36-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="a7a36-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7a36-104">SYNTAX</span></span>

### <span data-ttu-id="a7a36-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7a36-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7a36-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a7a36-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7a36-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a7a36-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7a36-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7a36-108">DESCRIPTION</span></span>
<span data-ttu-id="a7a36-109">Проверяет сертификат, загружая сертификат проверки, содержащий код проверки, полученный cmdlet Get-AzIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="a7a36-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="a7a36-110">Это последний этап процедуры подтверждения связи.</span><span class="sxs-lookup"><span data-stu-id="a7a36-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="a7a36-111">Подробное описание сертификатов ЦС в Azure IoT Hub см. в https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="a7a36-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="a7a36-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7a36-112">EXAMPLES</span></span>

### <span data-ttu-id="a7a36-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7a36-113">Example 1</span></span>
```
PS C:\> Set-AzIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="a7a36-114">Проверяет право собственности на закрытый ключ MyCertificate.</span><span class="sxs-lookup"><span data-stu-id="a7a36-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="a7a36-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7a36-115">PARAMETERS</span></span>

### <span data-ttu-id="a7a36-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a7a36-116">-CertificateName</span></span>
<span data-ttu-id="a7a36-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="a7a36-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="a7a36-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a36-118">-DefaultProfile</span></span>
<span data-ttu-id="a7a36-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7a36-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7a36-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="a7a36-120">-Etag</span></span>
<span data-ttu-id="a7a36-121">Etag of the Certificate</span><span class="sxs-lookup"><span data-stu-id="a7a36-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="a7a36-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7a36-122">-InputObject</span></span>
<span data-ttu-id="a7a36-123">Объект Certificate</span><span class="sxs-lookup"><span data-stu-id="a7a36-123">Certificate Object</span></span>

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

### <span data-ttu-id="a7a36-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a7a36-124">-Name</span></span>
<span data-ttu-id="a7a36-125">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="a7a36-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a7a36-126">-Path</span><span class="sxs-lookup"><span data-stu-id="a7a36-126">-Path</span></span>
<span data-ttu-id="a7a36-127">Представление файла сертификата X509 (CER- или PEM-файла) base-64.</span><span class="sxs-lookup"><span data-stu-id="a7a36-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7a36-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7a36-128">-ResourceGroupName</span></span>
<span data-ttu-id="a7a36-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a7a36-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a7a36-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7a36-130">-ResourceId</span></span>
<span data-ttu-id="a7a36-131">ИД ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="a7a36-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="a7a36-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7a36-132">-Confirm</span></span>
<span data-ttu-id="a7a36-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7a36-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7a36-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7a36-134">-WhatIf</span></span>
<span data-ttu-id="a7a36-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7a36-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7a36-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7a36-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7a36-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a36-137">CommonParameters</span></span>
<span data-ttu-id="a7a36-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7a36-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a36-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a36-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a36-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7a36-140">INPUTS</span></span>

### <span data-ttu-id="a7a36-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="a7a36-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="a7a36-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a7a36-142">System.String</span></span>

## <span data-ttu-id="a7a36-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7a36-143">OUTPUTS</span></span>

### <span data-ttu-id="a7a36-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="a7a36-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="a7a36-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7a36-145">NOTES</span></span>

## <span data-ttu-id="a7a36-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7a36-146">RELATED LINKS</span></span>
