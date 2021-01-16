---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 78881a7bd82aedeed4dca2a7ee08ea40812a0b05
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425887"
---
# <span data-ttu-id="00da0-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="00da0-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="00da0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00da0-102">SYNOPSIS</span></span>
<span data-ttu-id="00da0-103">Проверяет сертификат Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="00da0-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="00da0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="00da0-104">SYNTAX</span></span>

### <span data-ttu-id="00da0-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00da0-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00da0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="00da0-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00da0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="00da0-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00da0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00da0-108">DESCRIPTION</span></span>
<span data-ttu-id="00da0-109">Проверяет сертификат, загружая сертификат проверки, содержащий код проверки, полученный cmdlet Get-AzIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="00da0-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="00da0-110">Это последний шаг в процессе проверки связи.</span><span class="sxs-lookup"><span data-stu-id="00da0-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="00da0-111">Подробное описание сертификатов ЦС в Azure IoT Hub см. в https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="00da0-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="00da0-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="00da0-112">EXAMPLES</span></span>

### <span data-ttu-id="00da0-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00da0-113">Example 1</span></span>
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

<span data-ttu-id="00da0-114">Проверяет право собственности на закрытый ключ MyCertificate.</span><span class="sxs-lookup"><span data-stu-id="00da0-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="00da0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00da0-115">PARAMETERS</span></span>

### <span data-ttu-id="00da0-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="00da0-116">-CertificateName</span></span>
<span data-ttu-id="00da0-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="00da0-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="00da0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00da0-118">-DefaultProfile</span></span>
<span data-ttu-id="00da0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00da0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00da0-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="00da0-120">-Etag</span></span>
<span data-ttu-id="00da0-121">Etag of the Certificate</span><span class="sxs-lookup"><span data-stu-id="00da0-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="00da0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00da0-122">-InputObject</span></span>
<span data-ttu-id="00da0-123">Объект Certificate</span><span class="sxs-lookup"><span data-stu-id="00da0-123">Certificate Object</span></span>

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

### <span data-ttu-id="00da0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="00da0-124">-Name</span></span>
<span data-ttu-id="00da0-125">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="00da0-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="00da0-126">-Path</span><span class="sxs-lookup"><span data-stu-id="00da0-126">-Path</span></span>
<span data-ttu-id="00da0-127">Представление файла сертификата X509 (CER- или PEM-файла) base-64.</span><span class="sxs-lookup"><span data-stu-id="00da0-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="00da0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00da0-128">-ResourceGroupName</span></span>
<span data-ttu-id="00da0-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="00da0-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="00da0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00da0-130">-ResourceId</span></span>
<span data-ttu-id="00da0-131">ИД ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="00da0-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="00da0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00da0-132">-Confirm</span></span>
<span data-ttu-id="00da0-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00da0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00da0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00da0-134">-WhatIf</span></span>
<span data-ttu-id="00da0-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00da0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00da0-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="00da0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00da0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00da0-137">CommonParameters</span></span>
<span data-ttu-id="00da0-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00da0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00da0-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00da0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00da0-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00da0-140">INPUTS</span></span>

### <span data-ttu-id="00da0-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="00da0-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="00da0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="00da0-142">System.String</span></span>

## <span data-ttu-id="00da0-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="00da0-143">OUTPUTS</span></span>

### <span data-ttu-id="00da0-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="00da0-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="00da0-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="00da0-145">NOTES</span></span>

## <span data-ttu-id="00da0-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00da0-146">RELATED LINKS</span></span>
