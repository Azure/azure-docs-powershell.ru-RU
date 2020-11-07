---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: d75cbcbf89fde83419b9a1f97c0f66805258c82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730205"
---
# <span data-ttu-id="26f68-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="26f68-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="26f68-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26f68-102">SYNOPSIS</span></span>
<span data-ttu-id="26f68-103">Удаление конфигурации перенаправления из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="26f68-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="26f68-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26f68-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26f68-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26f68-105">DESCRIPTION</span></span>
<span data-ttu-id="26f68-106">Командлет **Remove-AzApplicationGatewayRedirectConfiguration** удаляет конфигурацию перенаправления из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="26f68-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="26f68-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26f68-107">EXAMPLES</span></span>

### <span data-ttu-id="26f68-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26f68-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="26f68-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="26f68-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="26f68-110">Вторая команда удаляет конфигурацию перенаправления с именем Redirect01 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="26f68-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="26f68-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26f68-111">PARAMETERS</span></span>

### <span data-ttu-id="26f68-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26f68-112">-ApplicationGateway</span></span>
<span data-ttu-id="26f68-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26f68-113">The applicationGateway</span></span>

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

### <span data-ttu-id="26f68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f68-114">-DefaultProfile</span></span>
<span data-ttu-id="26f68-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26f68-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26f68-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26f68-116">-Name</span></span>
<span data-ttu-id="26f68-117">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="26f68-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="26f68-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f68-118">CommonParameters</span></span>
<span data-ttu-id="26f68-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26f68-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f68-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26f68-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f68-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26f68-121">INPUTS</span></span>

### <span data-ttu-id="26f68-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26f68-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="26f68-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26f68-123">OUTPUTS</span></span>

### <span data-ttu-id="26f68-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26f68-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="26f68-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="26f68-125">NOTES</span></span>

## <span data-ttu-id="26f68-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26f68-126">RELATED LINKS</span></span>

[<span data-ttu-id="26f68-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="26f68-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="26f68-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="26f68-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="26f68-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="26f68-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="26f68-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="26f68-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
