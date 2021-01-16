---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 3e30b7aa3d1e43844fc1fe53e860ee8b8c66f385
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426071"
---
# <span data-ttu-id="ed3d5-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="ed3d5-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="ed3d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed3d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3d5-103">Удаляет сертификат Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="ed3d5-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="ed3d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed3d5-104">SYNTAX</span></span>

### <span data-ttu-id="ed3d5-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed3d5-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed3d5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ed3d5-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed3d5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ed3d5-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed3d5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed3d5-108">DESCRIPTION</span></span>
<span data-ttu-id="ed3d5-109">Подробное описание сертификатов ЦС в Azure IoT Hub см. в https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="ed3d5-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="ed3d5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed3d5-110">EXAMPLES</span></span>

### <span data-ttu-id="ed3d5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed3d5-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="ed3d5-112">Deletes MyCertificate</span><span class="sxs-lookup"><span data-stu-id="ed3d5-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="ed3d5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed3d5-113">PARAMETERS</span></span>

### <span data-ttu-id="ed3d5-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ed3d5-114">-CertificateName</span></span>
<span data-ttu-id="ed3d5-115">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="ed3d5-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="ed3d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed3d5-116">-DefaultProfile</span></span>
<span data-ttu-id="ed3d5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed3d5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed3d5-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="ed3d5-118">-Etag</span></span>
<span data-ttu-id="ed3d5-119">Etag of the Certificate</span><span class="sxs-lookup"><span data-stu-id="ed3d5-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="ed3d5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed3d5-120">-InputObject</span></span>
<span data-ttu-id="ed3d5-121">Объект Certificate</span><span class="sxs-lookup"><span data-stu-id="ed3d5-121">Certificate Object</span></span>

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

### <span data-ttu-id="ed3d5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ed3d5-122">-Name</span></span>
<span data-ttu-id="ed3d5-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="ed3d5-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ed3d5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed3d5-124">-PassThru</span></span>
<span data-ttu-id="ed3d5-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ed3d5-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed3d5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed3d5-126">-ResourceGroupName</span></span>
<span data-ttu-id="ed3d5-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ed3d5-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ed3d5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed3d5-128">-ResourceId</span></span>
<span data-ttu-id="ed3d5-129">ИД ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="ed3d5-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="ed3d5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed3d5-130">-Confirm</span></span>
<span data-ttu-id="ed3d5-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed3d5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed3d5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed3d5-132">-WhatIf</span></span>
<span data-ttu-id="ed3d5-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed3d5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed3d5-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ed3d5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed3d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3d5-135">CommonParameters</span></span>
<span data-ttu-id="ed3d5-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed3d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3d5-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed3d5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3d5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed3d5-138">INPUTS</span></span>

### <span data-ttu-id="ed3d5-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="ed3d5-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="ed3d5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ed3d5-140">System.String</span></span>

## <span data-ttu-id="ed3d5-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed3d5-141">OUTPUTS</span></span>

### <span data-ttu-id="ed3d5-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed3d5-142">System.Boolean</span></span>

## <span data-ttu-id="ed3d5-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed3d5-143">NOTES</span></span>

## <span data-ttu-id="ed3d5-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed3d5-144">RELATED LINKS</span></span>
