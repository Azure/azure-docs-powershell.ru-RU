---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 81b750188a85add491e519c023c765f302e31dea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518085"
---
# <span data-ttu-id="3c7c1-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3c7c1-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="3c7c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7c1-103">Удаляет http-прослушивание из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3c7c1-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="3c7c1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3c7c1-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c7c1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c7c1-105">DESCRIPTION</span></span>
<span data-ttu-id="3c7c1-106">С **помощью cmdlet Remove-AzApplicationGatewayHttpListener** http-прослушивание удаляется из шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3c7c1-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="3c7c1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3c7c1-107">EXAMPLES</span></span>

### <span data-ttu-id="3c7c1-108">Пример 1. Удаление http-прослушивание шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="3c7c1-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="3c7c1-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3c7c1-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3c7c1-110">Вторая команда удаляет HTTP-прослушивание с именем Listener02 из шлюза приложения, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3c7c1-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="3c7c1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c7c1-111">PARAMETERS</span></span>

### <span data-ttu-id="3c7c1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c7c1-112">-ApplicationGateway</span></span>
<span data-ttu-id="3c7c1-113">Указывает шлюз приложения, из которого необходимо удалить http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="3c7c1-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="3c7c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7c1-114">-DefaultProfile</span></span>
<span data-ttu-id="3c7c1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c7c1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c7c1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3c7c1-116">-Name</span></span>
<span data-ttu-id="3c7c1-117">Указывает имя http-прослушивание, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c7c1-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3c7c1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7c1-118">CommonParameters</span></span>
<span data-ttu-id="3c7c1-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c7c1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7c1-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c7c1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7c1-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c7c1-121">INPUTS</span></span>

### <span data-ttu-id="3c7c1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c7c1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3c7c1-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3c7c1-123">OUTPUTS</span></span>

### <span data-ttu-id="3c7c1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3c7c1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="3c7c1-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3c7c1-125">NOTES</span></span>

## <span data-ttu-id="3c7c1-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c7c1-126">RELATED LINKS</span></span>

[<span data-ttu-id="3c7c1-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3c7c1-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3c7c1-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3c7c1-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3c7c1-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3c7c1-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3c7c1-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3c7c1-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


