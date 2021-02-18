---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 5bf9106ccfd780fcfcdb7c86b6b86cdee82aba43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240925"
---
# <span data-ttu-id="c31f8-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c31f8-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="c31f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c31f8-102">SYNOPSIS</span></span>
<span data-ttu-id="c31f8-103">Создает конфигурацию автомасштабации для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="c31f8-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="c31f8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c31f8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c31f8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c31f8-105">DESCRIPTION</span></span>
<span data-ttu-id="c31f8-106">Для шлюза приложения Azure создается конфигурация автомасштабирования с использованием **new-AzApplicationGatewayAutoscaleConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="c31f8-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="c31f8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c31f8-107">EXAMPLES</span></span>

### <span data-ttu-id="c31f8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c31f8-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="c31f8-109">Первая команда создает конфигурацию с автоматической шкалой с минимальной емкостью 3.</span><span class="sxs-lookup"><span data-stu-id="c31f8-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="c31f8-110">Вторая команда создает шлюз приложения с конфигурацией автомасштаби.</span><span class="sxs-lookup"><span data-stu-id="c31f8-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="c31f8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c31f8-111">PARAMETERS</span></span>

### <span data-ttu-id="c31f8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c31f8-112">-DefaultProfile</span></span>
<span data-ttu-id="c31f8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c31f8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c31f8-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="c31f8-114">-MaxCapacity</span></span>
<span data-ttu-id="c31f8-115">Максимальное количество единиц емкости, которое всегда будет доступно [и зарядит] для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="c31f8-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="c31f8-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="c31f8-116">-MinCapacity</span></span>
<span data-ttu-id="c31f8-117">Минимальные единицы емкости, которые всегда будут доступны [и зарядят] для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="c31f8-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="c31f8-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c31f8-118">-Confirm</span></span>
<span data-ttu-id="c31f8-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c31f8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c31f8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c31f8-120">-WhatIf</span></span>
<span data-ttu-id="c31f8-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c31f8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c31f8-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c31f8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c31f8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c31f8-123">CommonParameters</span></span>
<span data-ttu-id="c31f8-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c31f8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c31f8-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c31f8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c31f8-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c31f8-126">INPUTS</span></span>

### <span data-ttu-id="c31f8-127">Нет</span><span class="sxs-lookup"><span data-stu-id="c31f8-127">None</span></span>

## <span data-ttu-id="c31f8-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c31f8-128">OUTPUTS</span></span>

### <span data-ttu-id="c31f8-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c31f8-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="c31f8-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c31f8-130">NOTES</span></span>

## <span data-ttu-id="c31f8-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c31f8-131">RELATED LINKS</span></span>

[<span data-ttu-id="c31f8-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c31f8-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c31f8-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c31f8-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c31f8-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c31f8-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
