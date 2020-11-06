---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHubVerifiedCertificate.md
ms.openlocfilehash: a241905b204de1bd7d0d372cdcafc6e321b8c98d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569015"
---
# <span data-ttu-id="e14bc-101">Set-AzureRmIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="e14bc-101">Set-AzureRmIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="e14bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e14bc-102">SYNOPSIS</span></span>
<span data-ttu-id="e14bc-103">Проверяет сертификат центра Интернета для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="e14bc-103">Verifies an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e14bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e14bc-104">SYNTAX</span></span>

### <span data-ttu-id="e14bc-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e14bc-105">ResourceSet (Default)</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e14bc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e14bc-106">InputObjectSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e14bc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e14bc-107">ResourceIdSet</span></span>
```
Set-AzureRmIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e14bc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e14bc-108">DESCRIPTION</span></span>
<span data-ttu-id="e14bc-109">Проверяет сертификат, выдавая сертификат проверки, который содержит проверочный код, полученный командлетом Get-AzureRmIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="e14bc-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzureRmIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="e14bc-110">Это последний шаг в ходе проверки.</span><span class="sxs-lookup"><span data-stu-id="e14bc-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="e14bc-111">Подробное описание сертификатов ЦС в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="e14bc-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="e14bc-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e14bc-112">EXAMPLES</span></span>

### <span data-ttu-id="e14bc-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e14bc-113">Example 1</span></span>
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

<span data-ttu-id="e14bc-114">Проверяет владение закрытым ключом MyCertificate.</span><span class="sxs-lookup"><span data-stu-id="e14bc-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="e14bc-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e14bc-115">PARAMETERS</span></span>

### <span data-ttu-id="e14bc-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e14bc-116">-CertificateName</span></span>
<span data-ttu-id="e14bc-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="e14bc-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="e14bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e14bc-118">-DefaultProfile</span></span>
<span data-ttu-id="e14bc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e14bc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e14bc-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="e14bc-120">-Etag</span></span>
<span data-ttu-id="e14bc-121">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="e14bc-121">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14bc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e14bc-122">-InputObject</span></span>
<span data-ttu-id="e14bc-123">Объект сертификата</span><span class="sxs-lookup"><span data-stu-id="e14bc-123">Certificate Object</span></span>

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

### <span data-ttu-id="e14bc-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e14bc-124">-Name</span></span>
<span data-ttu-id="e14bc-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="e14bc-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e14bc-126">-Path</span><span class="sxs-lookup"><span data-stu-id="e14bc-126">-Path</span></span>
<span data-ttu-id="e14bc-127">Base-64. путь к файлу, который является файлом сертификата X509. cer или. PEM.</span><span class="sxs-lookup"><span data-stu-id="e14bc-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14bc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e14bc-128">-ResourceGroupName</span></span>
<span data-ttu-id="e14bc-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e14bc-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e14bc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e14bc-130">-ResourceId</span></span>
<span data-ttu-id="e14bc-131">Идентификатор ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="e14bc-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="e14bc-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e14bc-132">-Confirm</span></span>
<span data-ttu-id="e14bc-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e14bc-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14bc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e14bc-134">-WhatIf</span></span>
<span data-ttu-id="e14bc-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e14bc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e14bc-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e14bc-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e14bc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e14bc-137">CommonParameters</span></span>
<span data-ttu-id="e14bc-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e14bc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e14bc-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e14bc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e14bc-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e14bc-140">INPUTS</span></span>

### <span data-ttu-id="e14bc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e14bc-141">System.String</span></span>

## <span data-ttu-id="e14bc-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e14bc-142">OUTPUTS</span></span>

### <span data-ttu-id="e14bc-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="e14bc-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="e14bc-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e14bc-144">NOTES</span></span>

## <span data-ttu-id="e14bc-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e14bc-145">RELATED LINKS</span></span>

