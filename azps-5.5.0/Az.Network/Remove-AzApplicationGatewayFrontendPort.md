---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: fe21bc83fce1e43e036f68ea64c8a10cf2f3c90e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213620"
---
# <span data-ttu-id="111a1-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="111a1-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="111a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="111a1-102">SYNOPSIS</span></span>
<span data-ttu-id="111a1-103">Удаление переднего порта из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="111a1-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="111a1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="111a1-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="111a1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="111a1-105">DESCRIPTION</span></span>
<span data-ttu-id="111a1-106">Для удаления переднего порта из шлюза приложения Azure удаляется клиентский порт **Remove-AzApplicationGatewayFrontendPort.**</span><span class="sxs-lookup"><span data-stu-id="111a1-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="111a1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="111a1-107">EXAMPLES</span></span>

### <span data-ttu-id="111a1-108">Пример: удаление переднего порта из шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="111a1-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="111a1-109">Первая команда получает шлюз приложения ApplicationGateway01, который принадлежит группе ресурсов ResourceGroup01, и сохраняет шлюз в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="111a1-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="111a1-110">Вторая команда удаляет порт FrontEndPort02 из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="111a1-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="111a1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="111a1-111">PARAMETERS</span></span>

### <span data-ttu-id="111a1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="111a1-112">-ApplicationGateway</span></span>
<span data-ttu-id="111a1-113">Указывает шлюз приложения, из которого нужно удалить передний порт.</span><span class="sxs-lookup"><span data-stu-id="111a1-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="111a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="111a1-114">-DefaultProfile</span></span>
<span data-ttu-id="111a1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="111a1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="111a1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="111a1-116">-Name</span></span>
<span data-ttu-id="111a1-117">Указывает имя порта переднего входа, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="111a1-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="111a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="111a1-118">CommonParameters</span></span>
<span data-ttu-id="111a1-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="111a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="111a1-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="111a1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="111a1-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="111a1-121">INPUTS</span></span>

### <span data-ttu-id="111a1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="111a1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="111a1-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="111a1-123">OUTPUTS</span></span>

### <span data-ttu-id="111a1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="111a1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="111a1-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="111a1-125">NOTES</span></span>

## <span data-ttu-id="111a1-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="111a1-126">RELATED LINKS</span></span>

[<span data-ttu-id="111a1-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="111a1-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="111a1-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="111a1-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="111a1-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="111a1-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="111a1-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="111a1-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


