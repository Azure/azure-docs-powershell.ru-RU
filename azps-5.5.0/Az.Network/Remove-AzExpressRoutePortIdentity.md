---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218369"
---
# <span data-ttu-id="b218b-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b218b-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="b218b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b218b-102">SYNOPSIS</span></span>
<span data-ttu-id="b218b-103">Удаляет удостоверение из ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b218b-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="b218b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b218b-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b218b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b218b-105">DESCRIPTION</span></span>
<span data-ttu-id="b218b-106">С **его использованием** можно удалить удостоверение из локального объекта Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b218b-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="b218b-107">Используйте **remove-AzExpressRoutePort,** чтобы удалить его из ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b218b-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="b218b-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b218b-108">EXAMPLES</span></span>

### <span data-ttu-id="b218b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b218b-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="b218b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b218b-110">PARAMETERS</span></span>

### <span data-ttu-id="b218b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b218b-111">-DefaultProfile</span></span>
<span data-ttu-id="b218b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b218b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b218b-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b218b-113">-ExpressRoutePort</span></span>
<span data-ttu-id="b218b-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b218b-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="b218b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b218b-115">-Confirm</span></span>
<span data-ttu-id="b218b-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b218b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b218b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b218b-117">-WhatIf</span></span>
<span data-ttu-id="b218b-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b218b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b218b-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b218b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b218b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b218b-120">CommonParameters</span></span>
<span data-ttu-id="b218b-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b218b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b218b-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b218b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="b218b-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b218b-123">INPUTS</span></span>

### <span data-ttu-id="b218b-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b218b-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="b218b-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b218b-125">OUTPUTS</span></span>

### <span data-ttu-id="b218b-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b218b-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="b218b-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b218b-127">NOTES</span></span>

## <span data-ttu-id="b218b-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b218b-128">RELATED LINKS</span></span>
[<span data-ttu-id="b218b-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b218b-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="b218b-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b218b-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="b218b-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="b218b-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
