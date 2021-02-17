---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 08637412afafe9220107e95dd3cb7dcc5154ba26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218289"
---
# <span data-ttu-id="22aa8-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="22aa8-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="22aa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="22aa8-103">Изменяет стойкий порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="22aa8-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="22aa8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="22aa8-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22aa8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22aa8-105">DESCRIPTION</span></span>
<span data-ttu-id="22aa8-106">Для шлюза приложения степенный порт **Set-AzApplicationGatewayFrontendPort** изменяется.</span><span class="sxs-lookup"><span data-stu-id="22aa8-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="22aa8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="22aa8-107">EXAMPLES</span></span>

### <span data-ttu-id="22aa8-108">Пример 1. Настройка переднего порта шлюза приложения на 80</span><span class="sxs-lookup"><span data-stu-id="22aa8-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="22aa8-109">Первая команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="22aa8-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="22aa8-110">Вторая команда изменяет шлюз в $AppGw, чтобы использовать порт 80 для переднего порта FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="22aa8-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="22aa8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22aa8-111">PARAMETERS</span></span>

### <span data-ttu-id="22aa8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22aa8-112">-ApplicationGateway</span></span>
<span data-ttu-id="22aa8-113">Определяет объект шлюза приложения, с которым этот cmdlet связывает стойкий порт.</span><span class="sxs-lookup"><span data-stu-id="22aa8-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="22aa8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22aa8-114">-DefaultProfile</span></span>
<span data-ttu-id="22aa8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22aa8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22aa8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="22aa8-116">-Name</span></span>
<span data-ttu-id="22aa8-117">Указывает имя переднего порта, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="22aa8-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="22aa8-118">-Port</span><span class="sxs-lookup"><span data-stu-id="22aa8-118">-Port</span></span>
<span data-ttu-id="22aa8-119">Номер порта, который нужно использовать для переднего порта.</span><span class="sxs-lookup"><span data-stu-id="22aa8-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22aa8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22aa8-120">CommonParameters</span></span>
<span data-ttu-id="22aa8-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22aa8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22aa8-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22aa8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22aa8-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22aa8-123">INPUTS</span></span>

### <span data-ttu-id="22aa8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22aa8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="22aa8-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22aa8-125">OUTPUTS</span></span>

### <span data-ttu-id="22aa8-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22aa8-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="22aa8-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="22aa8-127">NOTES</span></span>

## <span data-ttu-id="22aa8-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22aa8-128">RELATED LINKS</span></span>

[<span data-ttu-id="22aa8-129">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="22aa8-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="22aa8-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="22aa8-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="22aa8-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="22aa8-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="22aa8-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="22aa8-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
