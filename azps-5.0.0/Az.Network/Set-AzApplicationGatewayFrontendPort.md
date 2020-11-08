---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 08637412afafe9220107e95dd3cb7dcc5154ba26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249626"
---
# <span data-ttu-id="8a62b-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8a62b-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="8a62b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a62b-102">SYNOPSIS</span></span>
<span data-ttu-id="8a62b-103">Изменяет интерфейсный порт для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8a62b-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="8a62b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a62b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a62b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a62b-105">DESCRIPTION</span></span>
<span data-ttu-id="8a62b-106">Командлет **Set-AzApplicationGatewayFrontendPort** изменяет интерфейсный порт для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8a62b-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="8a62b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a62b-107">EXAMPLES</span></span>

### <span data-ttu-id="8a62b-108">Пример 1: Установка внешнего порта шлюза приложения в 80</span><span class="sxs-lookup"><span data-stu-id="8a62b-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="8a62b-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8a62b-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8a62b-110">Вторая команда изменяет шлюз в $AppGw для использования порта 80 для клиентского порта с именем FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="8a62b-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="8a62b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a62b-111">PARAMETERS</span></span>

### <span data-ttu-id="8a62b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a62b-112">-ApplicationGateway</span></span>
<span data-ttu-id="8a62b-113">Указывает объект шлюза приложения, с которым этот командлет связывает интерфейсный порт.</span><span class="sxs-lookup"><span data-stu-id="8a62b-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="8a62b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a62b-114">-DefaultProfile</span></span>
<span data-ttu-id="8a62b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a62b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a62b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a62b-116">-Name</span></span>
<span data-ttu-id="8a62b-117">Указывает имя переднего порта, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="8a62b-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="8a62b-118">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="8a62b-118">-Port</span></span>
<span data-ttu-id="8a62b-119">Задает номер порта, который будет использоваться для интерфейса переднего порта.</span><span class="sxs-lookup"><span data-stu-id="8a62b-119">Specifies the port number to use for the front-end port.</span></span>

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

### <span data-ttu-id="8a62b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a62b-120">CommonParameters</span></span>
<span data-ttu-id="8a62b-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a62b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a62b-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a62b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a62b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a62b-123">INPUTS</span></span>

### <span data-ttu-id="8a62b-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a62b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8a62b-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a62b-125">OUTPUTS</span></span>

### <span data-ttu-id="8a62b-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8a62b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8a62b-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a62b-127">NOTES</span></span>

## <span data-ttu-id="8a62b-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a62b-128">RELATED LINKS</span></span>

[<span data-ttu-id="8a62b-129">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8a62b-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8a62b-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8a62b-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8a62b-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8a62b-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8a62b-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8a62b-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
