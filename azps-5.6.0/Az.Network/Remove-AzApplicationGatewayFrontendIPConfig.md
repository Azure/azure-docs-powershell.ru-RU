---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 0c226cf7dabbc170e137f1a809cee0afe3c7e76f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992536"
---
# <span data-ttu-id="c524b-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c524b-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="c524b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c524b-102">SYNOPSIS</span></span>
<span data-ttu-id="c524b-103">Удаляет конфигурацию IP-адреса переднего ip-адреса из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="c524b-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="c524b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c524b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c524b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c524b-105">DESCRIPTION</span></span>
<span data-ttu-id="c524b-106">При этом из шлюза приложения Azure удаляется **IP-адрес** переднего входа.</span><span class="sxs-lookup"><span data-stu-id="c524b-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="c524b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c524b-107">EXAMPLES</span></span>

### <span data-ttu-id="c524b-108">Пример 1. Удаление конфигурации переднего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="c524b-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="c524b-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c524b-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c524b-110">Вторая команда удаляет ip-конфигурацию front-end с именем FrontEndIP02 из шлюза приложения, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c524b-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c524b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c524b-111">PARAMETERS</span></span>

### <span data-ttu-id="c524b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c524b-112">-ApplicationGateway</span></span>
<span data-ttu-id="c524b-113">Указывает шлюз приложения, из которого нужно удалить конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="c524b-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="c524b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c524b-114">-DefaultProfile</span></span>
<span data-ttu-id="c524b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c524b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c524b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c524b-116">-Name</span></span>
<span data-ttu-id="c524b-117">Указывает имя ip-конфигурации переднего ip-адреса, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c524b-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="c524b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c524b-118">CommonParameters</span></span>
<span data-ttu-id="c524b-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c524b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c524b-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c524b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c524b-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c524b-121">INPUTS</span></span>

### <span data-ttu-id="c524b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c524b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c524b-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c524b-123">OUTPUTS</span></span>

### <span data-ttu-id="c524b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c524b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c524b-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c524b-125">NOTES</span></span>

## <span data-ttu-id="c524b-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c524b-126">RELATED LINKS</span></span>

[<span data-ttu-id="c524b-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c524b-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c524b-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c524b-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c524b-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c524b-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="c524b-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c524b-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


