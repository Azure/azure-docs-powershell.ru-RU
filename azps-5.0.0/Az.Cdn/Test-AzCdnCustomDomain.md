---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249210"
---
# <span data-ttu-id="74c7e-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="74c7e-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="74c7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="74c7e-103">Проверяет, можно ли добавить в конечную точку настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="74c7e-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="74c7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74c7e-104">SYNTAX</span></span>

### <span data-ttu-id="74c7e-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74c7e-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74c7e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74c7e-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74c7e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74c7e-107">DESCRIPTION</span></span>
<span data-ttu-id="74c7e-108">Командлет **Test-AzCdnCustomDomain** проверяет, можно ли добавить настраиваемый домен в конечную точку, проверив сопоставление CNAME.</span><span class="sxs-lookup"><span data-stu-id="74c7e-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="74c7e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74c7e-109">EXAMPLES</span></span>

## <span data-ttu-id="74c7e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74c7e-110">PARAMETERS</span></span>

### <span data-ttu-id="74c7e-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="74c7e-111">-CdnEndpoint</span></span>
<span data-ttu-id="74c7e-112">Задает конечную точку, в которую вы хотите добавить настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="74c7e-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="74c7e-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="74c7e-113">-CustomDomainHostName</span></span>
<span data-ttu-id="74c7e-114">Указывает имя узла для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="74c7e-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="74c7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c7e-115">-DefaultProfile</span></span>
<span data-ttu-id="74c7e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="74c7e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74c7e-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="74c7e-117">-EndpointName</span></span>
<span data-ttu-id="74c7e-118">Указывает имя конечной точки, в которую вы хотите добавить настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="74c7e-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="74c7e-119">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="74c7e-119">-ProfileName</span></span>
<span data-ttu-id="74c7e-120">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="74c7e-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="74c7e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c7e-121">-ResourceGroupName</span></span>
<span data-ttu-id="74c7e-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74c7e-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="74c7e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c7e-123">CommonParameters</span></span>
<span data-ttu-id="74c7e-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74c7e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c7e-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74c7e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c7e-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74c7e-126">INPUTS</span></span>

### <span data-ttu-id="74c7e-127">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="74c7e-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="74c7e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74c7e-128">OUTPUTS</span></span>

### <span data-ttu-id="74c7e-129">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="74c7e-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="74c7e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="74c7e-130">NOTES</span></span>

## <span data-ttu-id="74c7e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74c7e-131">RELATED LINKS</span></span>

[<span data-ttu-id="74c7e-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="74c7e-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="74c7e-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="74c7e-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="74c7e-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="74c7e-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


