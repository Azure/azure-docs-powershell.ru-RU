---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 3e30b7aa3d1e43844fc1fe53e860ee8b8c66f385
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078242"
---
# <span data-ttu-id="a5252-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="a5252-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="a5252-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5252-102">SYNOPSIS</span></span>
<span data-ttu-id="a5252-103">Удаляет сертификат центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="a5252-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="a5252-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5252-104">SYNTAX</span></span>

### <span data-ttu-id="a5252-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5252-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5252-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a5252-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5252-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a5252-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5252-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5252-108">DESCRIPTION</span></span>
<span data-ttu-id="a5252-109">Подробное описание сертификатов ЦС в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="a5252-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="a5252-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5252-110">EXAMPLES</span></span>

### <span data-ttu-id="a5252-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a5252-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="a5252-112">Удаляет MyCertificate</span><span class="sxs-lookup"><span data-stu-id="a5252-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="a5252-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5252-113">PARAMETERS</span></span>

### <span data-ttu-id="a5252-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a5252-114">-CertificateName</span></span>
<span data-ttu-id="a5252-115">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="a5252-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="a5252-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5252-116">-DefaultProfile</span></span>
<span data-ttu-id="a5252-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5252-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5252-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="a5252-118">-Etag</span></span>
<span data-ttu-id="a5252-119">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="a5252-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="a5252-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5252-120">-InputObject</span></span>
<span data-ttu-id="a5252-121">Объект сертификата</span><span class="sxs-lookup"><span data-stu-id="a5252-121">Certificate Object</span></span>

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

### <span data-ttu-id="a5252-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a5252-122">-Name</span></span>
<span data-ttu-id="a5252-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="a5252-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a5252-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5252-124">-PassThru</span></span>
<span data-ttu-id="a5252-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="a5252-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a5252-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5252-126">-ResourceGroupName</span></span>
<span data-ttu-id="a5252-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a5252-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a5252-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5252-128">-ResourceId</span></span>
<span data-ttu-id="a5252-129">Идентификатор ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="a5252-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="a5252-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5252-130">-Confirm</span></span>
<span data-ttu-id="a5252-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a5252-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5252-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5252-132">-WhatIf</span></span>
<span data-ttu-id="a5252-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a5252-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5252-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a5252-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5252-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5252-135">CommonParameters</span></span>
<span data-ttu-id="a5252-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5252-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5252-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5252-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5252-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5252-138">INPUTS</span></span>

### <span data-ttu-id="a5252-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="a5252-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="a5252-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a5252-140">System.String</span></span>

## <span data-ttu-id="a5252-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5252-141">OUTPUTS</span></span>

### <span data-ttu-id="a5252-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5252-142">System.Boolean</span></span>

## <span data-ttu-id="a5252-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5252-143">NOTES</span></span>

## <span data-ttu-id="a5252-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5252-144">RELATED LINKS</span></span>
