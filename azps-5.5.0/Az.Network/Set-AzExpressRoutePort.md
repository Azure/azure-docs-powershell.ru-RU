---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: 2365729f3960e3652e2b4c0709ca14092fea3264
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240584"
---
# <span data-ttu-id="c9475-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c9475-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="c9475-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9475-102">SYNOPSIS</span></span>
<span data-ttu-id="c9475-103">Изменяет ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c9475-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="c9475-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c9475-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9475-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9475-105">DESCRIPTION</span></span>
<span data-ttu-id="c9475-106">С **его использованием** можно сохранить измененный expressRoutePort в Azure.</span><span class="sxs-lookup"><span data-stu-id="c9475-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="c9475-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c9475-107">EXAMPLES</span></span>

### <span data-ttu-id="c9475-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c9475-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="c9475-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c9475-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="c9475-110">Изменяет состояние администрирования ссылки ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c9475-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="c9475-111">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c9475-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="c9475-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9475-112">PARAMETERS</span></span>

### <span data-ttu-id="c9475-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9475-113">-AsJob</span></span>
<span data-ttu-id="c9475-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c9475-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9475-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9475-115">-DefaultProfile</span></span>
<span data-ttu-id="c9475-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9475-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9475-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c9475-117">-ExpressRoutePort</span></span>
<span data-ttu-id="c9475-118">Объект ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c9475-118">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9475-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9475-119">-Confirm</span></span>
<span data-ttu-id="c9475-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9475-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9475-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9475-121">-WhatIf</span></span>
<span data-ttu-id="c9475-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9475-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9475-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c9475-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9475-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9475-124">CommonParameters</span></span>
<span data-ttu-id="c9475-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9475-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9475-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9475-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9475-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9475-127">INPUTS</span></span>

### <span data-ttu-id="c9475-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c9475-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c9475-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c9475-129">OUTPUTS</span></span>

### <span data-ttu-id="c9475-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c9475-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c9475-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c9475-131">NOTES</span></span>

## <span data-ttu-id="c9475-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9475-132">RELATED LINKS</span></span>

[<span data-ttu-id="c9475-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c9475-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="c9475-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c9475-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="c9475-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c9475-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
