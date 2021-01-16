---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ded757d1e81ef5db94157f4676ed91dc11680fd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327546"
---
# <span data-ttu-id="d3f73-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d3f73-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="d3f73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3f73-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f73-103">Удаляет профиль ssl из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d3f73-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="d3f73-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3f73-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3f73-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3f73-105">DESCRIPTION</span></span>
<span data-ttu-id="d3f73-106">Для удаления профиля SSL из шлюза приложения удаляется **cmdlet Remove-AzApplicationGatewaySslProfile.**</span><span class="sxs-lookup"><span data-stu-id="d3f73-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="d3f73-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3f73-107">EXAMPLES</span></span>

### <span data-ttu-id="d3f73-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d3f73-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="d3f73-109">Первая команда получает шлюз приложения ApplicationGateway01, который принадлежит группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="d3f73-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="d3f73-110">Вторая команда удаляет SSL-профиль с именем SslProfile01 из шлюза приложения, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d3f73-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d3f73-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3f73-111">PARAMETERS</span></span>

### <span data-ttu-id="d3f73-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3f73-112">-ApplicationGateway</span></span>
<span data-ttu-id="d3f73-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3f73-113">The applicationGateway</span></span>

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

### <span data-ttu-id="d3f73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f73-114">-DefaultProfile</span></span>
<span data-ttu-id="d3f73-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f73-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3f73-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d3f73-116">-Name</span></span>
<span data-ttu-id="d3f73-117">Имя профиля SSL</span><span class="sxs-lookup"><span data-stu-id="d3f73-117">The name of the ssl profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f73-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f73-118">CommonParameters</span></span>
<span data-ttu-id="d3f73-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f73-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f73-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3f73-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f73-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3f73-121">INPUTS</span></span>

### <span data-ttu-id="d3f73-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3f73-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d3f73-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3f73-123">OUTPUTS</span></span>

### <span data-ttu-id="d3f73-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3f73-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d3f73-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3f73-125">NOTES</span></span>

## <span data-ttu-id="d3f73-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3f73-126">RELATED LINKS</span></span>

[<span data-ttu-id="d3f73-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d3f73-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d3f73-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d3f73-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d3f73-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d3f73-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="d3f73-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="d3f73-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)