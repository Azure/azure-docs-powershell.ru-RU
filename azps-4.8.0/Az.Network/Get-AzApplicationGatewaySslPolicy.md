---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3e7e9559761bce69473511fbd6cdb94d635e13c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236960"
---
# <span data-ttu-id="209c1-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="209c1-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="209c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="209c1-102">SYNOPSIS</span></span>
<span data-ttu-id="209c1-103">Возвращает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="209c1-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="209c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="209c1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="209c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="209c1-105">DESCRIPTION</span></span>
<span data-ttu-id="209c1-106">Командлет **Get-AzApplicationGatewaySslPolicy** получает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="209c1-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="209c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="209c1-107">EXAMPLES</span></span>

### <span data-ttu-id="209c1-108">1:</span><span class="sxs-lookup"><span data-stu-id="209c1-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="209c1-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="209c1-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="209c1-110">Вторая команда получает политику SSL из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="209c1-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="209c1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="209c1-111">PARAMETERS</span></span>

### <span data-ttu-id="209c1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="209c1-112">-ApplicationGateway</span></span>
<span data-ttu-id="209c1-113">Указывает шлюз приложения политики SSL, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="209c1-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="209c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="209c1-114">-DefaultProfile</span></span>
<span data-ttu-id="209c1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="209c1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="209c1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="209c1-116">CommonParameters</span></span>
<span data-ttu-id="209c1-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="209c1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="209c1-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="209c1-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="209c1-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="209c1-119">INPUTS</span></span>

### <span data-ttu-id="209c1-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="209c1-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="209c1-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="209c1-121">OUTPUTS</span></span>

### <span data-ttu-id="209c1-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="209c1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="209c1-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="209c1-123">NOTES</span></span>
* <span data-ttu-id="209c1-124">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="209c1-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="209c1-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="209c1-125">RELATED LINKS</span></span>

[<span data-ttu-id="209c1-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="209c1-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="209c1-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="209c1-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


