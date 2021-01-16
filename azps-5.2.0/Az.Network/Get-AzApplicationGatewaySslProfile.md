---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 6d4bab8f7c4c766730dd6fb09f0d0a011d5d3739
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396367"
---
# <span data-ttu-id="49bc0-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="49bc0-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="49bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="49bc0-103">Возвращает SSL-профиль шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="49bc0-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="49bc0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49bc0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49bc0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49bc0-105">DESCRIPTION</span></span>
<span data-ttu-id="49bc0-106">**Cmdlet Get-AzApplicationGatewaySslProfile** получает профиль SSL шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="49bc0-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="49bc0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49bc0-107">EXAMPLES</span></span>

### <span data-ttu-id="49bc0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49bc0-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="49bc0-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной. Вторая команда получает профиль SSL SslProfile01 для $AppGw и сохраняет его в $profile переменной.</span><span class="sxs-lookup"><span data-stu-id="49bc0-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="49bc0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49bc0-110">PARAMETERS</span></span>

### <span data-ttu-id="49bc0-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49bc0-111">-ApplicationGateway</span></span>
<span data-ttu-id="49bc0-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49bc0-112">The applicationGateway</span></span>

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

### <span data-ttu-id="49bc0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49bc0-113">-DefaultProfile</span></span>
<span data-ttu-id="49bc0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49bc0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49bc0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="49bc0-115">-Name</span></span>
<span data-ttu-id="49bc0-116">Имя профиля SSL</span><span class="sxs-lookup"><span data-stu-id="49bc0-116">The name of the ssl profile</span></span>

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

### <span data-ttu-id="49bc0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49bc0-117">CommonParameters</span></span>
<span data-ttu-id="49bc0-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49bc0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49bc0-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49bc0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49bc0-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49bc0-120">INPUTS</span></span>

### <span data-ttu-id="49bc0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49bc0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="49bc0-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49bc0-122">OUTPUTS</span></span>

### <span data-ttu-id="49bc0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="49bc0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="49bc0-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49bc0-124">NOTES</span></span>

## <span data-ttu-id="49bc0-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49bc0-125">RELATED LINKS</span></span>

[<span data-ttu-id="49bc0-126">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="49bc0-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="49bc0-127">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="49bc0-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="49bc0-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="49bc0-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="49bc0-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="49bc0-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)