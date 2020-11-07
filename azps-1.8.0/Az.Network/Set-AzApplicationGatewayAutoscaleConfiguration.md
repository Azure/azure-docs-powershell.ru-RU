---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 931d130ae40e6b7b0331c0aa3a50d28655dec8f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730069"
---
# <span data-ttu-id="288ab-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="288ab-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="288ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="288ab-102">SYNOPSIS</span></span>
<span data-ttu-id="288ab-103">Обновляет конфигурацию автоматического масштабирования для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="288ab-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="288ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="288ab-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="288ab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="288ab-105">DESCRIPTION</span></span>
<span data-ttu-id="288ab-106">Командлет **Set-AzApplicationGatewayAutoscaleConfiguration** изменяет существующую конфигурацию автомасштабирования для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="288ab-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="288ab-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="288ab-107">EXAMPLES</span></span>

### <span data-ttu-id="288ab-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="288ab-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="288ab-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="288ab-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="288ab-110">Вторая команда обновляет конфигурацию автомасштабирования из шлюза applicationg.</span><span class="sxs-lookup"><span data-stu-id="288ab-110">The second command updates the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="288ab-111">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="288ab-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="288ab-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="288ab-112">PARAMETERS</span></span>

### <span data-ttu-id="288ab-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="288ab-113">-ApplicationGateway</span></span>
<span data-ttu-id="288ab-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="288ab-114">The applicationGateway</span></span>

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

### <span data-ttu-id="288ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="288ab-115">-DefaultProfile</span></span>
<span data-ttu-id="288ab-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="288ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="288ab-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="288ab-117">-MaxCapacity</span></span>
<span data-ttu-id="288ab-118">Максимальная capcity для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="288ab-118">Maximum capcity for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="288ab-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="288ab-119">-MinCapacity</span></span>
<span data-ttu-id="288ab-120">Минимальная capcity для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="288ab-120">Minimum capcity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="288ab-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="288ab-121">-Confirm</span></span>
<span data-ttu-id="288ab-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="288ab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="288ab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="288ab-123">-WhatIf</span></span>
<span data-ttu-id="288ab-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="288ab-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="288ab-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="288ab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="288ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288ab-126">CommonParameters</span></span>
<span data-ttu-id="288ab-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="288ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288ab-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="288ab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288ab-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="288ab-129">INPUTS</span></span>

### <span data-ttu-id="288ab-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="288ab-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="288ab-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="288ab-131">OUTPUTS</span></span>

### <span data-ttu-id="288ab-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="288ab-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="288ab-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="288ab-133">NOTES</span></span>

## <span data-ttu-id="288ab-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="288ab-134">RELATED LINKS</span></span>

[<span data-ttu-id="288ab-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="288ab-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="288ab-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="288ab-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="288ab-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="288ab-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
