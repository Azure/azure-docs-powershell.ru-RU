---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 50f80f8c7a191c43bb9e8b6b4aed5f44d1ecb85a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506118"
---
# <span data-ttu-id="7cf23-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7cf23-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="7cf23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cf23-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf23-103">Возвращает массив сопоставлений URL-путей с пулом серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="7cf23-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7cf23-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7cf23-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cf23-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cf23-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf23-106">**Cmdlet Get-AzApplicationGatewayURLPathMapConfig** возвращает массив сопоставлений URL-путей с пулом серверов.</span><span class="sxs-lookup"><span data-stu-id="7cf23-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7cf23-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7cf23-107">EXAMPLES</span></span>

### <span data-ttu-id="7cf23-108">Пример 1. Настройка карты URL-адреса</span><span class="sxs-lookup"><span data-stu-id="7cf23-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="7cf23-109">Эта команда получает конфигурации URL-пути из сервера серверов серверов приложений, расположенного на шлюзе приложения "Шлюз".</span><span class="sxs-lookup"><span data-stu-id="7cf23-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="7cf23-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cf23-110">PARAMETERS</span></span>

### <span data-ttu-id="7cf23-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7cf23-111">-ApplicationGateway</span></span>
<span data-ttu-id="7cf23-112">Указывает шлюз приложения, к которому этот cmdlet получает конфигурацию карты URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7cf23-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="7cf23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf23-113">-DefaultProfile</span></span>
<span data-ttu-id="7cf23-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf23-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cf23-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7cf23-115">-Name</span></span>
<span data-ttu-id="7cf23-116">Указывает имя КАРТЫ URL-адреса, в котором этот cmdlet определяет конфигурацию карты пути.</span><span class="sxs-lookup"><span data-stu-id="7cf23-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="7cf23-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf23-117">CommonParameters</span></span>
<span data-ttu-id="7cf23-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf23-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf23-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cf23-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf23-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cf23-120">INPUTS</span></span>

### <span data-ttu-id="7cf23-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7cf23-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7cf23-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7cf23-122">OUTPUTS</span></span>

### <span data-ttu-id="7cf23-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="7cf23-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="7cf23-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7cf23-124">NOTES</span></span>

## <span data-ttu-id="7cf23-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cf23-125">RELATED LINKS</span></span>

[<span data-ttu-id="7cf23-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7cf23-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7cf23-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7cf23-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7cf23-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7cf23-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7cf23-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7cf23-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


