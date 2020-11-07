---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: cafc38503bd7978d1214fe8f3c78e4fd1f4a3e7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900314"
---
# <span data-ttu-id="40830-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="40830-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="40830-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40830-102">SYNOPSIS</span></span>
<span data-ttu-id="40830-103">Удаляет сертификат центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="40830-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="40830-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40830-104">SYNTAX</span></span>

### <span data-ttu-id="40830-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40830-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40830-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="40830-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40830-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="40830-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40830-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40830-108">DESCRIPTION</span></span>
<span data-ttu-id="40830-109">Подробное описание сертификатов ЦС в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="40830-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="40830-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40830-110">EXAMPLES</span></span>

### <span data-ttu-id="40830-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40830-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="40830-112">Удаляет MyCertificate</span><span class="sxs-lookup"><span data-stu-id="40830-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="40830-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40830-113">PARAMETERS</span></span>

### <span data-ttu-id="40830-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="40830-114">-CertificateName</span></span>
<span data-ttu-id="40830-115">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="40830-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="40830-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40830-116">-DefaultProfile</span></span>
<span data-ttu-id="40830-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40830-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40830-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="40830-118">-Etag</span></span>
<span data-ttu-id="40830-119">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="40830-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="40830-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40830-120">-InputObject</span></span>
<span data-ttu-id="40830-121">Объект сертификата</span><span class="sxs-lookup"><span data-stu-id="40830-121">Certificate Object</span></span>

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

### <span data-ttu-id="40830-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40830-122">-Name</span></span>
<span data-ttu-id="40830-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="40830-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="40830-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40830-124">-PassThru</span></span>
<span data-ttu-id="40830-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="40830-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="40830-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40830-126">-ResourceGroupName</span></span>
<span data-ttu-id="40830-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="40830-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="40830-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40830-128">-ResourceId</span></span>
<span data-ttu-id="40830-129">Идентификатор ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="40830-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="40830-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40830-130">-Confirm</span></span>
<span data-ttu-id="40830-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40830-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40830-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40830-132">-WhatIf</span></span>
<span data-ttu-id="40830-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40830-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40830-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40830-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40830-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40830-135">CommonParameters</span></span>
<span data-ttu-id="40830-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40830-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40830-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40830-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40830-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40830-138">INPUTS</span></span>

### <span data-ttu-id="40830-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="40830-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="40830-140">System. String</span><span class="sxs-lookup"><span data-stu-id="40830-140">System.String</span></span>

## <span data-ttu-id="40830-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40830-141">OUTPUTS</span></span>

### <span data-ttu-id="40830-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40830-142">System.Boolean</span></span>

## <span data-ttu-id="40830-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="40830-143">NOTES</span></span>

## <span data-ttu-id="40830-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40830-144">RELATED LINKS</span></span>
