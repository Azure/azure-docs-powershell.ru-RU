---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 06b7c1fdbd83d90e595683612555c1dca67f23ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568740"
---
# <span data-ttu-id="d5fb7-101">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d5fb7-101">Add-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d5fb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="d5fb7-103">Добавляет порт переднего плана в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="d5fb7-103">Adds a front-end port to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5fb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5fb7-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5fb7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5fb7-105">DESCRIPTION</span></span>
<span data-ttu-id="d5fb7-106">Командлет **Add-AzureRmApplicationGatewayFrontendPort** добавляет порт переднего плана в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="d5fb7-106">The **Add-AzureRmApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="d5fb7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5fb7-107">EXAMPLES</span></span>

### <span data-ttu-id="d5fb7-108">Пример 1: Добавление интерфейсного порта к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="d5fb7-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="d5fb7-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d5fb7-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d5fb7-110">Вторая команда добавляет порт 80 в качестве клиентского порта для шлюза приложения, который хранится в $AppGw, и присваивает имя порту FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="d5fb7-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="d5fb7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5fb7-111">PARAMETERS</span></span>

### <span data-ttu-id="d5fb7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5fb7-112">-ApplicationGateway</span></span>
<span data-ttu-id="d5fb7-113">Указывает шлюз приложений, к которому этот командлет добавляет порт переднего плана.</span><span class="sxs-lookup"><span data-stu-id="d5fb7-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="d5fb7-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5fb7-114">-Name</span></span>
<span data-ttu-id="d5fb7-115">Указывает имя интерфейса переднего порта.</span><span class="sxs-lookup"><span data-stu-id="d5fb7-115">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="d5fb7-116">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="d5fb7-116">-Port</span></span>
<span data-ttu-id="d5fb7-117">Задает номер порта.</span><span class="sxs-lookup"><span data-stu-id="d5fb7-117">Specifies the port number.</span></span>

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

### <span data-ttu-id="d5fb7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5fb7-118">-DefaultProfile</span></span>
<span data-ttu-id="d5fb7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5fb7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5fb7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fb7-120">CommonParameters</span></span>
<span data-ttu-id="d5fb7-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5fb7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fb7-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5fb7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fb7-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5fb7-123">INPUTS</span></span>

### <span data-ttu-id="d5fb7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d5fb7-124">System.String</span></span>

## <span data-ttu-id="d5fb7-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5fb7-125">OUTPUTS</span></span>

### <span data-ttu-id="d5fb7-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5fb7-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d5fb7-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5fb7-127">NOTES</span></span>

## <span data-ttu-id="d5fb7-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5fb7-128">RELATED LINKS</span></span>

[<span data-ttu-id="d5fb7-129">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d5fb7-129">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d5fb7-130">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d5fb7-130">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d5fb7-131">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d5fb7-131">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d5fb7-132">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d5fb7-132">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


