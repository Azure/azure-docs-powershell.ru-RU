---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: eee7040dab93a4f73bacdf440c6450a525fab9a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326356"
---
# <span data-ttu-id="1e4ff-101">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e4ff-101">Get-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="1e4ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4ff-103">Получает конфигурацию проверки подлинности клиента для объекта профиля SSL.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-103">Gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="1e4ff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1e4ff-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e4ff-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e4ff-105">DESCRIPTION</span></span>
<span data-ttu-id="1e4ff-106">Чтобы получить конфигурацию проверки подлинности клиента для объекта профиля SSL, можно выбрать cmdlet **Get-AzApplicationGateClientAuthConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="1e4ff-106">The **Get-AzApplicationGatewayClientAuthConfiguration** cmdlet gets the client authentication configuration of a SSL profile object.</span></span>

## <span data-ttu-id="1e4ff-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1e4ff-107">EXAMPLES</span></span>

### <span data-ttu-id="1e4ff-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1e4ff-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

<span data-ttu-id="1e4ff-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="1e4ff-110">Вторая команда получает профиль SSL с именем SslProfile01 для $AppGw и сохраняет его $SslProfile переменной.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="1e4ff-111">Последняя команда получает конфигурацию проверки подлинности клиента из профиля SSL$SslProfile и сохраняет ее в $ClientAuthConfig переменной.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-111">The last command gets the client authentication configuration from the SSL profile $SslProfile and stores it in the $ClientAuthConfig variable.</span></span>

## <span data-ttu-id="1e4ff-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e4ff-112">PARAMETERS</span></span>

### <span data-ttu-id="1e4ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4ff-113">-DefaultProfile</span></span>
<span data-ttu-id="1e4ff-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e4ff-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="1e4ff-115">-SslProfile</span></span>
<span data-ttu-id="1e4ff-116">Профиль SSL</span><span class="sxs-lookup"><span data-stu-id="1e4ff-116">The ssl profile</span></span>

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

### <span data-ttu-id="1e4ff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4ff-117">CommonParameters</span></span>
<span data-ttu-id="1e4ff-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e4ff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4ff-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e4ff-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4ff-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e4ff-120">INPUTS</span></span>

### <span data-ttu-id="1e4ff-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1e4ff-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1e4ff-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1e4ff-122">OUTPUTS</span></span>

### <span data-ttu-id="1e4ff-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e4ff-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="1e4ff-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1e4ff-124">NOTES</span></span>

## <span data-ttu-id="1e4ff-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e4ff-125">RELATED LINKS</span></span>

[<span data-ttu-id="1e4ff-126">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e4ff-126">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1e4ff-127">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e4ff-127">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1e4ff-128">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e4ff-128">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="1e4ff-129">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e4ff-129">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)