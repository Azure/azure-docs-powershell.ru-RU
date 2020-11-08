---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: b5170ef175b93bc977ba047d4188d51de2858e63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065799"
---
# <span data-ttu-id="26759-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="26759-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="26759-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26759-102">SYNOPSIS</span></span>
<span data-ttu-id="26759-103">Изменяет объект ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="26759-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="26759-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26759-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26759-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26759-105">DESCRIPTION</span></span>
<span data-ttu-id="26759-106">Командлет **Set-AzExpressRoutePort** сохраняет измененный ExpressRoutePort в Azure.</span><span class="sxs-lookup"><span data-stu-id="26759-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="26759-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26759-107">EXAMPLES</span></span>

### <span data-ttu-id="26759-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26759-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="26759-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="26759-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="26759-110">Изменяет состояние администратора для ссылки на ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="26759-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="26759-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26759-111">PARAMETERS</span></span>

### <span data-ttu-id="26759-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26759-112">-AsJob</span></span>
<span data-ttu-id="26759-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="26759-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26759-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26759-114">-DefaultProfile</span></span>
<span data-ttu-id="26759-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26759-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26759-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="26759-116">-ExpressRoutePort</span></span>
<span data-ttu-id="26759-117">Объект ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="26759-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="26759-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26759-118">-Confirm</span></span>
<span data-ttu-id="26759-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26759-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26759-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26759-120">-WhatIf</span></span>
<span data-ttu-id="26759-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26759-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26759-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26759-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26759-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26759-123">CommonParameters</span></span>
<span data-ttu-id="26759-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26759-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26759-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26759-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26759-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26759-126">INPUTS</span></span>

### <span data-ttu-id="26759-127">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="26759-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="26759-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26759-128">OUTPUTS</span></span>

### <span data-ttu-id="26759-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="26759-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="26759-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="26759-130">NOTES</span></span>

## <span data-ttu-id="26759-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26759-131">RELATED LINKS</span></span>

[<span data-ttu-id="26759-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="26759-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="26759-133">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="26759-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="26759-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="26759-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
