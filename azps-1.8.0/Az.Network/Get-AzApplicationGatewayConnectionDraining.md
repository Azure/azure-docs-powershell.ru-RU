---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 1630b0177efbccbf4d1cba674f0cf11ab457307e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402122"
---
# <span data-ttu-id="89e10-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="89e10-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="89e10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89e10-102">SYNOPSIS</span></span>
<span data-ttu-id="89e10-103">Получает конфигурацию разрядки подключения для объекта с замещающий http-параметрами.</span><span class="sxs-lookup"><span data-stu-id="89e10-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="89e10-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89e10-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89e10-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89e10-105">DESCRIPTION</span></span>
<span data-ttu-id="89e10-106">С **помощью cmdlet Get-AzApplicationGatewayConnectionDraining** получает конфигурацию разрядки подключения для объекта параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="89e10-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="89e10-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89e10-107">EXAMPLES</span></span>

### <span data-ttu-id="89e10-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="89e10-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="89e10-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="89e10-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="89e10-110">Вторая команда получает back-end HTTP-параметры с именем Settings01 для $AppGw и сохраняет их в $Settings переменной.</span><span class="sxs-lookup"><span data-stu-id="89e10-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="89e10-111">Последняя команда получает конфигурацию разрядки подключения из back-end HTTP-параметров $Settings и сохраняет ее в переменной $ConnectionDraining подключения.</span><span class="sxs-lookup"><span data-stu-id="89e10-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="89e10-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89e10-112">PARAMETERS</span></span>

### <span data-ttu-id="89e10-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="89e10-113">-BackendHttpSettings</span></span>
<span data-ttu-id="89e10-114">Параметры backend http</span><span class="sxs-lookup"><span data-stu-id="89e10-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89e10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e10-115">-DefaultProfile</span></span>
<span data-ttu-id="89e10-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89e10-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89e10-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e10-117">CommonParameters</span></span>
<span data-ttu-id="89e10-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e10-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e10-119">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89e10-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e10-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89e10-120">INPUTS</span></span>

### <span data-ttu-id="89e10-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="89e10-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="89e10-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89e10-122">OUTPUTS</span></span>

### <span data-ttu-id="89e10-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="89e10-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="89e10-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89e10-124">NOTES</span></span>

## <span data-ttu-id="89e10-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89e10-125">RELATED LINKS</span></span>

[<span data-ttu-id="89e10-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89e10-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="89e10-127">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="89e10-127">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="89e10-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="89e10-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="89e10-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="89e10-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
