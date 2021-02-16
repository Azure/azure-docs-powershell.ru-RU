---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229209"
---
# <span data-ttu-id="78e92-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78e92-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="78e92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78e92-102">SYNOPSIS</span></span>
<span data-ttu-id="78e92-103">Проверяет, можно ли добавить настраиваемый домен на конечную точку.</span><span class="sxs-lookup"><span data-stu-id="78e92-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="78e92-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78e92-104">SYNTAX</span></span>

### <span data-ttu-id="78e92-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78e92-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78e92-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e92-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78e92-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78e92-107">DESCRIPTION</span></span>
<span data-ttu-id="78e92-108">С **помощью cmdlet Test-AzCdnCustomDomain** можно ли добавить настраиваемый домен на конечную точку, проверив сопоставление CName.</span><span class="sxs-lookup"><span data-stu-id="78e92-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="78e92-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78e92-109">EXAMPLES</span></span>

## <span data-ttu-id="78e92-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78e92-110">PARAMETERS</span></span>

### <span data-ttu-id="78e92-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="78e92-111">-CdnEndpoint</span></span>
<span data-ttu-id="78e92-112">Указывает конечную точку, в которую вы хотите добавить настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="78e92-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="78e92-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="78e92-113">-CustomDomainHostName</span></span>
<span data-ttu-id="78e92-114">Указывает имя хоста пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="78e92-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="78e92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e92-115">-DefaultProfile</span></span>
<span data-ttu-id="78e92-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="78e92-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78e92-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="78e92-117">-EndpointName</span></span>
<span data-ttu-id="78e92-118">Указывает имя конечной точки, к которой вы хотите добавить настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="78e92-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="78e92-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="78e92-119">-ProfileName</span></span>
<span data-ttu-id="78e92-120">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="78e92-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="78e92-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e92-121">-ResourceGroupName</span></span>
<span data-ttu-id="78e92-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78e92-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="78e92-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e92-123">CommonParameters</span></span>
<span data-ttu-id="78e92-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78e92-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e92-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78e92-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e92-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78e92-126">INPUTS</span></span>

### <span data-ttu-id="78e92-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="78e92-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="78e92-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78e92-128">OUTPUTS</span></span>

### <span data-ttu-id="78e92-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="78e92-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="78e92-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78e92-130">NOTES</span></span>

## <span data-ttu-id="78e92-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78e92-131">RELATED LINKS</span></span>

[<span data-ttu-id="78e92-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78e92-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="78e92-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78e92-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="78e92-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="78e92-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


