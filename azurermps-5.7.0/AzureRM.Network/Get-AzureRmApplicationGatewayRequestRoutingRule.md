---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: d254008ef4d6d4fc6e16f9a543a38518a6537a5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734990"
---
# <span data-ttu-id="b744e-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b744e-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="b744e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b744e-102">SYNOPSIS</span></span>
<span data-ttu-id="b744e-103">Возвращает правило маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b744e-103">Gets the request routing rule of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b744e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b744e-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b744e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b744e-105">DESCRIPTION</span></span>
<span data-ttu-id="b744e-106">Командлет **Get-AzureRmApplicationGatewayRequestRoutingRule** получает правило маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b744e-106">The **Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="b744e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b744e-107">EXAMPLES</span></span>

### <span data-ttu-id="b744e-108">Пример 1: получение определенного правила маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="b744e-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzureRmApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="b744e-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b744e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b744e-110">Вторая команда получает правило маршрутизации запросов с именем Rule01 из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b744e-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="b744e-111">Пример 2: получение списка правил маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="b744e-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="b744e-112">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b744e-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b744e-113">Вторая команда получает список правил маршрутизации запросов из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b744e-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="b744e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b744e-114">PARAMETERS</span></span>

### <span data-ttu-id="b744e-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b744e-115">-ApplicationGateway</span></span>
<span data-ttu-id="b744e-116">Указывает объект шлюза приложения, который содержит правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="b744e-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="b744e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b744e-117">-DefaultProfile</span></span>
<span data-ttu-id="b744e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b744e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b744e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b744e-119">-Name</span></span>
<span data-ttu-id="b744e-120">Указывает имя правила маршрутизации запросов, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b744e-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="b744e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b744e-121">CommonParameters</span></span>
<span data-ttu-id="b744e-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b744e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b744e-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b744e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b744e-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b744e-124">INPUTS</span></span>

### <span data-ttu-id="b744e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b744e-125">System.String</span></span>

## <span data-ttu-id="b744e-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b744e-126">OUTPUTS</span></span>

### <span data-ttu-id="b744e-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b744e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="b744e-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b744e-128">NOTES</span></span>

## <span data-ttu-id="b744e-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b744e-129">RELATED LINKS</span></span>

[<span data-ttu-id="b744e-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b744e-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b744e-131">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b744e-131">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b744e-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b744e-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b744e-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b744e-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


