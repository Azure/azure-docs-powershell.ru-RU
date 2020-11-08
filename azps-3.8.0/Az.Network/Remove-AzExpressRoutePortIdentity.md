---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074050"
---
# <span data-ttu-id="f2be5-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="f2be5-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="f2be5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2be5-102">SYNOPSIS</span></span>
<span data-ttu-id="f2be5-103">Удаляет удостоверение из ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f2be5-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="f2be5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2be5-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2be5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2be5-105">DESCRIPTION</span></span>
<span data-ttu-id="f2be5-106">Командлет **Remove-AzExpressRoutePortIdentity** удаляет удостоверение из локального объекта Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f2be5-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="f2be5-107">С помощью **Remove-AzExpressRoutePort** удалите его из ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f2be5-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="f2be5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2be5-108">EXAMPLES</span></span>

### <span data-ttu-id="f2be5-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f2be5-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="f2be5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2be5-110">PARAMETERS</span></span>

### <span data-ttu-id="f2be5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2be5-111">-DefaultProfile</span></span>
<span data-ttu-id="f2be5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2be5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2be5-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f2be5-113">-ExpressRoutePort</span></span>
<span data-ttu-id="f2be5-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f2be5-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2be5-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2be5-115">-Confirm</span></span>
<span data-ttu-id="f2be5-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2be5-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2be5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2be5-117">-WhatIf</span></span>
<span data-ttu-id="f2be5-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2be5-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2be5-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2be5-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2be5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2be5-120">CommonParameters</span></span>
<span data-ttu-id="f2be5-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2be5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2be5-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2be5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="f2be5-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2be5-123">INPUTS</span></span>

### <span data-ttu-id="f2be5-124">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f2be5-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="f2be5-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2be5-125">OUTPUTS</span></span>

### <span data-ttu-id="f2be5-126">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f2be5-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="f2be5-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2be5-127">NOTES</span></span>

## <span data-ttu-id="f2be5-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2be5-128">RELATED LINKS</span></span>
[<span data-ttu-id="f2be5-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="f2be5-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="f2be5-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="f2be5-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="f2be5-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="f2be5-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
