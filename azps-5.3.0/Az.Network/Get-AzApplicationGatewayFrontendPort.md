---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520007"
---
# <span data-ttu-id="1067f-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1067f-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="1067f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1067f-102">SYNOPSIS</span></span>
<span data-ttu-id="1067f-103">Получение переднего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1067f-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="1067f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1067f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1067f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1067f-105">DESCRIPTION</span></span>
<span data-ttu-id="1067f-106">Для шлюза приложения требуется ли вам порт Переднего шлюза приложения, с его наступлении **cmdlet Get-AzApplicationGatewayFrontendPort.**</span><span class="sxs-lookup"><span data-stu-id="1067f-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="1067f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1067f-107">EXAMPLES</span></span>

### <span data-ttu-id="1067f-108">Пример 1. Получить указанный передней порт</span><span class="sxs-lookup"><span data-stu-id="1067f-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="1067f-109">Первая команда получает шлюз приложения ApplicationGateway01 из группы ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="1067f-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1067f-110">Вторая команда получает от имени frontEndPort01 порт переднего $AppGw и сохраняет его в переменной $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="1067f-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="1067f-111">Пример 2. Получить список переднего порта</span><span class="sxs-lookup"><span data-stu-id="1067f-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="1067f-112">Первая команда получает шлюз приложения ApplicationGateway01 из группы ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="1067f-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1067f-113">Вторая команда получает список переднего порта из $AppGw и сохраняет его в переменной $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="1067f-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="1067f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1067f-114">PARAMETERS</span></span>

### <span data-ttu-id="1067f-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1067f-115">-ApplicationGateway</span></span>
<span data-ttu-id="1067f-116">Определяет объект шлюза приложения, содержащий порт переднего.</span><span class="sxs-lookup"><span data-stu-id="1067f-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="1067f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1067f-117">-DefaultProfile</span></span>
<span data-ttu-id="1067f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1067f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1067f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1067f-119">-Name</span></span>
<span data-ttu-id="1067f-120">Указывает имя переднего порта, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="1067f-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="1067f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1067f-121">CommonParameters</span></span>
<span data-ttu-id="1067f-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1067f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1067f-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1067f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1067f-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1067f-124">INPUTS</span></span>

### <span data-ttu-id="1067f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1067f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1067f-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1067f-126">OUTPUTS</span></span>

### <span data-ttu-id="1067f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1067f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="1067f-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1067f-128">NOTES</span></span>

## <span data-ttu-id="1067f-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1067f-129">RELATED LINKS</span></span>

[<span data-ttu-id="1067f-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1067f-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="1067f-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1067f-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="1067f-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1067f-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="1067f-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1067f-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


