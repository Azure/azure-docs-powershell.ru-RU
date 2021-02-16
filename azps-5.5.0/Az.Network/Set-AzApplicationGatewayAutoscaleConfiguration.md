---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: cf9e847454fc638afc3c25cc3b5d8f0e78ef2fb0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213457"
---
# <span data-ttu-id="dc722-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc722-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="dc722-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc722-102">SYNOPSIS</span></span>
<span data-ttu-id="dc722-103">Обновляет конфигурацию автомасштабы шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="dc722-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="dc722-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc722-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc722-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc722-105">DESCRIPTION</span></span>
<span data-ttu-id="dc722-106">**Cmdlet Set-AzApplicationGatewayAutoscaleConfiguration** изменяет существующую настройку автомасштабирования шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="dc722-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="dc722-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc722-107">EXAMPLES</span></span>

### <span data-ttu-id="dc722-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc722-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="dc722-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="dc722-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="dc722-110">Вторая команда обновляет конфигурацию автомасштаби из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="dc722-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="dc722-111">Третья команда обновляет шлюз приложения в Azure.</span><span class="sxs-lookup"><span data-stu-id="dc722-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="dc722-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc722-112">PARAMETERS</span></span>

### <span data-ttu-id="dc722-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc722-113">-ApplicationGateway</span></span>
<span data-ttu-id="dc722-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc722-114">The applicationGateway</span></span>

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

### <span data-ttu-id="dc722-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc722-115">-DefaultProfile</span></span>
<span data-ttu-id="dc722-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc722-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc722-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="dc722-117">-MaxCapacity</span></span>
<span data-ttu-id="dc722-118">Максимальная пропускная способность для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="dc722-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="dc722-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="dc722-119">-MinCapacity</span></span>
<span data-ttu-id="dc722-120">Минимальная емкость шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="dc722-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="dc722-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc722-121">-Confirm</span></span>
<span data-ttu-id="dc722-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc722-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc722-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc722-123">-WhatIf</span></span>
<span data-ttu-id="dc722-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc722-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc722-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dc722-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc722-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc722-126">CommonParameters</span></span>
<span data-ttu-id="dc722-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc722-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc722-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc722-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc722-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc722-129">INPUTS</span></span>

### <span data-ttu-id="dc722-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc722-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc722-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc722-131">OUTPUTS</span></span>

### <span data-ttu-id="dc722-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dc722-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dc722-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc722-133">NOTES</span></span>

## <span data-ttu-id="dc722-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc722-134">RELATED LINKS</span></span>

[<span data-ttu-id="dc722-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc722-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="dc722-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc722-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="dc722-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc722-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
