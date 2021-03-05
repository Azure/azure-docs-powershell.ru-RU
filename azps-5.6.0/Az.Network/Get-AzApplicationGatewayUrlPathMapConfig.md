---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: f82882a4975c2f873362ece62f6eac9e6b7a53a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993936"
---
# <span data-ttu-id="c0479-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c0479-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="c0479-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0479-102">SYNOPSIS</span></span>
<span data-ttu-id="c0479-103">Возвращает массив сопоставлений URL-путей с пулом серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="c0479-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="c0479-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c0479-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0479-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0479-105">DESCRIPTION</span></span>
<span data-ttu-id="c0479-106">Cmdlet **Get-AzApplicationGatewayURLPathMapConfig** возвращает массив сопоставлений URL-путей с пулом серверов.</span><span class="sxs-lookup"><span data-stu-id="c0479-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="c0479-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c0479-107">EXAMPLES</span></span>

### <span data-ttu-id="c0479-108">Пример 1. Настройка карты URL-адреса</span><span class="sxs-lookup"><span data-stu-id="c0479-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="c0479-109">Эта команда получает конфигурации URL-пути из сервера серверов серверов приложений, расположенного на шлюзе приложения "Шлюз".</span><span class="sxs-lookup"><span data-stu-id="c0479-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="c0479-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0479-110">PARAMETERS</span></span>

### <span data-ttu-id="c0479-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0479-111">-ApplicationGateway</span></span>
<span data-ttu-id="c0479-112">Указывает шлюз приложения, к которому этот cmdlet получает конфигурацию карты URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="c0479-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="c0479-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0479-113">-DefaultProfile</span></span>
<span data-ttu-id="c0479-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0479-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0479-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c0479-115">-Name</span></span>
<span data-ttu-id="c0479-116">Указывает имя карты URL-адреса, в которой этот cmdlet определяет конфигурацию карты пути.</span><span class="sxs-lookup"><span data-stu-id="c0479-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="c0479-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0479-117">CommonParameters</span></span>
<span data-ttu-id="c0479-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0479-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0479-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0479-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0479-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0479-120">INPUTS</span></span>

### <span data-ttu-id="c0479-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0479-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c0479-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c0479-122">OUTPUTS</span></span>

### <span data-ttu-id="c0479-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c0479-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="c0479-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c0479-124">NOTES</span></span>

## <span data-ttu-id="c0479-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0479-125">RELATED LINKS</span></span>

[<span data-ttu-id="c0479-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c0479-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c0479-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c0479-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c0479-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c0479-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c0479-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c0479-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


