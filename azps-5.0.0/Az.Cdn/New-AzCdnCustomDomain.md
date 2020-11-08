---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 6a0a90657ee76401117971a29dc03a78a7330afc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249526"
---
# <span data-ttu-id="d8628-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d8628-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="d8628-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8628-102">SYNOPSIS</span></span>
<span data-ttu-id="d8628-103">Создание настраиваемого домена для конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="d8628-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="d8628-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8628-104">SYNTAX</span></span>

### <span data-ttu-id="d8628-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8628-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8628-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8628-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8628-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8628-107">DESCRIPTION</span></span>
<span data-ttu-id="d8628-108">Командлет **New-AzCdnCustomDomain** создает настраиваемый домен для конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="d8628-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d8628-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8628-109">EXAMPLES</span></span>

## <span data-ttu-id="d8628-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8628-110">PARAMETERS</span></span>

### <span data-ttu-id="d8628-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8628-111">-CdnEndpoint</span></span>
<span data-ttu-id="d8628-112">Указывает объект конечной точки сети CDN, в который добавляется настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="d8628-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="d8628-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d8628-113">-CustomDomainName</span></span>
<span data-ttu-id="d8628-114">Указывает имя ресурса для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="d8628-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="d8628-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8628-115">-DefaultProfile</span></span>
<span data-ttu-id="d8628-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d8628-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8628-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d8628-117">-EndpointName</span></span>
<span data-ttu-id="d8628-118">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d8628-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="d8628-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="d8628-119">-HostName</span></span>
<span data-ttu-id="d8628-120">Указывает имя узла для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="d8628-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="d8628-121">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="d8628-121">-ProfileName</span></span>
<span data-ttu-id="d8628-122">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="d8628-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="d8628-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8628-123">-ResourceGroupName</span></span>
<span data-ttu-id="d8628-124">Указывает имя группы ресурсов, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="d8628-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="d8628-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8628-125">-Confirm</span></span>
<span data-ttu-id="d8628-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8628-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8628-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8628-127">-WhatIf</span></span>
<span data-ttu-id="d8628-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8628-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8628-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8628-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8628-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8628-130">CommonParameters</span></span>
<span data-ttu-id="d8628-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8628-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8628-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8628-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8628-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8628-133">INPUTS</span></span>

### <span data-ttu-id="d8628-134">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8628-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="d8628-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8628-135">OUTPUTS</span></span>

### <span data-ttu-id="d8628-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d8628-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="d8628-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8628-137">NOTES</span></span>

## <span data-ttu-id="d8628-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8628-138">RELATED LINKS</span></span>

[<span data-ttu-id="d8628-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d8628-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="d8628-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d8628-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="d8628-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d8628-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


