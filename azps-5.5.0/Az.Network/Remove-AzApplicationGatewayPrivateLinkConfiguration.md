---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227585"
---
# <span data-ttu-id="9ca44-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ca44-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="9ca44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ca44-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca44-103">Удаляет конфигурацию PrivateLink из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9ca44-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="9ca44-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ca44-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ca44-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ca44-105">DESCRIPTION</span></span>
<span data-ttu-id="9ca44-106">С **его** использованием можно удалить конфигурацию PrivateLink из шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="9ca44-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="9ca44-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ca44-107">EXAMPLES</span></span>

### <span data-ttu-id="9ca44-108">Пример 1. Удаление конфигурации PrivateLink шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="9ca44-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="9ca44-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9ca44-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9ca44-110">Вторая команда удаляет конфигурацию PrivateLink с именем privateLinkConfig01 из шлюза приложения, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9ca44-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="9ca44-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ca44-111">PARAMETERS</span></span>

### <span data-ttu-id="9ca44-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ca44-112">-ApplicationGateway</span></span>
<span data-ttu-id="9ca44-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ca44-113">The applicationGateway</span></span>

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

### <span data-ttu-id="9ca44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca44-114">-DefaultProfile</span></span>
<span data-ttu-id="9ca44-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ca44-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ca44-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9ca44-116">-Name</span></span>
<span data-ttu-id="9ca44-117">Имя конфигурации PrivateLink шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="9ca44-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="9ca44-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca44-118">CommonParameters</span></span>
<span data-ttu-id="9ca44-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ca44-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca44-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ca44-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca44-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ca44-121">INPUTS</span></span>

### <span data-ttu-id="9ca44-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ca44-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ca44-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ca44-123">OUTPUTS</span></span>

### <span data-ttu-id="9ca44-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ca44-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ca44-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ca44-125">NOTES</span></span>

## <span data-ttu-id="9ca44-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ca44-126">RELATED LINKS</span></span>

[<span data-ttu-id="9ca44-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ca44-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="9ca44-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ca44-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="9ca44-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ca44-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="9ca44-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ca44-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)