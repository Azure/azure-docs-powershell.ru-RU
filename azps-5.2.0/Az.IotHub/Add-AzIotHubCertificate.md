---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubCertificate.md
ms.openlocfilehash: 6d77bcc6d940c5891b4fc06875dc353af5f75939
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397095"
---
# <span data-ttu-id="6bac4-101">Add-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="6bac4-101">Add-AzIotHubCertificate</span></span>

## <span data-ttu-id="6bac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bac4-102">SYNOPSIS</span></span>
<span data-ttu-id="6bac4-103">Создание и обновление сертификата Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="6bac4-103">Create/update an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="6bac4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6bac4-104">SYNTAX</span></span>

### <span data-ttu-id="6bac4-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6bac4-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6bac4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6bac4-106">InputObjectSet</span></span>
```
Add-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bac4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6bac4-107">ResourceIdSet</span></span>
```
Add-AzIotHubCertificate [-ResourceId] <String> [-Path] <String> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bac4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bac4-108">DESCRIPTION</span></span>
<span data-ttu-id="6bac4-109">Отправка нового сертификата или замена существующего сертификата таким же именем.</span><span class="sxs-lookup"><span data-stu-id="6bac4-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="6bac4-110">Подробное описание сертификатов ЦС в Azure IoT Hub см. в https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="6bac4-110">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="6bac4-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6bac4-111">EXAMPLES</span></span>

### <span data-ttu-id="6bac4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6bac4-112">Example 1</span></span>
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

<span data-ttu-id="6bac4-113">Отправка cer-файла сертификата ЦС в центр IoT.</span><span class="sxs-lookup"><span data-stu-id="6bac4-113">Uploads a CA certificate CER file to an IoT hub.</span></span> 

### <span data-ttu-id="6bac4-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6bac4-114">Example 2</span></span>
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

<span data-ttu-id="6bac4-115">Обновляет сертификат ЦС в центре IoT путем отправки нового файла CER.</span><span class="sxs-lookup"><span data-stu-id="6bac4-115">Updates a CA certificate in an IoT hub by uploading a new CER file.</span></span> 

## <span data-ttu-id="6bac4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bac4-116">PARAMETERS</span></span>

### <span data-ttu-id="6bac4-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="6bac4-117">-CertificateName</span></span>
<span data-ttu-id="6bac4-118">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="6bac4-118">Name of the Certificate</span></span>

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

### <span data-ttu-id="6bac4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bac4-119">-DefaultProfile</span></span>
<span data-ttu-id="6bac4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6bac4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bac4-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="6bac4-121">-Etag</span></span>
<span data-ttu-id="6bac4-122">Etag of the Certificate</span><span class="sxs-lookup"><span data-stu-id="6bac4-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="6bac4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bac4-123">-InputObject</span></span>
<span data-ttu-id="6bac4-124">Объект Certificate</span><span class="sxs-lookup"><span data-stu-id="6bac4-124">Certificate Object</span></span>

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

### <span data-ttu-id="6bac4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6bac4-125">-Name</span></span>
<span data-ttu-id="6bac4-126">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="6bac4-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6bac4-127">-Path</span><span class="sxs-lookup"><span data-stu-id="6bac4-127">-Path</span></span>
<span data-ttu-id="6bac4-128">Представление файла сертификата X509 (CER- или PEM-файла) base-64.</span><span class="sxs-lookup"><span data-stu-id="6bac4-128">base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="6bac4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bac4-129">-ResourceGroupName</span></span>
<span data-ttu-id="6bac4-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6bac4-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6bac4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6bac4-131">-ResourceId</span></span>
<span data-ttu-id="6bac4-132">ИД ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="6bac4-132">Certificate Resource Id</span></span>

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

### <span data-ttu-id="6bac4-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bac4-133">-Confirm</span></span>
<span data-ttu-id="6bac4-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bac4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bac4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bac4-135">-WhatIf</span></span>
<span data-ttu-id="6bac4-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bac4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bac4-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6bac4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bac4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bac4-138">CommonParameters</span></span>
<span data-ttu-id="6bac4-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bac4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bac4-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bac4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bac4-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bac4-141">INPUTS</span></span>

### <span data-ttu-id="6bac4-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="6bac4-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="6bac4-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6bac4-143">System.String</span></span>

## <span data-ttu-id="6bac4-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6bac4-144">OUTPUTS</span></span>

### <span data-ttu-id="6bac4-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="6bac4-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="6bac4-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6bac4-146">NOTES</span></span>

## <span data-ttu-id="6bac4-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bac4-147">RELATED LINKS</span></span>
