---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405524"
---
# <span data-ttu-id="ae9d6-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ae9d6-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="ae9d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae9d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ae9d6-103">Возвращает настраиваемый домен CDN.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="ae9d6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ae9d6-104">SYNTAX</span></span>

### <span data-ttu-id="ae9d6-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae9d6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9d6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae9d6-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae9d6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae9d6-107">DESCRIPTION</span></span>
<span data-ttu-id="ae9d6-108">**Cmdlet Get-AzCdnCustomDomain** получает настраиваемый домен сети доставки содержимого (CDN) Azure и связанные с ним параметры.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="ae9d6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ae9d6-109">EXAMPLES</span></span>

## <span data-ttu-id="ae9d6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae9d6-110">PARAMETERS</span></span>

### <span data-ttu-id="ae9d6-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae9d6-111">-CdnEndpoint</span></span>
<span data-ttu-id="ae9d6-112">Определяет объект конечной точки CDN, к которому является настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="ae9d6-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ae9d6-113">-CustomDomainName</span></span>
<span data-ttu-id="ae9d6-114">Указывает имя пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="ae9d6-115">Имя пользовательского домена отличается от имени его хоста.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="ae9d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae9d6-116">-DefaultProfile</span></span>
<span data-ttu-id="ae9d6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ae9d6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae9d6-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ae9d6-118">-EndpointName</span></span>
<span data-ttu-id="ae9d6-119">Указывает имя конечной точки, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ae9d6-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ae9d6-120">-ProfileName</span></span>
<span data-ttu-id="ae9d6-121">Имя профиля, к которому принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ae9d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae9d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae9d6-123">Имя группы ресурсов, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ae9d6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae9d6-124">CommonParameters</span></span>
<span data-ttu-id="ae9d6-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae9d6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae9d6-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae9d6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae9d6-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae9d6-127">INPUTS</span></span>

### <span data-ttu-id="ae9d6-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ae9d6-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="ae9d6-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae9d6-129">OUTPUTS</span></span>

### <span data-ttu-id="ae9d6-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ae9d6-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="ae9d6-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ae9d6-131">NOTES</span></span>

## <span data-ttu-id="ae9d6-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae9d6-132">RELATED LINKS</span></span>

[<span data-ttu-id="ae9d6-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ae9d6-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="ae9d6-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ae9d6-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


