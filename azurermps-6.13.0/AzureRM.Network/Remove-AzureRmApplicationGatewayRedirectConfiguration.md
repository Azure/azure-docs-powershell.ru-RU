---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: f542783ce1edcebf0c0c4e70116423836ddff736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562856"
---
# <span data-ttu-id="b9ff7-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9ff7-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="b9ff7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ff7-103">Удаление конфигурации перенаправления из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b9ff7-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9ff7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9ff7-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9ff7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="b9ff7-106">Командлет **Remove-AzureRmApplicationGatewayRedirectConfiguration** удаляет конфигурацию перенаправления из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b9ff7-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="b9ff7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9ff7-107">EXAMPLES</span></span>

### <span data-ttu-id="b9ff7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9ff7-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="b9ff7-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b9ff7-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b9ff7-110">Вторая команда удаляет конфигурацию перенаправления с именем Redirect01 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b9ff7-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b9ff7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9ff7-111">PARAMETERS</span></span>

### <span data-ttu-id="b9ff7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9ff7-112">-ApplicationGateway</span></span>
<span data-ttu-id="b9ff7-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9ff7-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b9ff7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ff7-114">-DefaultProfile</span></span>
<span data-ttu-id="b9ff7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ff7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ff7-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b9ff7-116">-Name</span></span>
<span data-ttu-id="b9ff7-117">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="b9ff7-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="b9ff7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ff7-118">CommonParameters</span></span>
<span data-ttu-id="b9ff7-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9ff7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ff7-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9ff7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ff7-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9ff7-121">INPUTS</span></span>

### <span data-ttu-id="b9ff7-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9ff7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="b9ff7-123">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b9ff7-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="b9ff7-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9ff7-124">OUTPUTS</span></span>

### <span data-ttu-id="b9ff7-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9ff7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9ff7-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9ff7-126">NOTES</span></span>

## <span data-ttu-id="b9ff7-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9ff7-127">RELATED LINKS</span></span>
