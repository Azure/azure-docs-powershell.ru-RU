---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: a1e6bd507b7ddcc0a70405136cb76bba9231a7f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396359"
---
# <span data-ttu-id="50bf7-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="50bf7-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="50bf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50bf7-102">SYNOPSIS</span></span>
<span data-ttu-id="50bf7-103">Возвращает SSL-политику SSL-профиля шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="50bf7-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="50bf7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50bf7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50bf7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50bf7-105">DESCRIPTION</span></span>
<span data-ttu-id="50bf7-106">Для SSL-профиля шлюза приложения возвращается политика SSL **для get-AzApplicationGatewaySslProfilePolicy.**</span><span class="sxs-lookup"><span data-stu-id="50bf7-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="50bf7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50bf7-107">EXAMPLES</span></span>

### <span data-ttu-id="50bf7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50bf7-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="50bf7-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="50bf7-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="50bf7-110">Вторая команда получает профиль SSL с именем SslProfile01 для $AppGw и сохраняет его $SslProfile переменной.</span><span class="sxs-lookup"><span data-stu-id="50bf7-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="50bf7-111">Последняя команда получает политику SSL из профиля SSL$SslProfile и сохраняет ее в переменной $sslpolicy.</span><span class="sxs-lookup"><span data-stu-id="50bf7-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="50bf7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50bf7-112">PARAMETERS</span></span>

### <span data-ttu-id="50bf7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50bf7-113">-DefaultProfile</span></span>
<span data-ttu-id="50bf7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50bf7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50bf7-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="50bf7-115">-SslProfile</span></span>
<span data-ttu-id="50bf7-116">SSL-профиль шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="50bf7-116">The application Gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50bf7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50bf7-117">CommonParameters</span></span>
<span data-ttu-id="50bf7-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50bf7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50bf7-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50bf7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50bf7-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50bf7-120">INPUTS</span></span>

### <span data-ttu-id="50bf7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="50bf7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="50bf7-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50bf7-122">OUTPUTS</span></span>

### <span data-ttu-id="50bf7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="50bf7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="50bf7-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50bf7-124">NOTES</span></span>

## <span data-ttu-id="50bf7-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50bf7-125">RELATED LINKS</span></span>

[<span data-ttu-id="50bf7-126">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="50bf7-126">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="50bf7-127">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="50bf7-127">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="50bf7-128">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="50bf7-128">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="50bf7-129">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="50bf7-129">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)