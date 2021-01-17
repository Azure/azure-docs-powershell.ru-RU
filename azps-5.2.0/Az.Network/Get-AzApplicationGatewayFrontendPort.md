---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326315"
---
# <span data-ttu-id="e300d-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e300d-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="e300d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e300d-102">SYNOPSIS</span></span>
<span data-ttu-id="e300d-103">Получение переднего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e300d-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="e300d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e300d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e300d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e300d-105">DESCRIPTION</span></span>
<span data-ttu-id="e300d-106">Для шлюза приложения требуется ли вам порт Переднего шлюза приложения, с его наступлении **cmdlet Get-AzApplicationGatewayFrontendPort.**</span><span class="sxs-lookup"><span data-stu-id="e300d-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="e300d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e300d-107">EXAMPLES</span></span>

### <span data-ttu-id="e300d-108">Пример 1. Получить указанный передней порт</span><span class="sxs-lookup"><span data-stu-id="e300d-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="e300d-109">Первая команда получает шлюз приложения ApplicationGateway01 из группы ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="e300d-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e300d-110">Вторая команда получает от имени frontEndPort01 порт переднего $AppGw и сохраняет его в переменной $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="e300d-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="e300d-111">Пример 2. Получить список переднего порта</span><span class="sxs-lookup"><span data-stu-id="e300d-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="e300d-112">Первая команда получает шлюз приложения ApplicationGateway01 из группы ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="e300d-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e300d-113">Вторая команда получает список переднего порта из $AppGw и сохраняет его в переменной $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="e300d-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="e300d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e300d-114">PARAMETERS</span></span>

### <span data-ttu-id="e300d-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e300d-115">-ApplicationGateway</span></span>
<span data-ttu-id="e300d-116">Определяет объект шлюза приложения, содержащий порт переднего.</span><span class="sxs-lookup"><span data-stu-id="e300d-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="e300d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e300d-117">-DefaultProfile</span></span>
<span data-ttu-id="e300d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e300d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e300d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e300d-119">-Name</span></span>
<span data-ttu-id="e300d-120">Указывает имя переднего порта, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="e300d-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="e300d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e300d-121">CommonParameters</span></span>
<span data-ttu-id="e300d-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e300d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e300d-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e300d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e300d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e300d-124">INPUTS</span></span>

### <span data-ttu-id="e300d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e300d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e300d-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e300d-126">OUTPUTS</span></span>

### <span data-ttu-id="e300d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e300d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="e300d-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e300d-128">NOTES</span></span>

## <span data-ttu-id="e300d-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e300d-129">RELATED LINKS</span></span>

[<span data-ttu-id="e300d-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e300d-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e300d-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e300d-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e300d-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e300d-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e300d-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e300d-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


