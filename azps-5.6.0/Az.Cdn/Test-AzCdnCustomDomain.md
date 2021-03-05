---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: b2c061f7755c7891946bcf8ea8f3fa5cdb15439d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986961"
---
# <span data-ttu-id="84a37-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="84a37-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="84a37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84a37-102">SYNOPSIS</span></span>
<span data-ttu-id="84a37-103">Проверяет, можно ли добавить настраиваемый домен на конечную точку.</span><span class="sxs-lookup"><span data-stu-id="84a37-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="84a37-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="84a37-104">SYNTAX</span></span>

### <span data-ttu-id="84a37-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84a37-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84a37-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84a37-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84a37-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84a37-107">DESCRIPTION</span></span>
<span data-ttu-id="84a37-108">С **помощью cmdlet Test-AzCdnCustomDomain** можно ли добавить настраиваемый домен на конечную точку, проверив сопоставление CName.</span><span class="sxs-lookup"><span data-stu-id="84a37-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="84a37-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="84a37-109">EXAMPLES</span></span>

## <span data-ttu-id="84a37-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84a37-110">PARAMETERS</span></span>

### <span data-ttu-id="84a37-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="84a37-111">-CdnEndpoint</span></span>
<span data-ttu-id="84a37-112">Указывает конечную точку, в которую вы хотите добавить настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="84a37-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="84a37-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="84a37-113">-CustomDomainHostName</span></span>
<span data-ttu-id="84a37-114">Указывает имя хоста пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="84a37-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="84a37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a37-115">-DefaultProfile</span></span>
<span data-ttu-id="84a37-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="84a37-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84a37-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="84a37-117">-EndpointName</span></span>
<span data-ttu-id="84a37-118">Указывает имя конечной точки, к которой вы хотите добавить настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="84a37-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="84a37-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="84a37-119">-ProfileName</span></span>
<span data-ttu-id="84a37-120">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="84a37-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="84a37-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a37-121">-ResourceGroupName</span></span>
<span data-ttu-id="84a37-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84a37-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="84a37-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a37-123">CommonParameters</span></span>
<span data-ttu-id="84a37-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a37-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a37-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84a37-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a37-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84a37-126">INPUTS</span></span>

### <span data-ttu-id="84a37-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="84a37-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="84a37-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84a37-128">OUTPUTS</span></span>

### <span data-ttu-id="84a37-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="84a37-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="84a37-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="84a37-130">NOTES</span></span>

## <span data-ttu-id="84a37-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84a37-131">RELATED LINKS</span></span>

[<span data-ttu-id="84a37-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="84a37-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="84a37-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="84a37-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="84a37-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="84a37-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


