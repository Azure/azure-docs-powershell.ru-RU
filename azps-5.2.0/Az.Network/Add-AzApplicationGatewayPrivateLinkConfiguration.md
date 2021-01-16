---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399132"
---
# <span data-ttu-id="b9a22-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9a22-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="b9a22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9a22-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a22-103">Добавляет конфигурацию личной ссылки к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="b9a22-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="b9a22-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9a22-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9a22-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9a22-105">DESCRIPTION</span></span>
<span data-ttu-id="b9a22-106">Для шлюза приложения будет добавлена конфигурация закрытой ссылки **Add-AzApplicationGatewayPrivateLinkConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="b9a22-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="b9a22-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9a22-107">EXAMPLES</span></span>

### <span data-ttu-id="b9a22-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9a22-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="b9a22-109">Первая команда создает частную переменнуюLinkIpConfiguration и сохраняет ее в $PrivateLinkIpConfiguration переменной.</span><span class="sxs-lookup"><span data-stu-id="b9a22-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="b9a22-110">Вторая команда получает шлюз приложения ApplicationGateway01, который принадлежит группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw Ресурса.</span><span class="sxs-lookup"><span data-stu-id="b9a22-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b9a22-111">Третья команда добавляет конфигурацию частной ссылки privateLinkConfig01 для шлюза в $AppGw</span><span class="sxs-lookup"><span data-stu-id="b9a22-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="b9a22-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9a22-112">PARAMETERS</span></span>

### <span data-ttu-id="b9a22-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9a22-113">-ApplicationGateway</span></span>
<span data-ttu-id="b9a22-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9a22-114">The applicationGateway</span></span>

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

### <span data-ttu-id="b9a22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a22-115">-DefaultProfile</span></span>
<span data-ttu-id="b9a22-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9a22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9a22-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9a22-117">-IpConfiguration</span></span>
<span data-ttu-id="b9a22-118">Список ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9a22-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9a22-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b9a22-119">-Name</span></span>
<span data-ttu-id="b9a22-120">Имя конфигурации PrivateLink</span><span class="sxs-lookup"><span data-stu-id="b9a22-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="b9a22-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a22-121">CommonParameters</span></span>
<span data-ttu-id="b9a22-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a22-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a22-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9a22-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a22-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9a22-124">INPUTS</span></span>

### <span data-ttu-id="b9a22-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9a22-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="b9a22-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="b9a22-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="b9a22-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9a22-127">OUTPUTS</span></span>

### <span data-ttu-id="b9a22-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9a22-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9a22-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9a22-129">NOTES</span></span>

## <span data-ttu-id="b9a22-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9a22-130">RELATED LINKS</span></span>

[<span data-ttu-id="b9a22-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9a22-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="b9a22-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9a22-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="b9a22-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9a22-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="b9a22-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9a22-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)