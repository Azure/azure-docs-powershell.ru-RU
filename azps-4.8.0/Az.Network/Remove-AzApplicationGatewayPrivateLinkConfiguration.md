---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079446"
---
# <span data-ttu-id="003d6-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="003d6-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="003d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="003d6-102">SYNOPSIS</span></span>
<span data-ttu-id="003d6-103">Удаляет конфигурацию privateLink из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="003d6-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="003d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="003d6-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="003d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="003d6-105">DESCRIPTION</span></span>
<span data-ttu-id="003d6-106">Командлет **Remove-AzApplicationGatewayPrivateLinkConfiguration** удаляет конфигурацию privateLink из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="003d6-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="003d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="003d6-107">EXAMPLES</span></span>

### <span data-ttu-id="003d6-108">Пример 1: Удаление конфигурации PrivateLink шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="003d6-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="003d6-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="003d6-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="003d6-110">Вторая команда удаляет конфигурацию privateLink с именем privateLinkConfig01 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="003d6-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="003d6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="003d6-111">PARAMETERS</span></span>

### <span data-ttu-id="003d6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="003d6-112">-ApplicationGateway</span></span>
<span data-ttu-id="003d6-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="003d6-113">The applicationGateway</span></span>

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

### <span data-ttu-id="003d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003d6-114">-DefaultProfile</span></span>
<span data-ttu-id="003d6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="003d6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003d6-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="003d6-116">-Name</span></span>
<span data-ttu-id="003d6-117">Имя конфигурации privateLink шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="003d6-117">The name of the application gateway privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003d6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003d6-118">CommonParameters</span></span>
<span data-ttu-id="003d6-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="003d6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003d6-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="003d6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003d6-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="003d6-121">INPUTS</span></span>

### <span data-ttu-id="003d6-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="003d6-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="003d6-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="003d6-123">OUTPUTS</span></span>

### <span data-ttu-id="003d6-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="003d6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="003d6-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="003d6-125">NOTES</span></span>

## <span data-ttu-id="003d6-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="003d6-126">RELATED LINKS</span></span>

[<span data-ttu-id="003d6-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="003d6-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="003d6-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="003d6-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="003d6-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="003d6-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="003d6-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="003d6-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)