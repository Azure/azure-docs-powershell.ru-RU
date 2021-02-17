---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3e7e9559761bce69473511fbd6cdb94d635e13c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226068"
---
# <span data-ttu-id="effd7-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="effd7-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="effd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="effd7-102">SYNOPSIS</span></span>
<span data-ttu-id="effd7-103">Возвращает политику SSL шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="effd7-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="effd7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="effd7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="effd7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="effd7-105">DESCRIPTION</span></span>
<span data-ttu-id="effd7-106">Для шлюза приложения политика SSL возвращается стебом **Get-AzApplicationGatewaySslPolicy.**</span><span class="sxs-lookup"><span data-stu-id="effd7-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="effd7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="effd7-107">EXAMPLES</span></span>

### <span data-ttu-id="effd7-108">1:</span><span class="sxs-lookup"><span data-stu-id="effd7-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="effd7-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет результат в переменной с $AppGW.</span><span class="sxs-lookup"><span data-stu-id="effd7-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="effd7-110">Вторая команда получает политику ssl из шлюза приложения, храняного в переменной с $AppGW.</span><span class="sxs-lookup"><span data-stu-id="effd7-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="effd7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="effd7-111">PARAMETERS</span></span>

### <span data-ttu-id="effd7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="effd7-112">-ApplicationGateway</span></span>
<span data-ttu-id="effd7-113">Указывает шлюз приложения для политики SSL, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="effd7-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="effd7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="effd7-114">-DefaultProfile</span></span>
<span data-ttu-id="effd7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="effd7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="effd7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="effd7-116">CommonParameters</span></span>
<span data-ttu-id="effd7-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="effd7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="effd7-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="effd7-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="effd7-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="effd7-119">INPUTS</span></span>

### <span data-ttu-id="effd7-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="effd7-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="effd7-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="effd7-121">OUTPUTS</span></span>

### <span data-ttu-id="effd7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="effd7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="effd7-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="effd7-123">NOTES</span></span>
* <span data-ttu-id="effd7-124">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="effd7-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="effd7-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="effd7-125">RELATED LINKS</span></span>

[<span data-ttu-id="effd7-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="effd7-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="effd7-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="effd7-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


