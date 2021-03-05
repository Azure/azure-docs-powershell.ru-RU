---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: c431b03c4dd417638f84fe3a483bcaf9eefcb837
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963976"
---
# <span data-ttu-id="47c29-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="47c29-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="47c29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47c29-102">SYNOPSIS</span></span>
<span data-ttu-id="47c29-103">Изменяет ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="47c29-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="47c29-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47c29-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47c29-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47c29-105">DESCRIPTION</span></span>
<span data-ttu-id="47c29-106">С **его использованием** можно сохранить измененный expressRoutePort в Azure.</span><span class="sxs-lookup"><span data-stu-id="47c29-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="47c29-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47c29-107">EXAMPLES</span></span>

### <span data-ttu-id="47c29-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="47c29-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="47c29-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="47c29-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="47c29-110">Изменяет состояние администрирования ссылки ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="47c29-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="47c29-111">Пример 3</span><span class="sxs-lookup"><span data-stu-id="47c29-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="47c29-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47c29-112">PARAMETERS</span></span>

### <span data-ttu-id="47c29-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47c29-113">-AsJob</span></span>
<span data-ttu-id="47c29-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="47c29-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47c29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47c29-115">-DefaultProfile</span></span>
<span data-ttu-id="47c29-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47c29-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47c29-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="47c29-117">-ExpressRoutePort</span></span>
<span data-ttu-id="47c29-118">Объект ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="47c29-118">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="47c29-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47c29-119">-Confirm</span></span>
<span data-ttu-id="47c29-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47c29-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47c29-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47c29-121">-WhatIf</span></span>
<span data-ttu-id="47c29-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47c29-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47c29-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="47c29-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47c29-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c29-124">CommonParameters</span></span>
<span data-ttu-id="47c29-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47c29-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c29-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47c29-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c29-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47c29-127">INPUTS</span></span>

### <span data-ttu-id="47c29-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="47c29-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="47c29-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47c29-129">OUTPUTS</span></span>

### <span data-ttu-id="47c29-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="47c29-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="47c29-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47c29-131">NOTES</span></span>

## <span data-ttu-id="47c29-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47c29-132">RELATED LINKS</span></span>

[<span data-ttu-id="47c29-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="47c29-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="47c29-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="47c29-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="47c29-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="47c29-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
