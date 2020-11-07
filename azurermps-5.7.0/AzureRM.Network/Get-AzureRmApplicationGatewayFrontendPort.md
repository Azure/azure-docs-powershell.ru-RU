---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 1f347545fd5bf53eeb5b083410c919ce1c602553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733020"
---
# <span data-ttu-id="ad3a5-101">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ad3a5-101">Get-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="ad3a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad3a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3a5-103">Получает интерфейсный порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ad3a5-103">Gets the front-end port of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad3a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad3a5-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad3a5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad3a5-105">DESCRIPTION</span></span>
<span data-ttu-id="ad3a5-106">Командлет **Get-AzureRmApplicationGatewayFrontendPort** получает интерфейсный порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ad3a5-106">The **Get-AzureRmApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="ad3a5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad3a5-107">EXAMPLES</span></span>

### <span data-ttu-id="ad3a5-108">Пример 1: получение указанного клиентского порта</span><span class="sxs-lookup"><span data-stu-id="ad3a5-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzureRmApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="ad3a5-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ad3a5-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ad3a5-110">Вторая команда получает интерфейсный порт с именем FrontEndPort01 from $AppGw и сохраняет его в переменной $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="ad3a5-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="ad3a5-111">Пример 2: получение списка внешних портов</span><span class="sxs-lookup"><span data-stu-id="ad3a5-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzureRmApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="ad3a5-112">Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ad3a5-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ad3a5-113">Вторая команда возвращает список портов переднего плана из $AppGw и сохраняет их в переменной $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="ad3a5-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="ad3a5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad3a5-114">PARAMETERS</span></span>

### <span data-ttu-id="ad3a5-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ad3a5-115">-ApplicationGateway</span></span>
<span data-ttu-id="ad3a5-116">Указывает объект шлюза приложения, который содержит интерфейсный порт.</span><span class="sxs-lookup"><span data-stu-id="ad3a5-116">Specifies the application gateway object that contains the front-end port.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad3a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3a5-117">-DefaultProfile</span></span>
<span data-ttu-id="ad3a5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad3a5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3a5-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad3a5-119">-Name</span></span>
<span data-ttu-id="ad3a5-120">Указывает имя внешнего порта для получения.</span><span class="sxs-lookup"><span data-stu-id="ad3a5-120">Specifies the name of the front-end port to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad3a5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3a5-121">CommonParameters</span></span>
<span data-ttu-id="ad3a5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad3a5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3a5-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad3a5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3a5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad3a5-124">INPUTS</span></span>

### <span data-ttu-id="ad3a5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ad3a5-125">System.String</span></span>

## <span data-ttu-id="ad3a5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad3a5-126">OUTPUTS</span></span>

### <span data-ttu-id="ad3a5-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ad3a5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="ad3a5-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad3a5-128">NOTES</span></span>

## <span data-ttu-id="ad3a5-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad3a5-129">RELATED LINKS</span></span>

[<span data-ttu-id="ad3a5-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ad3a5-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ad3a5-131">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ad3a5-131">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ad3a5-132">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ad3a5-132">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ad3a5-133">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ad3a5-133">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


