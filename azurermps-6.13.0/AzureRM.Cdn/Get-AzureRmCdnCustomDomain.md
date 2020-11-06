---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e0c1d2e49cce4798499506352811d1e341bf47e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568963"
---
# <span data-ttu-id="6c0d3-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6c0d3-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="6c0d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c0d3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0d3-103">Получает настраиваемый домен CDN.</span><span class="sxs-lookup"><span data-stu-id="6c0d3-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c0d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c0d3-104">SYNTAX</span></span>

### <span data-ttu-id="6c0d3-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c0d3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c0d3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c0d3-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c0d3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c0d3-107">DESCRIPTION</span></span>
<span data-ttu-id="6c0d3-108">Командлет **Get-AzureRmCdnCustomDomain** получает настраиваемый домен сети доставки содержимого (CDN) для Azure и связанные с ним параметры.</span><span class="sxs-lookup"><span data-stu-id="6c0d3-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="6c0d3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c0d3-109">EXAMPLES</span></span>

## <span data-ttu-id="6c0d3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c0d3-110">PARAMETERS</span></span>

### <span data-ttu-id="6c0d3-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c0d3-111">-CdnEndpoint</span></span>
<span data-ttu-id="6c0d3-112">Указывает объект конечной точки CDN, членом которого является настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="6c0d3-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c0d3-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="6c0d3-113">-CustomDomainName</span></span>
<span data-ttu-id="6c0d3-114">Указывает имя настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="6c0d3-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="6c0d3-115">Имя настраиваемого домена отличается от имени узла настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="6c0d3-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="6c0d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0d3-116">-DefaultProfile</span></span>
<span data-ttu-id="6c0d3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6c0d3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c0d3-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6c0d3-118">-EndpointName</span></span>
<span data-ttu-id="6c0d3-119">Указывает имя конечной точки, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="6c0d3-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0d3-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="6c0d3-120">-ProfileName</span></span>
<span data-ttu-id="6c0d3-121">Указывает имя профиля, которому принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="6c0d3-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0d3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c0d3-122">-ResourceGroupName</span></span>
<span data-ttu-id="6c0d3-123">Указывает имя группы ресурсов, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="6c0d3-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0d3-124">CommonParameters</span></span>
<span data-ttu-id="6c0d3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c0d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0d3-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c0d3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0d3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c0d3-127">INPUTS</span></span>

### <span data-ttu-id="6c0d3-128">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c0d3-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="6c0d3-129">Параметры: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c0d3-129">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="6c0d3-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c0d3-130">OUTPUTS</span></span>

### <span data-ttu-id="6c0d3-131">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6c0d3-131">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="6c0d3-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c0d3-132">NOTES</span></span>

## <span data-ttu-id="6c0d3-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c0d3-133">RELATED LINKS</span></span>

[<span data-ttu-id="6c0d3-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6c0d3-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="6c0d3-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6c0d3-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


