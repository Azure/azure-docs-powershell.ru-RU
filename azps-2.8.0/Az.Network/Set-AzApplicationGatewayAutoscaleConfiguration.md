---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: ad8795016fc10212a885267d23a61ddc7224c906
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903365"
---
# <span data-ttu-id="cfb55-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfb55-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="cfb55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfb55-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb55-103">Обновляет конфигурацию автоматического масштабирования для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="cfb55-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="cfb55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfb55-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfb55-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfb55-105">DESCRIPTION</span></span>
<span data-ttu-id="cfb55-106">Командлет **Set-AzApplicationGatewayAutoscaleConfiguration** изменяет существующую конфигурацию автомасштабирования для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="cfb55-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="cfb55-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfb55-107">EXAMPLES</span></span>

### <span data-ttu-id="cfb55-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cfb55-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="cfb55-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="cfb55-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="cfb55-110">Вторая команда обновляет конфигурацию автомасштабирования с шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="cfb55-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="cfb55-111">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="cfb55-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="cfb55-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfb55-112">PARAMETERS</span></span>

### <span data-ttu-id="cfb55-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfb55-113">-ApplicationGateway</span></span>
<span data-ttu-id="cfb55-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfb55-114">The applicationGateway</span></span>

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

### <span data-ttu-id="cfb55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfb55-115">-DefaultProfile</span></span>
<span data-ttu-id="cfb55-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfb55-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfb55-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="cfb55-117">-MaxCapacity</span></span>
<span data-ttu-id="cfb55-118">Максимальная емкость для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="cfb55-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="cfb55-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="cfb55-119">-MinCapacity</span></span>
<span data-ttu-id="cfb55-120">Минимальная емкость для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="cfb55-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="cfb55-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfb55-121">-Confirm</span></span>
<span data-ttu-id="cfb55-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cfb55-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfb55-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfb55-123">-WhatIf</span></span>
<span data-ttu-id="cfb55-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cfb55-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfb55-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cfb55-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfb55-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb55-126">CommonParameters</span></span>
<span data-ttu-id="cfb55-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfb55-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb55-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfb55-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb55-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfb55-129">INPUTS</span></span>

### <span data-ttu-id="cfb55-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfb55-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cfb55-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfb55-131">OUTPUTS</span></span>

### <span data-ttu-id="cfb55-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfb55-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cfb55-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfb55-133">NOTES</span></span>

## <span data-ttu-id="cfb55-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfb55-134">RELATED LINKS</span></span>

[<span data-ttu-id="cfb55-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfb55-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="cfb55-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfb55-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="cfb55-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfb55-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
