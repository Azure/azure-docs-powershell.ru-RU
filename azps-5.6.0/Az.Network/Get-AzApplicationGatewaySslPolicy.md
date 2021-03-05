---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 4e15a4296a405a7f0f1e9ac918a5a806603203da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994045"
---
# <span data-ttu-id="e3f80-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e3f80-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e3f80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3f80-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f80-103">Возвращает политику SSL шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e3f80-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="e3f80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e3f80-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3f80-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3f80-105">DESCRIPTION</span></span>
<span data-ttu-id="e3f80-106">Для шлюза приложения политика SSL возвращается **Скайп-AzApplicationGatewaySslPolicy.**</span><span class="sxs-lookup"><span data-stu-id="e3f80-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="e3f80-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e3f80-107">EXAMPLES</span></span>

### <span data-ttu-id="e3f80-108">1:</span><span class="sxs-lookup"><span data-stu-id="e3f80-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="e3f80-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет результат в переменной с $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e3f80-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e3f80-110">Вторая команда получает политику ssl из шлюза приложения, храняного в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e3f80-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="e3f80-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3f80-111">PARAMETERS</span></span>

### <span data-ttu-id="e3f80-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3f80-112">-ApplicationGateway</span></span>
<span data-ttu-id="e3f80-113">Указывает шлюз приложения для политики SSL, которая получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3f80-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e3f80-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f80-114">-DefaultProfile</span></span>
<span data-ttu-id="e3f80-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3f80-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3f80-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f80-116">CommonParameters</span></span>
<span data-ttu-id="e3f80-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f80-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f80-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3f80-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f80-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3f80-119">INPUTS</span></span>

### <span data-ttu-id="e3f80-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3f80-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3f80-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e3f80-121">OUTPUTS</span></span>

### <span data-ttu-id="e3f80-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e3f80-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e3f80-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e3f80-123">NOTES</span></span>
* <span data-ttu-id="e3f80-124">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="e3f80-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e3f80-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3f80-125">RELATED LINKS</span></span>

[<span data-ttu-id="e3f80-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e3f80-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e3f80-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e3f80-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


