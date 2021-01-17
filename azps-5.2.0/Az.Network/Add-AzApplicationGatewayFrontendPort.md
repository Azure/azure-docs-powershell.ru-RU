---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9cd7cd0b859ff806b084ebfe1c76e07aed3a7c43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406967"
---
# <span data-ttu-id="d7f7b-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d7f7b-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d7f7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f7b-103">Добавляет стойкий порт к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="d7f7b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d7f7b-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7f7b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7f7b-105">DESCRIPTION</span></span>
<span data-ttu-id="d7f7b-106">Для шлюза приложения добавляется порт переднего входа **Add-AzApplicationGatewayFrontendPort.**</span><span class="sxs-lookup"><span data-stu-id="d7f7b-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="d7f7b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d7f7b-107">EXAMPLES</span></span>

### <span data-ttu-id="d7f7b-108">Пример 1. Добавление переднего порта к шлюзу приложения</span><span class="sxs-lookup"><span data-stu-id="d7f7b-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="d7f7b-109">Первая команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d7f7b-110">Вторая команда добавляет порт 80 в качестве переднего порта шлюза приложения, $AppGw порт FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="d7f7b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7f7b-111">PARAMETERS</span></span>

### <span data-ttu-id="d7f7b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7f7b-112">-ApplicationGateway</span></span>
<span data-ttu-id="d7f7b-113">Указывает шлюз приложения, к которому этот cmdlet добавляет стойкий порт.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="d7f7b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f7b-114">-DefaultProfile</span></span>
<span data-ttu-id="d7f7b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7f7b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d7f7b-116">-Name</span></span>
<span data-ttu-id="d7f7b-117">Указывает имя переднего порта.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="d7f7b-118">-Port</span><span class="sxs-lookup"><span data-stu-id="d7f7b-118">-Port</span></span>
<span data-ttu-id="d7f7b-119">Номер порта.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="d7f7b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f7b-120">CommonParameters</span></span>
<span data-ttu-id="d7f7b-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f7b-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7f7b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f7b-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7f7b-123">INPUTS</span></span>

### <span data-ttu-id="d7f7b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7f7b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d7f7b-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7f7b-125">OUTPUTS</span></span>

### <span data-ttu-id="d7f7b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7f7b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d7f7b-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d7f7b-127">NOTES</span></span>

## <span data-ttu-id="d7f7b-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7f7b-128">RELATED LINKS</span></span>

[<span data-ttu-id="d7f7b-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d7f7b-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d7f7b-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d7f7b-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d7f7b-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d7f7b-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d7f7b-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d7f7b-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


