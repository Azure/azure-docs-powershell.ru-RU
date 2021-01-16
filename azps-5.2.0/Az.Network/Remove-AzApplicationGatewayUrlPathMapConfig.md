---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409735"
---
# <span data-ttu-id="9599c-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9599c-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="9599c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9599c-102">SYNOPSIS</span></span>
<span data-ttu-id="9599c-103">Удаляет сопоставления путей URL-адреса с пулом серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="9599c-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9599c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9599c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9599c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9599c-105">DESCRIPTION</span></span>
<span data-ttu-id="9599c-106">Для удаления сопоставления URL-путей с пулом серверов серверов удаляются команды **Remove-AzApplicationGatewayUrlPathMapConfig.**</span><span class="sxs-lookup"><span data-stu-id="9599c-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9599c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9599c-107">EXAMPLES</span></span>

### <span data-ttu-id="9599c-108">Пример 1. Удаление сопоставления URL-пути из шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="9599c-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="9599c-109">Первая команда получает шлюз приложения appGwName и сохраняет результат в переменной $appgw.</span><span class="sxs-lookup"><span data-stu-id="9599c-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="9599c-110">Вторая команда удаляет сопоставление URL-адреса с именем map01 из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9599c-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="9599c-111">Третья команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="9599c-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="9599c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9599c-112">PARAMETERS</span></span>

### <span data-ttu-id="9599c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9599c-113">-ApplicationGateway</span></span>
<span data-ttu-id="9599c-114">Указывает шлюз приложения, для которого этот cmdlet удаляет конфигурацию карты URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="9599c-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="9599c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9599c-115">-DefaultProfile</span></span>
<span data-ttu-id="9599c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9599c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9599c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9599c-117">-Name</span></span>
<span data-ttu-id="9599c-118">Указывает имя карты URL-адреса, которое этот cmdlet удаляет с сервера серверов.</span><span class="sxs-lookup"><span data-stu-id="9599c-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="9599c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9599c-119">CommonParameters</span></span>
<span data-ttu-id="9599c-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9599c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9599c-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9599c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9599c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9599c-122">INPUTS</span></span>

### <span data-ttu-id="9599c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9599c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9599c-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9599c-124">OUTPUTS</span></span>

### <span data-ttu-id="9599c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9599c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9599c-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9599c-126">NOTES</span></span>

## <span data-ttu-id="9599c-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9599c-127">RELATED LINKS</span></span>

[<span data-ttu-id="9599c-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9599c-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9599c-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9599c-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9599c-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9599c-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9599c-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9599c-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


