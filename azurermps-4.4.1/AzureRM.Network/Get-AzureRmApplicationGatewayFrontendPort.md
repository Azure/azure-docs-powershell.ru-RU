---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: f0a897dfcc68d2313326d974d1b5a172bd79db6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559688"
---
# <span data-ttu-id="49b85-101">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="49b85-101">Get-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="49b85-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49b85-102">SYNOPSIS</span></span>
<span data-ttu-id="49b85-103">Получает интерфейсный порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="49b85-103">Gets the front-end port of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49b85-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49b85-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49b85-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49b85-105">DESCRIPTION</span></span>
<span data-ttu-id="49b85-106">Командлет **Get-AzureRmApplicationGatewayFrontendPort** получает интерфейсный порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="49b85-106">The **Get-AzureRmApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="49b85-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49b85-107">EXAMPLES</span></span>

### <span data-ttu-id="49b85-108">Пример 1: получение указанного клиентского порта</span><span class="sxs-lookup"><span data-stu-id="49b85-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzureRmApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="49b85-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="49b85-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="49b85-110">Вторая команда получает интерфейсный порт с именем FrontEndPort01 from $AppGw и сохраняет его в переменной $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="49b85-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="49b85-111">Пример 2: получение списка внешних портов</span><span class="sxs-lookup"><span data-stu-id="49b85-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzureRmApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="49b85-112">Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="49b85-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="49b85-113">Вторая команда возвращает список портов переднего плана из $AppGw и сохраняет их в переменной $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="49b85-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="49b85-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49b85-114">PARAMETERS</span></span>

### <span data-ttu-id="49b85-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49b85-115">-ApplicationGateway</span></span>
<span data-ttu-id="49b85-116">Указывает объект шлюза приложения, который содержит интерфейсный порт.</span><span class="sxs-lookup"><span data-stu-id="49b85-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="49b85-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49b85-117">-Name</span></span>
<span data-ttu-id="49b85-118">Указывает имя внешнего порта для получения.</span><span class="sxs-lookup"><span data-stu-id="49b85-118">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="49b85-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b85-119">-DefaultProfile</span></span>
<span data-ttu-id="49b85-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49b85-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b85-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b85-121">CommonParameters</span></span>
<span data-ttu-id="49b85-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49b85-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b85-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49b85-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b85-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49b85-124">INPUTS</span></span>

### <span data-ttu-id="49b85-125">System. String</span><span class="sxs-lookup"><span data-stu-id="49b85-125">System.String</span></span>

## <span data-ttu-id="49b85-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49b85-126">OUTPUTS</span></span>

### <span data-ttu-id="49b85-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="49b85-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="49b85-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="49b85-128">NOTES</span></span>

## <span data-ttu-id="49b85-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49b85-129">RELATED LINKS</span></span>

[<span data-ttu-id="49b85-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="49b85-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="49b85-131">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="49b85-131">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="49b85-132">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="49b85-132">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="49b85-133">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="49b85-133">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


