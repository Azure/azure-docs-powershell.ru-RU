---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: 3462e256889dffd086d9fa1d0fb96dba42ed109a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727614"
---
# <span data-ttu-id="d3b3f-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d3b3f-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="d3b3f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b3f-103">Получает настраиваемый домен CDN.</span><span class="sxs-lookup"><span data-stu-id="d3b3f-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="d3b3f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3b3f-104">SYNTAX</span></span>

### <span data-ttu-id="d3b3f-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3b3f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3b3f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3b3f-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3b3f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3b3f-107">DESCRIPTION</span></span>
<span data-ttu-id="d3b3f-108">Командлет **Get-AzCdnCustomDomain** получает настраиваемый домен сети доставки содержимого (CDN) для Azure и связанные с ним параметры.</span><span class="sxs-lookup"><span data-stu-id="d3b3f-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="d3b3f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3b3f-109">EXAMPLES</span></span>

## <span data-ttu-id="d3b3f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3b3f-110">PARAMETERS</span></span>

### <span data-ttu-id="d3b3f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3b3f-111">-CdnEndpoint</span></span>
<span data-ttu-id="d3b3f-112">Указывает объект конечной точки CDN, членом которого является настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="d3b3f-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="d3b3f-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d3b3f-113">-CustomDomainName</span></span>
<span data-ttu-id="d3b3f-114">Указывает имя настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="d3b3f-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="d3b3f-115">Имя настраиваемого домена отличается от имени узла настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="d3b3f-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="d3b3f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b3f-116">-DefaultProfile</span></span>
<span data-ttu-id="d3b3f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d3b3f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3b3f-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d3b3f-118">-EndpointName</span></span>
<span data-ttu-id="d3b3f-119">Указывает имя конечной точки, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="d3b3f-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="d3b3f-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="d3b3f-120">-ProfileName</span></span>
<span data-ttu-id="d3b3f-121">Указывает имя профиля, которому принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="d3b3f-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="d3b3f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3b3f-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3b3f-123">Указывает имя группы ресурсов, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="d3b3f-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="d3b3f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b3f-124">CommonParameters</span></span>
<span data-ttu-id="d3b3f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3b3f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b3f-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3b3f-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b3f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3b3f-127">INPUTS</span></span>

### <span data-ttu-id="d3b3f-128">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3b3f-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="d3b3f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3b3f-129">OUTPUTS</span></span>

### <span data-ttu-id="d3b3f-130">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d3b3f-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="d3b3f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3b3f-131">NOTES</span></span>

## <span data-ttu-id="d3b3f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3b3f-132">RELATED LINKS</span></span>

[<span data-ttu-id="d3b3f-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d3b3f-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="d3b3f-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d3b3f-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


