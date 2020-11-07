---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 27561ec3592633e1e7c668a4d901ba1e7d39c050
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730191"
---
# <span data-ttu-id="fcf89-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fcf89-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="fcf89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fcf89-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf89-103">Удаление сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="fcf89-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="fcf89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fcf89-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcf89-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcf89-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf89-106">Командлет **Remove-AzApplicationGatewayUrlPathMapConfig** Удаляет сопоставления URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="fcf89-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="fcf89-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fcf89-107">EXAMPLES</span></span>

### <span data-ttu-id="fcf89-108">Пример 1: Удаление сопоставления URL-пути из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="fcf89-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="fcf89-109">Первая команда получает шлюз приложения с именем appGwName и сохраняет результат в переменной $appgw.</span><span class="sxs-lookup"><span data-stu-id="fcf89-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="fcf89-110">Вторая команда удаляет сопоставление URL-пути с именем map01 из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="fcf89-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="fcf89-111">Третья команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="fcf89-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="fcf89-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fcf89-112">PARAMETERS</span></span>

### <span data-ttu-id="fcf89-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fcf89-113">-ApplicationGateway</span></span>
<span data-ttu-id="fcf89-114">Указывает шлюз приложений, для которого этот командлет удаляет конфигурацию карты URL-пути.</span><span class="sxs-lookup"><span data-stu-id="fcf89-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="fcf89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf89-115">-DefaultProfile</span></span>
<span data-ttu-id="fcf89-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf89-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcf89-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fcf89-117">-Name</span></span>
<span data-ttu-id="fcf89-118">Указывает имя карты URL-пути, которое удаляется этим командлетом из внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="fcf89-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf89-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf89-119">CommonParameters</span></span>
<span data-ttu-id="fcf89-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fcf89-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf89-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf89-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf89-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fcf89-122">INPUTS</span></span>

### <span data-ttu-id="fcf89-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fcf89-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fcf89-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcf89-124">OUTPUTS</span></span>

### <span data-ttu-id="fcf89-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fcf89-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fcf89-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="fcf89-126">NOTES</span></span>

## <span data-ttu-id="fcf89-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fcf89-127">RELATED LINKS</span></span>

[<span data-ttu-id="fcf89-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fcf89-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="fcf89-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fcf89-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="fcf89-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fcf89-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="fcf89-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fcf89-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


