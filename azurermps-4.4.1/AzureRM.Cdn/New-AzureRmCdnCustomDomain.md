---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: ec15b97aa87c5e581069606a425f25b71dd495dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733403"
---
# <span data-ttu-id="6b71b-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b71b-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="6b71b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b71b-102">SYNOPSIS</span></span>
<span data-ttu-id="6b71b-103">Создание настраиваемого домена для конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="6b71b-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b71b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b71b-104">SYNTAX</span></span>

### <span data-ttu-id="6b71b-105">Параметры, заданные для параметров полей (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b71b-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b71b-106">Параметр, заданный для параметров объекта</span><span class="sxs-lookup"><span data-stu-id="6b71b-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b71b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b71b-107">DESCRIPTION</span></span>
<span data-ttu-id="6b71b-108">Командлет **New-AzureRmCdnCustomDomain** создает настраиваемый домен для конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="6b71b-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="6b71b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b71b-109">EXAMPLES</span></span>

## <span data-ttu-id="6b71b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b71b-110">PARAMETERS</span></span>

### <span data-ttu-id="6b71b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b71b-111">-CdnEndpoint</span></span>
<span data-ttu-id="6b71b-112">Указывает объект конечной точки сети CDN, в который добавляется настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="6b71b-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b71b-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="6b71b-113">-CustomDomainName</span></span>
<span data-ttu-id="6b71b-114">Указывает имя ресурса для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="6b71b-114">Specifies the resource name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b71b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6b71b-115">-EndpointName</span></span>
<span data-ttu-id="6b71b-116">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="6b71b-116">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b71b-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="6b71b-117">-HostName</span></span>
<span data-ttu-id="6b71b-118">Указывает имя узла для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="6b71b-118">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b71b-119">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="6b71b-119">-ProfileName</span></span>
<span data-ttu-id="6b71b-120">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="6b71b-120">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b71b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b71b-121">-ResourceGroupName</span></span>
<span data-ttu-id="6b71b-122">Указывает имя группы ресурсов, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="6b71b-122">Specifies the name of the resource group to which the custom domain belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b71b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b71b-123">-Confirm</span></span>
<span data-ttu-id="6b71b-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b71b-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b71b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b71b-125">-WhatIf</span></span>
<span data-ttu-id="6b71b-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b71b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b71b-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b71b-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b71b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b71b-128">-DefaultProfile</span></span>
<span data-ttu-id="6b71b-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b71b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b71b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b71b-130">CommonParameters</span></span>
<span data-ttu-id="6b71b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b71b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b71b-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b71b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b71b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b71b-133">INPUTS</span></span>

### <span data-ttu-id="6b71b-134">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6b71b-134">PSEndpoint</span></span>
<span data-ttu-id="6b71b-135">Параметр "CdnEndpoint" принимает значение типа "PSEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6b71b-135">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="6b71b-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b71b-136">OUTPUTS</span></span>

### <span data-ttu-id="6b71b-137">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b71b-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="6b71b-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b71b-138">NOTES</span></span>

## <span data-ttu-id="6b71b-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b71b-139">RELATED LINKS</span></span>

[<span data-ttu-id="6b71b-140">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b71b-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="6b71b-141">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b71b-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="6b71b-142">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6b71b-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


