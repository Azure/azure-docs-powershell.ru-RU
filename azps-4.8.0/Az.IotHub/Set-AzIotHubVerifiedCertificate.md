---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubverifiedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubVerifiedCertificate.md
ms.openlocfilehash: 78881a7bd82aedeed4dca2a7ee08ea40812a0b05
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244506"
---
# <span data-ttu-id="92175-101">Set-AzIotHubVerifiedCertificate</span><span class="sxs-lookup"><span data-stu-id="92175-101">Set-AzIotHubVerifiedCertificate</span></span>

## <span data-ttu-id="92175-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92175-102">SYNOPSIS</span></span>
<span data-ttu-id="92175-103">Проверяет сертификат центра Интернета для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="92175-103">Verifies an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="92175-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92175-104">SYNTAX</span></span>

### <span data-ttu-id="92175-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92175-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92175-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="92175-106">InputObjectSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-InputObject] <PSCertificateDescription> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92175-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="92175-107">ResourceIdSet</span></span>
```
Set-AzIotHubVerifiedCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92175-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92175-108">DESCRIPTION</span></span>
<span data-ttu-id="92175-109">Проверяет сертификат, выдавая сертификат проверки, который содержит проверочный код, полученный командлетом Get-AzIotHubCertificateVerificationCode.</span><span class="sxs-lookup"><span data-stu-id="92175-109">Verifies a certificate by uploading a verification certificate containing the verification code obtained by cmdlet Get-AzIotHubCertificateVerificationCode.</span></span> <span data-ttu-id="92175-110">Это последний шаг в ходе проверки.</span><span class="sxs-lookup"><span data-stu-id="92175-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="92175-111">Подробное описание сертификатов ЦС в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="92175-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="92175-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92175-112">EXAMPLES</span></span>

### <span data-ttu-id="92175-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92175-113">Example 1</span></span>
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

<span data-ttu-id="92175-114">Проверяет владение закрытым ключом MyCertificate.</span><span class="sxs-lookup"><span data-stu-id="92175-114">Verifies ownership of the MyCertificate private key.</span></span> 

## <span data-ttu-id="92175-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92175-115">PARAMETERS</span></span>

### <span data-ttu-id="92175-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="92175-116">-CertificateName</span></span>
<span data-ttu-id="92175-117">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="92175-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="92175-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92175-118">-DefaultProfile</span></span>
<span data-ttu-id="92175-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92175-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92175-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="92175-120">-Etag</span></span>
<span data-ttu-id="92175-121">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="92175-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="92175-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92175-122">-InputObject</span></span>
<span data-ttu-id="92175-123">Объект сертификата</span><span class="sxs-lookup"><span data-stu-id="92175-123">Certificate Object</span></span>

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

### <span data-ttu-id="92175-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92175-124">-Name</span></span>
<span data-ttu-id="92175-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="92175-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="92175-126">-Path</span><span class="sxs-lookup"><span data-stu-id="92175-126">-Path</span></span>
<span data-ttu-id="92175-127">Base-64. путь к файлу, который является файлом сертификата X509. cer или. PEM.</span><span class="sxs-lookup"><span data-stu-id="92175-127">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="92175-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92175-128">-ResourceGroupName</span></span>
<span data-ttu-id="92175-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="92175-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="92175-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92175-130">-ResourceId</span></span>
<span data-ttu-id="92175-131">Идентификатор ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="92175-131">Certificate Resource Id</span></span>

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

### <span data-ttu-id="92175-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92175-132">-Confirm</span></span>
<span data-ttu-id="92175-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="92175-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92175-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92175-134">-WhatIf</span></span>
<span data-ttu-id="92175-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="92175-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92175-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="92175-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92175-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92175-137">CommonParameters</span></span>
<span data-ttu-id="92175-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92175-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92175-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92175-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92175-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92175-140">INPUTS</span></span>

### <span data-ttu-id="92175-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="92175-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="92175-142">System. String</span><span class="sxs-lookup"><span data-stu-id="92175-142">System.String</span></span>

## <span data-ttu-id="92175-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92175-143">OUTPUTS</span></span>

### <span data-ttu-id="92175-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="92175-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="92175-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="92175-145">NOTES</span></span>

## <span data-ttu-id="92175-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92175-146">RELATED LINKS</span></span>