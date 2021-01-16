---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e2d80f6c132967e18e5a03a3a4bee4ed470f1719
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390932"
---
# <span data-ttu-id="c68bb-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c68bb-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="c68bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c68bb-102">SYNOPSIS</span></span>
<span data-ttu-id="c68bb-103">Удаляет конфигурацию автомасштабации из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="c68bb-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="c68bb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c68bb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c68bb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c68bb-105">DESCRIPTION</span></span>
<span data-ttu-id="c68bb-106">Для **удаления azApplicationGatewayAutoscaleConfiguration** конфигурация автомасштабирования удаляется из существующего шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="c68bb-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="c68bb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c68bb-107">EXAMPLES</span></span>

### <span data-ttu-id="c68bb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c68bb-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="c68bb-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="c68bb-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="c68bb-110">Вторая команда удаляет конфигурацию автомасштабы из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="c68bb-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="c68bb-111">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="c68bb-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="c68bb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c68bb-112">PARAMETERS</span></span>

### <span data-ttu-id="c68bb-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c68bb-113">-ApplicationGateway</span></span>
<span data-ttu-id="c68bb-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c68bb-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c68bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68bb-115">-DefaultProfile</span></span>
<span data-ttu-id="c68bb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c68bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c68bb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c68bb-117">-Force</span></span>
<span data-ttu-id="c68bb-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c68bb-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c68bb-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c68bb-119">-Confirm</span></span>
<span data-ttu-id="c68bb-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c68bb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c68bb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c68bb-121">-WhatIf</span></span>
<span data-ttu-id="c68bb-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c68bb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c68bb-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c68bb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c68bb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68bb-124">CommonParameters</span></span>
<span data-ttu-id="c68bb-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c68bb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68bb-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c68bb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68bb-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c68bb-127">INPUTS</span></span>

### <span data-ttu-id="c68bb-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c68bb-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c68bb-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c68bb-129">OUTPUTS</span></span>

### <span data-ttu-id="c68bb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c68bb-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c68bb-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c68bb-131">NOTES</span></span>

## <span data-ttu-id="c68bb-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c68bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="c68bb-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c68bb-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c68bb-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c68bb-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c68bb-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c68bb-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
