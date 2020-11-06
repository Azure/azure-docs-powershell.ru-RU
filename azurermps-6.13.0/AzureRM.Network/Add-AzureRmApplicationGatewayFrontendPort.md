---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 81952db3ce99ea41388d85085d58a2fb54ccc63f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567727"
---
# <span data-ttu-id="b7a26-101">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b7a26-101">Add-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="b7a26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7a26-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a26-103">Добавляет порт переднего плана в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b7a26-103">Adds a front-end port to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7a26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7a26-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7a26-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7a26-105">DESCRIPTION</span></span>
<span data-ttu-id="b7a26-106">Командлет **Add-AzureRmApplicationGatewayFrontendPort** добавляет порт переднего плана в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b7a26-106">The **Add-AzureRmApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="b7a26-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7a26-107">EXAMPLES</span></span>

### <span data-ttu-id="b7a26-108">Пример 1: Добавление интерфейсного порта к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="b7a26-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="b7a26-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b7a26-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b7a26-110">Вторая команда добавляет порт 80 в качестве клиентского порта для шлюза приложения, который хранится в $AppGw, и присваивает имя порту FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="b7a26-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="b7a26-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7a26-111">PARAMETERS</span></span>

### <span data-ttu-id="b7a26-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7a26-112">-ApplicationGateway</span></span>
<span data-ttu-id="b7a26-113">Указывает шлюз приложений, к которому этот командлет добавляет порт переднего плана.</span><span class="sxs-lookup"><span data-stu-id="b7a26-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="b7a26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a26-114">-DefaultProfile</span></span>
<span data-ttu-id="b7a26-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a26-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7a26-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7a26-116">-Name</span></span>
<span data-ttu-id="b7a26-117">Указывает имя интерфейса переднего порта.</span><span class="sxs-lookup"><span data-stu-id="b7a26-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="b7a26-118">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="b7a26-118">-Port</span></span>
<span data-ttu-id="b7a26-119">Задает номер порта.</span><span class="sxs-lookup"><span data-stu-id="b7a26-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="b7a26-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a26-120">CommonParameters</span></span>
<span data-ttu-id="b7a26-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7a26-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a26-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7a26-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a26-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7a26-123">INPUTS</span></span>

### <span data-ttu-id="b7a26-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7a26-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="b7a26-125">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b7a26-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="b7a26-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7a26-126">OUTPUTS</span></span>

### <span data-ttu-id="b7a26-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7a26-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b7a26-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7a26-128">NOTES</span></span>

## <span data-ttu-id="b7a26-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7a26-129">RELATED LINKS</span></span>

[<span data-ttu-id="b7a26-130">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b7a26-130">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b7a26-131">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b7a26-131">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b7a26-132">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b7a26-132">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b7a26-133">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b7a26-133">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


