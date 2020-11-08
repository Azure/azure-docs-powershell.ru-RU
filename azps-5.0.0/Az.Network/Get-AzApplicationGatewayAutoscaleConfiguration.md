---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: b4238f5b1492afad7d09ee9c338a346d5f54a5e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248365"
---
# <span data-ttu-id="44267-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="44267-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="44267-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44267-102">SYNOPSIS</span></span>
<span data-ttu-id="44267-103">Получает конфигурацию автоматического масштабирования для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="44267-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="44267-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44267-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44267-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44267-105">DESCRIPTION</span></span>
<span data-ttu-id="44267-106">Командлет **Get-AzApplicationGatewayAutoscaleConfiguration** получает конфигурацию автомасштабирования шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="44267-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="44267-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44267-107">EXAMPLES</span></span>

### <span data-ttu-id="44267-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="44267-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="44267-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="44267-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="44267-110">Вторая команда извлекает конфигурацию автомасштабирования из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="44267-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="44267-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44267-111">PARAMETERS</span></span>

### <span data-ttu-id="44267-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="44267-112">-ApplicationGateway</span></span>
<span data-ttu-id="44267-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="44267-113">The applicationGateway</span></span>

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

### <span data-ttu-id="44267-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44267-114">-DefaultProfile</span></span>
<span data-ttu-id="44267-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44267-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44267-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44267-116">CommonParameters</span></span>
<span data-ttu-id="44267-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44267-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44267-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44267-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44267-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44267-119">INPUTS</span></span>

### <span data-ttu-id="44267-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="44267-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="44267-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44267-121">OUTPUTS</span></span>

### <span data-ttu-id="44267-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="44267-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="44267-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="44267-123">NOTES</span></span>

## <span data-ttu-id="44267-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44267-124">RELATED LINKS</span></span>

[<span data-ttu-id="44267-125">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="44267-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="44267-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="44267-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="44267-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="44267-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
