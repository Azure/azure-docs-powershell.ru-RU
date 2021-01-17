---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: d376bc1e70d0441f139b64c19466a88daf6877c4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398255"
---
# <span data-ttu-id="92b73-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="92b73-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="92b73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92b73-102">SYNOPSIS</span></span>
<span data-ttu-id="92b73-103">Удаляет конфигурацию IP-адреса переднего ip-адреса из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="92b73-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="92b73-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92b73-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92b73-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92b73-105">DESCRIPTION</span></span>
<span data-ttu-id="92b73-106">Для удаления IP-адреса из шлюза приложения Azure удаляется ip-адрес переднего входа в **AzApplicationGatewayFrontendIPConfig.**</span><span class="sxs-lookup"><span data-stu-id="92b73-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="92b73-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92b73-107">EXAMPLES</span></span>

### <span data-ttu-id="92b73-108">Пример 1. Удаление конфигурации IP-адреса переднего</span><span class="sxs-lookup"><span data-stu-id="92b73-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="92b73-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="92b73-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="92b73-110">Вторая команда удаляет ip-конфигурацию front-end с именем FrontEndIP02 из шлюза приложения, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="92b73-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="92b73-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92b73-111">PARAMETERS</span></span>

### <span data-ttu-id="92b73-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92b73-112">-ApplicationGateway</span></span>
<span data-ttu-id="92b73-113">Указывает шлюз приложения, из которого нужно удалить конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="92b73-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="92b73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b73-114">-DefaultProfile</span></span>
<span data-ttu-id="92b73-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92b73-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92b73-116">-Name</span><span class="sxs-lookup"><span data-stu-id="92b73-116">-Name</span></span>
<span data-ttu-id="92b73-117">Указывает имя ip-конфигурации переднего ip-адреса, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="92b73-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="92b73-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b73-118">CommonParameters</span></span>
<span data-ttu-id="92b73-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92b73-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b73-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92b73-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b73-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92b73-121">INPUTS</span></span>

### <span data-ttu-id="92b73-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92b73-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="92b73-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92b73-123">OUTPUTS</span></span>

### <span data-ttu-id="92b73-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92b73-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="92b73-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92b73-125">NOTES</span></span>

## <span data-ttu-id="92b73-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92b73-126">RELATED LINKS</span></span>

[<span data-ttu-id="92b73-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="92b73-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="92b73-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="92b73-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="92b73-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="92b73-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="92b73-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="92b73-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


