---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 402084acc332102c8a2f003e31e140b175b6f22f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910069"
---
# <span data-ttu-id="8fab1-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8fab1-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="8fab1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8fab1-102">SYNOPSIS</span></span>
<span data-ttu-id="8fab1-103">Возвращает правило маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8fab1-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="8fab1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8fab1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fab1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fab1-105">DESCRIPTION</span></span>
<span data-ttu-id="8fab1-106">Командлет **Get-AzApplicationGatewayRequestRoutingRule** получает правило маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8fab1-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="8fab1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8fab1-107">EXAMPLES</span></span>

### <span data-ttu-id="8fab1-108">Пример 1: получение определенного правила маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="8fab1-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="8fab1-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="8fab1-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="8fab1-110">Вторая команда получает правило маршрутизации запросов с именем Rule01 из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="8fab1-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="8fab1-111">Пример 2: получение списка правил маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="8fab1-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="8fab1-112">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="8fab1-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="8fab1-113">Вторая команда получает список правил маршрутизации запросов из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="8fab1-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="8fab1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8fab1-114">PARAMETERS</span></span>

### <span data-ttu-id="8fab1-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8fab1-115">-ApplicationGateway</span></span>
<span data-ttu-id="8fab1-116">Указывает объект шлюза приложения, который содержит правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="8fab1-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="8fab1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fab1-117">-DefaultProfile</span></span>
<span data-ttu-id="8fab1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8fab1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fab1-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8fab1-119">-Name</span></span>
<span data-ttu-id="8fab1-120">Указывает имя правила маршрутизации запросов, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8fab1-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="8fab1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fab1-121">CommonParameters</span></span>
<span data-ttu-id="8fab1-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8fab1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fab1-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fab1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fab1-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8fab1-124">INPUTS</span></span>

### <span data-ttu-id="8fab1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8fab1-125">System.String</span></span>

## <span data-ttu-id="8fab1-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fab1-126">OUTPUTS</span></span>

### <span data-ttu-id="8fab1-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8fab1-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="8fab1-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8fab1-128">NOTES</span></span>

## <span data-ttu-id="8fab1-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8fab1-129">RELATED LINKS</span></span>

[<span data-ttu-id="8fab1-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8fab1-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8fab1-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8fab1-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8fab1-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8fab1-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8fab1-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8fab1-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


