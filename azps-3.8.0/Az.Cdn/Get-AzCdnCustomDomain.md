---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065273"
---
# <span data-ttu-id="324f7-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="324f7-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="324f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="324f7-102">SYNOPSIS</span></span>
<span data-ttu-id="324f7-103">Получает настраиваемый домен CDN.</span><span class="sxs-lookup"><span data-stu-id="324f7-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="324f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="324f7-104">SYNTAX</span></span>

### <span data-ttu-id="324f7-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="324f7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="324f7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="324f7-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="324f7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="324f7-107">DESCRIPTION</span></span>
<span data-ttu-id="324f7-108">Командлет **Get-AzCdnCustomDomain** получает настраиваемый домен сети доставки содержимого (CDN) для Azure и связанные с ним параметры.</span><span class="sxs-lookup"><span data-stu-id="324f7-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="324f7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="324f7-109">EXAMPLES</span></span>

## <span data-ttu-id="324f7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="324f7-110">PARAMETERS</span></span>

### <span data-ttu-id="324f7-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="324f7-111">-CdnEndpoint</span></span>
<span data-ttu-id="324f7-112">Указывает объект конечной точки CDN, членом которого является настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="324f7-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="324f7-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="324f7-113">-CustomDomainName</span></span>
<span data-ttu-id="324f7-114">Указывает имя настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="324f7-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="324f7-115">Имя настраиваемого домена отличается от имени узла настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="324f7-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="324f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="324f7-116">-DefaultProfile</span></span>
<span data-ttu-id="324f7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="324f7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="324f7-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="324f7-118">-EndpointName</span></span>
<span data-ttu-id="324f7-119">Указывает имя конечной точки, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="324f7-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="324f7-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="324f7-120">-ProfileName</span></span>
<span data-ttu-id="324f7-121">Указывает имя профиля, которому принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="324f7-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="324f7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="324f7-122">-ResourceGroupName</span></span>
<span data-ttu-id="324f7-123">Указывает имя группы ресурсов, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="324f7-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="324f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="324f7-124">CommonParameters</span></span>
<span data-ttu-id="324f7-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="324f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="324f7-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="324f7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="324f7-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="324f7-127">INPUTS</span></span>

### <span data-ttu-id="324f7-128">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="324f7-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="324f7-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="324f7-129">OUTPUTS</span></span>

### <span data-ttu-id="324f7-130">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="324f7-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="324f7-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="324f7-131">NOTES</span></span>

## <span data-ttu-id="324f7-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="324f7-132">RELATED LINKS</span></span>

[<span data-ttu-id="324f7-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="324f7-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="324f7-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="324f7-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


