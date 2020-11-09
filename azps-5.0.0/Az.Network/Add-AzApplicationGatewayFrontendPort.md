---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9cd7cd0b859ff806b084ebfe1c76e07aed3a7c43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316128"
---
# <span data-ttu-id="c7aef-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7aef-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c7aef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7aef-102">SYNOPSIS</span></span>
<span data-ttu-id="c7aef-103">Добавляет порт переднего плана в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c7aef-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="c7aef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7aef-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7aef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7aef-105">DESCRIPTION</span></span>
<span data-ttu-id="c7aef-106">Командлет **Add-AzApplicationGatewayFrontendPort** добавляет порт переднего плана в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c7aef-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="c7aef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7aef-107">EXAMPLES</span></span>

### <span data-ttu-id="c7aef-108">Пример 1: Добавление интерфейсного порта к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="c7aef-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="c7aef-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c7aef-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c7aef-110">Вторая команда добавляет порт 80 в качестве клиентского порта для шлюза приложения, который хранится в $AppGw, и присваивает имя порту FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="c7aef-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="c7aef-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7aef-111">PARAMETERS</span></span>

### <span data-ttu-id="c7aef-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7aef-112">-ApplicationGateway</span></span>
<span data-ttu-id="c7aef-113">Указывает шлюз приложений, к которому этот командлет добавляет порт переднего плана.</span><span class="sxs-lookup"><span data-stu-id="c7aef-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="c7aef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7aef-114">-DefaultProfile</span></span>
<span data-ttu-id="c7aef-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7aef-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7aef-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7aef-116">-Name</span></span>
<span data-ttu-id="c7aef-117">Указывает имя интерфейса переднего порта.</span><span class="sxs-lookup"><span data-stu-id="c7aef-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="c7aef-118">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="c7aef-118">-Port</span></span>
<span data-ttu-id="c7aef-119">Задает номер порта.</span><span class="sxs-lookup"><span data-stu-id="c7aef-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="c7aef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7aef-120">CommonParameters</span></span>
<span data-ttu-id="c7aef-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7aef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7aef-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7aef-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7aef-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7aef-123">INPUTS</span></span>

### <span data-ttu-id="c7aef-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7aef-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c7aef-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7aef-125">OUTPUTS</span></span>

### <span data-ttu-id="c7aef-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7aef-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c7aef-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7aef-127">NOTES</span></span>

## <span data-ttu-id="c7aef-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7aef-128">RELATED LINKS</span></span>

[<span data-ttu-id="c7aef-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7aef-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c7aef-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7aef-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c7aef-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7aef-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c7aef-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7aef-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


