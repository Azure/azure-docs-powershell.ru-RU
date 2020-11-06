---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
ms.openlocfilehash: 45afd8c7f690be7785a14d336fabe7ac52a6f44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568528"
---
# <span data-ttu-id="ac5d2-101">Set-AzureRmIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="ac5d2-101">Set-AzureRmIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="ac5d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ac5d2-103">Проверяет сертификат центра Интернета для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-103">Verifies an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac5d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac5d2-104">SYNTAX</span></span>

### <span data-ttu-id="ac5d2-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac5d2-105">ResourceSet (Default)</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac5d2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ac5d2-106">InputObjectSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac5d2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ac5d2-107">ResourceIdSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac5d2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac5d2-108">DESCRIPTION</span></span>
<span data-ttu-id="ac5d2-109">Проверяет сертификат, выдавая сертификат проверки, который содержит проверочный код, полученный командлетом Get-AzureRmIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzureRmIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="ac5d2-110">Это последний шаг в ходе проверки.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="ac5d2-111">Подробное описание сертификатов ЦС в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="ac5d2-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="ac5d2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac5d2-112">EXAMPLES</span></span>

### <span data-ttu-id="ac5d2-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac5d2-113">Example 1</span></span>
```
PS C:\> Set-AzureRmIotHubVerifiedCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\myverifiedcertificate.cer" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="ac5d2-114">Проверяет владение закрытым ключом MyCertificate.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="ac5d2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac5d2-115">PARAMETERS</span></span>

### <span data-ttu-id="ac5d2-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ac5d2-116">-CertificateName</span></span>
<span data-ttu-id="ac5d2-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="ac5d2-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="ac5d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac5d2-118">-DefaultProfile</span></span>
<span data-ttu-id="ac5d2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac5d2-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="ac5d2-120">-Etag</span></span>
<span data-ttu-id="ac5d2-121">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="ac5d2-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="ac5d2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac5d2-122">-InputObject</span></span>
<span data-ttu-id="ac5d2-123">Объект сертификата</span><span class="sxs-lookup"><span data-stu-id="ac5d2-123">Certificate Object</span></span>

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

### <span data-ttu-id="ac5d2-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac5d2-124">-Name</span></span>
<span data-ttu-id="ac5d2-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="ac5d2-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ac5d2-126">-Path</span><span class="sxs-lookup"><span data-stu-id="ac5d2-126">-Path</span></span>
<span data-ttu-id="ac5d2-127">Base-64. путь к файлу, который является файлом сертификата X509. cer или. PEM.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="ac5d2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac5d2-128">-ResourceGroupName</span></span>
<span data-ttu-id="ac5d2-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ac5d2-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ac5d2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac5d2-130">-ResourceId</span></span>
<span data-ttu-id="ac5d2-131">Идентификатор ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="ac5d2-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="ac5d2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac5d2-132">-Confirm</span></span>
<span data-ttu-id="ac5d2-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac5d2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac5d2-134">-WhatIf</span></span>
<span data-ttu-id="ac5d2-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac5d2-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac5d2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac5d2-137">CommonParameters</span></span>
<span data-ttu-id="ac5d2-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac5d2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac5d2-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac5d2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac5d2-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac5d2-140">INPUTS</span></span>

### <span data-ttu-id="ac5d2-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="ac5d2-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="ac5d2-142">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ac5d2-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ac5d2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ac5d2-143">System.String</span></span>

## <span data-ttu-id="ac5d2-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac5d2-144">OUTPUTS</span></span>

### <span data-ttu-id="ac5d2-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="ac5d2-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="ac5d2-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac5d2-146">NOTES</span></span>

## <span data-ttu-id="ac5d2-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac5d2-147">RELATED LINKS</span></span>
