---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 4b28feb85ebc8f4d5669f28609aa4723061c1709
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992533"
---
# <span data-ttu-id="1e7c6-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1e7c6-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="1e7c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e7c6-102">SYNOPSIS</span></span>
<span data-ttu-id="1e7c6-103">Удаление переднего порта из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="1e7c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1e7c6-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e7c6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e7c6-105">DESCRIPTION</span></span>
<span data-ttu-id="1e7c6-106">Для удаления переднего порта из шлюза приложения Azure удаляется клиентский порт **Remove-AzApplicationGatewayFrontendPort.**</span><span class="sxs-lookup"><span data-stu-id="1e7c6-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="1e7c6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1e7c6-107">EXAMPLES</span></span>

### <span data-ttu-id="1e7c6-108">Пример: удаление переднего порта из шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="1e7c6-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="1e7c6-109">Первая команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет шлюз в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="1e7c6-110">Вторая команда удаляет порт FrontEndPort02 из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="1e7c6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e7c6-111">PARAMETERS</span></span>

### <span data-ttu-id="1e7c6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e7c6-112">-ApplicationGateway</span></span>
<span data-ttu-id="1e7c6-113">Указывает шлюз приложения, из которого нужно удалить передний порт.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="1e7c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e7c6-114">-DefaultProfile</span></span>
<span data-ttu-id="1e7c6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e7c6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1e7c6-116">-Name</span></span>
<span data-ttu-id="1e7c6-117">Указывает имя порта переднего входа, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="1e7c6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e7c6-118">CommonParameters</span></span>
<span data-ttu-id="1e7c6-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e7c6-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e7c6-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e7c6-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e7c6-121">INPUTS</span></span>

### <span data-ttu-id="1e7c6-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e7c6-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1e7c6-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1e7c6-123">OUTPUTS</span></span>

### <span data-ttu-id="1e7c6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e7c6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1e7c6-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1e7c6-125">NOTES</span></span>

## <span data-ttu-id="1e7c6-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e7c6-126">RELATED LINKS</span></span>

[<span data-ttu-id="1e7c6-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1e7c6-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="1e7c6-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1e7c6-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="1e7c6-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1e7c6-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="1e7c6-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1e7c6-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


