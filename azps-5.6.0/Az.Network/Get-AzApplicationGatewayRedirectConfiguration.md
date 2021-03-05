---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: b2e62b0785cc01dfc9b26aeac7b267c06a4d24b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994087"
---
# <span data-ttu-id="1db4a-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1db4a-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="1db4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1db4a-102">SYNOPSIS</span></span>
<span data-ttu-id="1db4a-103">Получает существующую конфигурацию перенаправления из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1db4a-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="1db4a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1db4a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1db4a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1db4a-105">DESCRIPTION</span></span>
<span data-ttu-id="1db4a-106">Cmdlet **Get-AzApplicationGatewayRedirectConfiguration** получает существующую конфигурацию перенаправления из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1db4a-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="1db4a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1db4a-107">EXAMPLES</span></span>

### <span data-ttu-id="1db4a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1db4a-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="1db4a-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет результат в переменной с $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1db4a-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="1db4a-110">Вторая команда получает конфигурацию перенаправления Redirect01 из шлюза приложения, храняного в переменной $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1db4a-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="1db4a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1db4a-111">PARAMETERS</span></span>

### <span data-ttu-id="1db4a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1db4a-112">-ApplicationGateway</span></span>
<span data-ttu-id="1db4a-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1db4a-113">The applicationGateway</span></span>

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

### <span data-ttu-id="1db4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db4a-114">-DefaultProfile</span></span>
<span data-ttu-id="1db4a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1db4a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1db4a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1db4a-116">-Name</span></span>
<span data-ttu-id="1db4a-117">Имя правила маршрутки запроса</span><span class="sxs-lookup"><span data-stu-id="1db4a-117">The name of the request routing rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1db4a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db4a-118">CommonParameters</span></span>
<span data-ttu-id="1db4a-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1db4a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db4a-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1db4a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db4a-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1db4a-121">INPUTS</span></span>

### <span data-ttu-id="1db4a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1db4a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1db4a-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1db4a-123">OUTPUTS</span></span>

### <span data-ttu-id="1db4a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1db4a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="1db4a-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1db4a-125">NOTES</span></span>

## <span data-ttu-id="1db4a-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1db4a-126">RELATED LINKS</span></span>

[<span data-ttu-id="1db4a-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1db4a-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="1db4a-128">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1db4a-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="1db4a-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1db4a-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="1db4a-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1db4a-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
