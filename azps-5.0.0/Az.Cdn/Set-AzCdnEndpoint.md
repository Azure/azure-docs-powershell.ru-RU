---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 7222b33470dc1fff22039c5e88bf3c6560b80c31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247647"
---
# <span data-ttu-id="c9982-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9982-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="c9982-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9982-102">SYNOPSIS</span></span>
<span data-ttu-id="c9982-103">Обновляет конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="c9982-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="c9982-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9982-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9982-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9982-105">DESCRIPTION</span></span>
<span data-ttu-id="c9982-106">Командлет **Set-AzCdnEndpoint** обновляет конечную точку сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="c9982-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="c9982-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9982-107">EXAMPLES</span></span>

## <span data-ttu-id="c9982-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9982-108">PARAMETERS</span></span>

### <span data-ttu-id="c9982-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9982-109">-CdnEndpoint</span></span>
<span data-ttu-id="c9982-110">Указывает конечную точку, которую обновляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c9982-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9982-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9982-111">-DefaultProfile</span></span>
<span data-ttu-id="c9982-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c9982-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9982-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9982-113">-Confirm</span></span>
<span data-ttu-id="c9982-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9982-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9982-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9982-115">-WhatIf</span></span>
<span data-ttu-id="c9982-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9982-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9982-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9982-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9982-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9982-118">CommonParameters</span></span>
<span data-ttu-id="c9982-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9982-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9982-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9982-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9982-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9982-121">INPUTS</span></span>

### <span data-ttu-id="c9982-122">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9982-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c9982-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9982-123">OUTPUTS</span></span>

### <span data-ttu-id="c9982-124">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9982-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c9982-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9982-125">NOTES</span></span>

## <span data-ttu-id="c9982-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9982-126">RELATED LINKS</span></span>

[<span data-ttu-id="c9982-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9982-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="c9982-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9982-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="c9982-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9982-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="c9982-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9982-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="c9982-131">Остановить-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c9982-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


