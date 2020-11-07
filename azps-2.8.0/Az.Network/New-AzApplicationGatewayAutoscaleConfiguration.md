---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 0d99ec672d75844eca37cb63d63a2c6d7433d04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902797"
---
# <span data-ttu-id="b8bf3-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8bf3-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="b8bf3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="b8bf3-103">Создает конфигурацию автомасштабирования для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="b8bf3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8bf3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8bf3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="b8bf3-106">Командлет **New-AzApplicationGatewayAutoscaleConfiguration** создает конфигурацию автомасштабирования для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="b8bf3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="b8bf3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b8bf3-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="b8bf3-109">Первая команда создает конфигурацию автомасштабирования с минимальной емкостью 3.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="b8bf3-110">Вторая команда создает шлюз приложений с конфигурацией автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="b8bf3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8bf3-111">PARAMETERS</span></span>

### <span data-ttu-id="b8bf3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8bf3-112">-DefaultProfile</span></span>
<span data-ttu-id="b8bf3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8bf3-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="b8bf3-114">-MaxCapacity</span></span>
<span data-ttu-id="b8bf3-115">Максимальные единицы мощности, которые будут всегда доступны [и заряжена] для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="b8bf3-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="b8bf3-116">-MinCapacity</span></span>
<span data-ttu-id="b8bf3-117">Минимальные единицы мощности, которые будут всегда доступны [и заряжена] для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="b8bf3-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8bf3-118">-Confirm</span></span>
<span data-ttu-id="b8bf3-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8bf3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8bf3-120">-WhatIf</span></span>
<span data-ttu-id="b8bf3-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8bf3-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8bf3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8bf3-123">CommonParameters</span></span>
<span data-ttu-id="b8bf3-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8bf3-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8bf3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8bf3-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8bf3-126">INPUTS</span></span>

### <span data-ttu-id="b8bf3-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="b8bf3-127">None</span></span>

## <span data-ttu-id="b8bf3-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8bf3-128">OUTPUTS</span></span>

### <span data-ttu-id="b8bf3-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8bf3-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="b8bf3-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8bf3-130">NOTES</span></span>

## <span data-ttu-id="b8bf3-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8bf3-131">RELATED LINKS</span></span>

[<span data-ttu-id="b8bf3-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8bf3-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="b8bf3-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8bf3-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="b8bf3-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8bf3-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
