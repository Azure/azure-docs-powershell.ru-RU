---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 50f80f8c7a191c43bb9e8b6b4aed5f44d1ecb85a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078942"
---
# <span data-ttu-id="7f049-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7f049-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="7f049-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f049-102">SYNOPSIS</span></span>
<span data-ttu-id="7f049-103">Получает массив сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="7f049-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7f049-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f049-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f049-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f049-105">DESCRIPTION</span></span>
<span data-ttu-id="7f049-106">Командлет **Get-AzApplicationGatewayURLPathMapConfig** получает массив сопоставлений URL-путей с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="7f049-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7f049-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f049-107">EXAMPLES</span></span>

### <span data-ttu-id="7f049-108">Пример 1: получение конфигурации карты URL-пути</span><span class="sxs-lookup"><span data-stu-id="7f049-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="7f049-109">Эта команда получает параметры карты URL-пути на внутреннем сервере, расположенном на шлюзе приложений с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="7f049-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="7f049-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f049-110">PARAMETERS</span></span>

### <span data-ttu-id="7f049-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f049-111">-ApplicationGateway</span></span>
<span data-ttu-id="7f049-112">Указывает шлюз приложения, на который этот командлет получает конфигурацию карты URL-пути.</span><span class="sxs-lookup"><span data-stu-id="7f049-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="7f049-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f049-113">-DefaultProfile</span></span>
<span data-ttu-id="7f049-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f049-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f049-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7f049-115">-Name</span></span>
<span data-ttu-id="7f049-116">Указывает имя карты URL-пути, в котором этот командлет получает конфигурацию схемы пути.</span><span class="sxs-lookup"><span data-stu-id="7f049-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="7f049-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f049-117">CommonParameters</span></span>
<span data-ttu-id="7f049-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f049-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f049-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f049-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f049-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f049-120">INPUTS</span></span>

### <span data-ttu-id="7f049-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f049-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f049-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f049-122">OUTPUTS</span></span>

### <span data-ttu-id="7f049-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="7f049-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="7f049-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f049-124">NOTES</span></span>

## <span data-ttu-id="7f049-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f049-125">RELATED LINKS</span></span>

[<span data-ttu-id="7f049-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7f049-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7f049-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7f049-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7f049-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7f049-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7f049-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7f049-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


