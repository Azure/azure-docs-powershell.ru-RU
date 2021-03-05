---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 7796dae8d9eac66c3dd5b8fa22ed92c2c3c0b232
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997954"
---
# <span data-ttu-id="595bb-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="595bb-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="595bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="595bb-102">SYNOPSIS</span></span>
<span data-ttu-id="595bb-103">Создание и обновление сертификата Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="595bb-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="595bb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="595bb-104">SYNTAX</span></span>

### <span data-ttu-id="595bb-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="595bb-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="595bb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="595bb-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="595bb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="595bb-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="595bb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="595bb-108">DESCRIPTION</span></span>
<span data-ttu-id="595bb-109">Отправка нового сертификата или замена существующего сертификата таким же именем.</span><span class="sxs-lookup"><span data-stu-id="595bb-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="595bb-110">Подробное описание сертификатов ЦС в Azure IoT Hub см. в https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="595bb-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="595bb-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="595bb-111">EXAMPLES</span></span>

### <span data-ttu-id="595bb-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="595bb-112">Example 1</span></span>
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

<span data-ttu-id="595bb-113">Отправка cer-файла сертификата ЦС в центр IoT.</span><span class="sxs-lookup"><span data-stu-id="595bb-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="595bb-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="595bb-114">Example 2</span></span>
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

<span data-ttu-id="595bb-115">Обновляет сертификат ЦС в центре IoT путем отправки нового файла CER.</span><span class="sxs-lookup"><span data-stu-id="595bb-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="595bb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="595bb-116">PARAMETERS</span></span>

### <span data-ttu-id="595bb-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="595bb-117">-CertificateName</span></span>
<span data-ttu-id="595bb-118">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="595bb-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="595bb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="595bb-119">-DefaultProfile</span></span>
<span data-ttu-id="595bb-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="595bb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="595bb-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="595bb-121">-Etag</span></span>
<span data-ttu-id="595bb-122">Etag of the Certificate</span><span class="sxs-lookup"><span data-stu-id="595bb-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="595bb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="595bb-123">-InputObject</span></span>
<span data-ttu-id="595bb-124">Объект Certificate</span><span class="sxs-lookup"><span data-stu-id="595bb-124">Certificate Object</span></span>

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

### <span data-ttu-id="595bb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="595bb-125">-Name</span></span>
<span data-ttu-id="595bb-126">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="595bb-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="595bb-127">-Path</span><span class="sxs-lookup"><span data-stu-id="595bb-127">-Path</span></span>
<span data-ttu-id="595bb-128">Представление файла сертификата X509 (CER- или PEM-файла) base-64.</span><span class="sxs-lookup"><span data-stu-id="595bb-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="595bb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="595bb-129">-ResourceGroupName</span></span>
<span data-ttu-id="595bb-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="595bb-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="595bb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="595bb-131">-ResourceId</span></span>
<span data-ttu-id="595bb-132">ИД ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="595bb-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="595bb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="595bb-133">-Confirm</span></span>
<span data-ttu-id="595bb-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="595bb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="595bb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="595bb-135">-WhatIf</span></span>
<span data-ttu-id="595bb-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="595bb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="595bb-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="595bb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="595bb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595bb-138">CommonParameters</span></span>
<span data-ttu-id="595bb-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="595bb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595bb-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="595bb-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595bb-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="595bb-141">INPUTS</span></span>

### <span data-ttu-id="595bb-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="595bb-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="595bb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="595bb-143">System.String</span></span>

## <span data-ttu-id="595bb-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="595bb-144">OUTPUTS</span></span>

### <span data-ttu-id="595bb-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="595bb-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="595bb-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="595bb-146">NOTES</span></span>

## <span data-ttu-id="595bb-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="595bb-147">RELATED LINKS</span></span>
