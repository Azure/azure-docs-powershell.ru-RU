---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 25602712a792a1de7b79ce00baf5074ebb8177a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730231"
---
# <span data-ttu-id="d8578-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8578-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="d8578-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8578-102">SYNOPSIS</span></span>
<span data-ttu-id="d8578-103">Удаляет конфигурацию автомасштабирования из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="d8578-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="d8578-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8578-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8578-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8578-105">DESCRIPTION</span></span>
<span data-ttu-id="d8578-106">Командлет **Remove-AzApplicationGatewayAutoscaleConfiguration** удаляет конфигурацию автомасштабирования из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="d8578-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="d8578-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8578-107">EXAMPLES</span></span>

### <span data-ttu-id="d8578-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8578-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="d8578-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="d8578-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="d8578-110">Вторая команда удаляет конфигурацию автомасштабирования из шлюза applicationg.</span><span class="sxs-lookup"><span data-stu-id="d8578-110">The second command removes the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="d8578-111">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="d8578-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="d8578-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8578-112">PARAMETERS</span></span>

### <span data-ttu-id="d8578-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8578-113">-ApplicationGateway</span></span>
<span data-ttu-id="d8578-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8578-114">The applicationGateway</span></span>

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

### <span data-ttu-id="d8578-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8578-115">-DefaultProfile</span></span>
<span data-ttu-id="d8578-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8578-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8578-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d8578-117">-Force</span></span>
<span data-ttu-id="d8578-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d8578-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d8578-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8578-119">-Confirm</span></span>
<span data-ttu-id="d8578-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8578-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8578-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8578-121">-WhatIf</span></span>
<span data-ttu-id="d8578-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8578-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8578-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8578-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8578-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8578-124">CommonParameters</span></span>
<span data-ttu-id="d8578-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8578-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8578-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8578-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8578-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8578-127">INPUTS</span></span>

### <span data-ttu-id="d8578-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8578-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8578-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8578-129">OUTPUTS</span></span>

### <span data-ttu-id="d8578-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8578-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8578-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8578-131">NOTES</span></span>

## <span data-ttu-id="d8578-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8578-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8578-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8578-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="d8578-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8578-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="d8578-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8578-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
