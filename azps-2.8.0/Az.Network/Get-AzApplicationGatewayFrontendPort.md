---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 92549d4f6a7573bb5a81444dab8eb358f721fe22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902509"
---
# <span data-ttu-id="5a444-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a444-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5a444-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a444-102">SYNOPSIS</span></span>
<span data-ttu-id="5a444-103">Получает интерфейсный порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="5a444-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="5a444-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a444-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a444-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a444-105">DESCRIPTION</span></span>
<span data-ttu-id="5a444-106">Командлет **Get-AzApplicationGatewayFrontendPort** получает интерфейсный порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="5a444-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="5a444-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a444-107">EXAMPLES</span></span>

### <span data-ttu-id="5a444-108">Пример 1: получение указанного клиентского порта</span><span class="sxs-lookup"><span data-stu-id="5a444-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="5a444-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5a444-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5a444-110">Вторая команда получает интерфейсный порт с именем FrontEndPort01 from $AppGw и сохраняет его в переменной $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="5a444-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="5a444-111">Пример 2: получение списка внешних портов</span><span class="sxs-lookup"><span data-stu-id="5a444-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="5a444-112">Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5a444-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5a444-113">Вторая команда возвращает список портов переднего плана из $AppGw и сохраняет их в переменной $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="5a444-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="5a444-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a444-114">PARAMETERS</span></span>

### <span data-ttu-id="5a444-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a444-115">-ApplicationGateway</span></span>
<span data-ttu-id="5a444-116">Указывает объект шлюза приложения, который содержит интерфейсный порт.</span><span class="sxs-lookup"><span data-stu-id="5a444-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="5a444-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a444-117">-DefaultProfile</span></span>
<span data-ttu-id="5a444-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a444-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a444-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5a444-119">-Name</span></span>
<span data-ttu-id="5a444-120">Указывает имя внешнего порта для получения.</span><span class="sxs-lookup"><span data-stu-id="5a444-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="5a444-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a444-121">CommonParameters</span></span>
<span data-ttu-id="5a444-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a444-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a444-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a444-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a444-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a444-124">INPUTS</span></span>

### <span data-ttu-id="5a444-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a444-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5a444-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a444-126">OUTPUTS</span></span>

### <span data-ttu-id="5a444-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a444-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5a444-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a444-128">NOTES</span></span>

## <span data-ttu-id="5a444-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a444-129">RELATED LINKS</span></span>

[<span data-ttu-id="5a444-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a444-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5a444-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a444-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5a444-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a444-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5a444-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5a444-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


