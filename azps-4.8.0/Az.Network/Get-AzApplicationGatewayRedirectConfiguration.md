---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236977"
---
# <span data-ttu-id="a33fc-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a33fc-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="a33fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a33fc-102">SYNOPSIS</span></span>
<span data-ttu-id="a33fc-103">Получает существующую конфигурацию перенаправления из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a33fc-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="a33fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a33fc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a33fc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a33fc-105">DESCRIPTION</span></span>
<span data-ttu-id="a33fc-106">Командлет **Get-AzApplicationGatewayRedirectConfiguration** получает существующую конфигурацию перенаправления из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a33fc-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="a33fc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a33fc-107">EXAMPLES</span></span>

### <span data-ttu-id="a33fc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a33fc-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="a33fc-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="a33fc-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="a33fc-110">Вторая команда получает конфигурацию перенаправления с именем Redirect01 из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="a33fc-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="a33fc-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a33fc-111">PARAMETERS</span></span>

### <span data-ttu-id="a33fc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a33fc-112">-ApplicationGateway</span></span>
<span data-ttu-id="a33fc-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a33fc-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a33fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33fc-114">-DefaultProfile</span></span>
<span data-ttu-id="a33fc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a33fc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a33fc-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a33fc-116">-Name</span></span>
<span data-ttu-id="a33fc-117">Имя правила маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="a33fc-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="a33fc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33fc-118">CommonParameters</span></span>
<span data-ttu-id="a33fc-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a33fc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33fc-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a33fc-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33fc-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a33fc-121">INPUTS</span></span>

### <span data-ttu-id="a33fc-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a33fc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a33fc-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a33fc-123">OUTPUTS</span></span>

### <span data-ttu-id="a33fc-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a33fc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="a33fc-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="a33fc-125">NOTES</span></span>

## <span data-ttu-id="a33fc-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a33fc-126">RELATED LINKS</span></span>

[<span data-ttu-id="a33fc-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a33fc-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="a33fc-128">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a33fc-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="a33fc-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a33fc-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="a33fc-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a33fc-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
