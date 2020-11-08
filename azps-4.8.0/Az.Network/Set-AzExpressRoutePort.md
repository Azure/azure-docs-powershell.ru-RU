---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: b5170ef175b93bc977ba047d4188d51de2858e63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234895"
---
# <span data-ttu-id="e49e5-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e49e5-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="e49e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e49e5-102">SYNOPSIS</span></span>
<span data-ttu-id="e49e5-103">Изменяет объект ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="e49e5-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="e49e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e49e5-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e49e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e49e5-105">DESCRIPTION</span></span>
<span data-ttu-id="e49e5-106">Командлет **Set-AzExpressRoutePort** сохраняет измененный ExpressRoutePort в Azure.</span><span class="sxs-lookup"><span data-stu-id="e49e5-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="e49e5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e49e5-107">EXAMPLES</span></span>

### <span data-ttu-id="e49e5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e49e5-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="e49e5-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e49e5-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="e49e5-110">Изменяет состояние администратора для ссылки на ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e49e5-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="e49e5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e49e5-111">PARAMETERS</span></span>

### <span data-ttu-id="e49e5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e49e5-112">-AsJob</span></span>
<span data-ttu-id="e49e5-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e49e5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e49e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49e5-114">-DefaultProfile</span></span>
<span data-ttu-id="e49e5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e49e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e49e5-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e49e5-116">-ExpressRoutePort</span></span>
<span data-ttu-id="e49e5-117">Объект ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="e49e5-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="e49e5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e49e5-118">-Confirm</span></span>
<span data-ttu-id="e49e5-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e49e5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e49e5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e49e5-120">-WhatIf</span></span>
<span data-ttu-id="e49e5-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e49e5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e49e5-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e49e5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e49e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49e5-123">CommonParameters</span></span>
<span data-ttu-id="e49e5-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e49e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49e5-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e49e5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49e5-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e49e5-126">INPUTS</span></span>

### <span data-ttu-id="e49e5-127">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e49e5-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="e49e5-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e49e5-128">OUTPUTS</span></span>

### <span data-ttu-id="e49e5-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e49e5-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="e49e5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="e49e5-130">NOTES</span></span>

## <span data-ttu-id="e49e5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e49e5-131">RELATED LINKS</span></span>

[<span data-ttu-id="e49e5-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e49e5-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="e49e5-133">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e49e5-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="e49e5-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e49e5-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
