---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 6f93a66739fe1943182726e6998267d1e406f0a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902998"
---
# <span data-ttu-id="ad517-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ad517-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="ad517-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad517-102">SYNOPSIS</span></span>
<span data-ttu-id="ad517-103">Возвращает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ad517-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="ad517-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad517-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad517-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad517-105">DESCRIPTION</span></span>
<span data-ttu-id="ad517-106">Командлет **Get-AzApplicationGatewaySslPolicy** получает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ad517-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="ad517-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad517-107">EXAMPLES</span></span>

### <span data-ttu-id="ad517-108">1:</span><span class="sxs-lookup"><span data-stu-id="ad517-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="ad517-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="ad517-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="ad517-110">Вторая команда получает политику SSL из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="ad517-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="ad517-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad517-111">PARAMETERS</span></span>

### <span data-ttu-id="ad517-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ad517-112">-ApplicationGateway</span></span>
<span data-ttu-id="ad517-113">Указывает шлюз приложения политики SSL, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ad517-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ad517-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad517-114">-DefaultProfile</span></span>
<span data-ttu-id="ad517-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad517-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad517-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad517-116">CommonParameters</span></span>
<span data-ttu-id="ad517-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad517-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad517-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad517-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad517-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad517-119">INPUTS</span></span>

### <span data-ttu-id="ad517-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ad517-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ad517-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad517-121">OUTPUTS</span></span>

### <span data-ttu-id="ad517-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ad517-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="ad517-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad517-123">NOTES</span></span>
* <span data-ttu-id="ad517-124">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="ad517-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ad517-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad517-125">RELATED LINKS</span></span>

[<span data-ttu-id="ad517-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ad517-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="ad517-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="ad517-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


