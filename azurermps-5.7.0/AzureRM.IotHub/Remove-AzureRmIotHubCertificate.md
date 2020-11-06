---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
ms.openlocfilehash: cc9bc7ef4171ea59f79f6e4687dddea4bc1dbae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563487"
---
# <span data-ttu-id="63876-101">Remove-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="63876-101">Remove-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="63876-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63876-102">SYNOPSIS</span></span>
<span data-ttu-id="63876-103">Удаляет сертификат центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="63876-103">Deletes an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63876-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63876-104">SYNTAX</span></span>

### <span data-ttu-id="63876-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63876-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63876-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="63876-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63876-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="63876-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63876-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63876-108">DESCRIPTION</span></span>
<span data-ttu-id="63876-109">Подробное описание сертификатов ЦС в центре Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="63876-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="63876-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63876-110">EXAMPLES</span></span>

### <span data-ttu-id="63876-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63876-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="63876-112">Удаляет MyCertificate</span><span class="sxs-lookup"><span data-stu-id="63876-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="63876-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63876-113">PARAMETERS</span></span>

### <span data-ttu-id="63876-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="63876-114">-CertificateName</span></span>
<span data-ttu-id="63876-115">Имя сертификата</span><span class="sxs-lookup"><span data-stu-id="63876-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="63876-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63876-116">-DefaultProfile</span></span>
<span data-ttu-id="63876-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63876-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63876-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="63876-118">-Etag</span></span>
<span data-ttu-id="63876-119">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="63876-119">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63876-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63876-120">-InputObject</span></span>
<span data-ttu-id="63876-121">Объект сертификата</span><span class="sxs-lookup"><span data-stu-id="63876-121">Certificate Object</span></span>

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

### <span data-ttu-id="63876-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63876-122">-Name</span></span>
<span data-ttu-id="63876-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="63876-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="63876-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63876-124">-PassThru</span></span>
<span data-ttu-id="63876-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="63876-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63876-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63876-126">-ResourceGroupName</span></span>
<span data-ttu-id="63876-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="63876-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="63876-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63876-128">-ResourceId</span></span>
<span data-ttu-id="63876-129">Идентификатор ресурса сертификата</span><span class="sxs-lookup"><span data-stu-id="63876-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="63876-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63876-130">-Confirm</span></span>
<span data-ttu-id="63876-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63876-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63876-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63876-132">-WhatIf</span></span>
<span data-ttu-id="63876-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63876-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63876-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63876-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63876-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63876-135">CommonParameters</span></span>
<span data-ttu-id="63876-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63876-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63876-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63876-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63876-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63876-138">INPUTS</span></span>

### <span data-ttu-id="63876-139">System. String</span><span class="sxs-lookup"><span data-stu-id="63876-139">System.String</span></span>

## <span data-ttu-id="63876-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63876-140">OUTPUTS</span></span>

### <span data-ttu-id="63876-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="63876-141">System.Boolean</span></span>

## <span data-ttu-id="63876-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="63876-142">NOTES</span></span>

## <span data-ttu-id="63876-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63876-143">RELATED LINKS</span></span>

