---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 4270f7c9781ef960cdbb20a8a067a3dc22255723
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996862"
---
# <span data-ttu-id="80ca9-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ca9-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="80ca9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="80ca9-103">Обновляет конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="80ca9-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="80ca9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="80ca9-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80ca9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80ca9-105">DESCRIPTION</span></span>
<span data-ttu-id="80ca9-106">Для обновления конечной точки сети доставки содержимого (CDN) Azure обновляется **cmdnEndpoint Set-AzCdnEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="80ca9-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="80ca9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="80ca9-107">EXAMPLES</span></span>

## <span data-ttu-id="80ca9-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80ca9-108">PARAMETERS</span></span>

### <span data-ttu-id="80ca9-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ca9-109">-CdnEndpoint</span></span>
<span data-ttu-id="80ca9-110">Указывает конечную точку, обновляемую этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80ca9-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="80ca9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ca9-111">-DefaultProfile</span></span>
<span data-ttu-id="80ca9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="80ca9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80ca9-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80ca9-113">-Confirm</span></span>
<span data-ttu-id="80ca9-114">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80ca9-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80ca9-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80ca9-115">-WhatIf</span></span>
<span data-ttu-id="80ca9-116">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80ca9-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80ca9-117">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="80ca9-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80ca9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ca9-118">CommonParameters</span></span>
<span data-ttu-id="80ca9-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80ca9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ca9-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80ca9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ca9-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80ca9-121">INPUTS</span></span>

### <span data-ttu-id="80ca9-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ca9-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="80ca9-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="80ca9-123">OUTPUTS</span></span>

### <span data-ttu-id="80ca9-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ca9-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="80ca9-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="80ca9-125">NOTES</span></span>

## <span data-ttu-id="80ca9-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80ca9-126">RELATED LINKS</span></span>

[<span data-ttu-id="80ca9-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ca9-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="80ca9-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ca9-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="80ca9-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ca9-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="80ca9-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ca9-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="80ca9-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="80ca9-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


