---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: dd7ad8110afad4302c393295599ed1ef9d6fd4bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913459"
---
# <span data-ttu-id="3768f-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3768f-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="3768f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3768f-102">SYNOPSIS</span></span>
<span data-ttu-id="3768f-103">Получает массив сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="3768f-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3768f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3768f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3768f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3768f-105">DESCRIPTION</span></span>
<span data-ttu-id="3768f-106">Командлет **Get-AzureRmApplicationGatewayURLPathMapConfig** получает массив сопоставлений URL-путей с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="3768f-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="3768f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3768f-107">EXAMPLES</span></span>

### <span data-ttu-id="3768f-108">Пример 1: получение конфигурации карты URL-пути</span><span class="sxs-lookup"><span data-stu-id="3768f-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="3768f-109">Эта команда получает параметры карты URL-пути на внутреннем сервере, расположенном на шлюзе приложений с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="3768f-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="3768f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3768f-110">PARAMETERS</span></span>

### <span data-ttu-id="3768f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3768f-111">-ApplicationGateway</span></span>
<span data-ttu-id="3768f-112">Указывает шлюз приложения, на который этот командлет получает конфигурацию карты URL-пути.</span><span class="sxs-lookup"><span data-stu-id="3768f-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3768f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3768f-113">-DefaultProfile</span></span>
<span data-ttu-id="3768f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3768f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3768f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3768f-115">-Name</span></span>
<span data-ttu-id="3768f-116">Указывает имя карты URL-пути, в котором этот командлет получает конфигурацию схемы пути.</span><span class="sxs-lookup"><span data-stu-id="3768f-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3768f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3768f-117">CommonParameters</span></span>
<span data-ttu-id="3768f-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3768f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3768f-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3768f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3768f-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3768f-120">INPUTS</span></span>

### <span data-ttu-id="3768f-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3768f-121">PSApplicationGateway</span></span>
<span data-ttu-id="3768f-122">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3768f-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="3768f-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3768f-123">OUTPUTS</span></span>

### <span data-ttu-id="3768f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="3768f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="3768f-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Networking. Models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="3768f-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="3768f-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="3768f-126">NOTES</span></span>

## <span data-ttu-id="3768f-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3768f-127">RELATED LINKS</span></span>

[<span data-ttu-id="3768f-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3768f-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3768f-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3768f-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3768f-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3768f-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3768f-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3768f-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


