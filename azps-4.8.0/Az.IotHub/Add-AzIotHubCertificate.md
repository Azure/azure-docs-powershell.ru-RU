---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 6d77bcc6d940c5891b4fc06875dc353af5f75939
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236453"
---
# <span data-ttu-id="54fae-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="54fae-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="54fae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54fae-102">SYNOPSIS</span></span>
<span data-ttu-id="54fae-103">Создание или обновление сертификата центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="54fae-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="54fae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54fae-104">SYNTAX</span></span>

### <span data-ttu-id="54fae-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54fae-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54fae-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="54fae-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54fae-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="54fae-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54fae-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54fae-108">DESCRIPTION</span></span>
<span data-ttu-id="54fae-109">Выгружает новый сертификат или заменяет существующий сертификат с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="54fae-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="54fae-110">Подробное описание сертификатов ЦС в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="54fae-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="54fae-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54fae-111">EXAMPLES</span></span>

### <span data-ttu-id="54fae-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54fae-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="54fae-113">Передает файл CER сертификата ЦС в центр Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="54fae-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="54fae-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="54fae-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="54fae-115">Обновляет сертификат ЦС в центре Интернета вещей, загружая новый файл CER.</span><span class="sxs-lookup"><span data-stu-id="54fae-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="54fae-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54fae-116">PARAMETERS</span></span>

### <span data-ttu-id="54fae-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="54fae-117">-CertificateName</span></span>
<span data-ttu-id="54fae-118">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="54fae-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="54fae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fae-119">-DefaultProfile</span></span>
<span data-ttu-id="54fae-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54fae-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54fae-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="54fae-121">-Etag</span></span>
<span data-ttu-id="54fae-122">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="54fae-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="54fae-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54fae-123">-InputObject</span></span>
<span data-ttu-id="54fae-124">Объект сертификата</span><span class="sxs-lookup"><span data-stu-id="54fae-124">Certificate Object</span></span>

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

### <span data-ttu-id="54fae-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54fae-125">-Name</span></span>
<span data-ttu-id="54fae-126">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="54fae-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="54fae-127">-Path</span><span class="sxs-lookup"><span data-stu-id="54fae-127">-Path</span></span>
<span data-ttu-id="54fae-128">Base-64. путь к файлу, который является файлом сертификата X509. cer или. PEM.</span><span class="sxs-lookup"><span data-stu-id="54fae-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="54fae-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fae-129">-ResourceGroupName</span></span>
<span data-ttu-id="54fae-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="54fae-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="54fae-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54fae-131">-ResourceId</span></span>
<span data-ttu-id="54fae-132">Идентификатор ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="54fae-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="54fae-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54fae-133">-Confirm</span></span>
<span data-ttu-id="54fae-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54fae-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54fae-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fae-135">-WhatIf</span></span>
<span data-ttu-id="54fae-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54fae-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54fae-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54fae-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54fae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fae-138">CommonParameters</span></span>
<span data-ttu-id="54fae-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54fae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fae-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54fae-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fae-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54fae-141">INPUTS</span></span>

### <span data-ttu-id="54fae-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="54fae-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="54fae-143">System. String</span><span class="sxs-lookup"><span data-stu-id="54fae-143">System.String</span></span>

## <span data-ttu-id="54fae-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54fae-144">OUTPUTS</span></span>

### <span data-ttu-id="54fae-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="54fae-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="54fae-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="54fae-146">NOTES</span></span>

## <span data-ttu-id="54fae-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54fae-147">RELATED LINKS</span></span>
