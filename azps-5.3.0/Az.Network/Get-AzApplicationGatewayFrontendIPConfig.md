---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 1efce67698ca6d2e3a8bc9eeab3d89e00e1833f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520009"
---
# <span data-ttu-id="e165f-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e165f-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="e165f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e165f-102">SYNOPSIS</span></span>
<span data-ttu-id="e165f-103">Получает конфигурацию переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e165f-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="e165f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e165f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e165f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e165f-105">DESCRIPTION</span></span>
<span data-ttu-id="e165f-106">Для шлюза приложения передовой IP-конфигурацией получается **cmdlet Get-AzApplicationGatewayFrontendIPConfig.**</span><span class="sxs-lookup"><span data-stu-id="e165f-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="e165f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e165f-107">EXAMPLES</span></span>

### <span data-ttu-id="e165f-108">Пример 1. Получить указанную конфигурацию переднего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="e165f-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="e165f-109">Первая команда получает шлюз приложения ApplicationGateway01 из группы ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса. Вторая команда получает от имени FrontEndIP01 конфигурацию переднего IP-адреса из $AppGw и сохраняет ее в переменной $FrontEndIP.</span><span class="sxs-lookup"><span data-stu-id="e165f-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="e165f-110">Пример 2. Получить список конфигураций IP-адресов переднего</span><span class="sxs-lookup"><span data-stu-id="e165f-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="e165f-111">Первая команда получает шлюз приложения ApplicationGateway01 из группы ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса. Вторая команда получает список конфигураций IP-адресов переднего $AppGw и сохраняет его в переменной $FrontEndIPs.</span><span class="sxs-lookup"><span data-stu-id="e165f-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="e165f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e165f-112">PARAMETERS</span></span>

### <span data-ttu-id="e165f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e165f-113">-ApplicationGateway</span></span>
<span data-ttu-id="e165f-114">Определяет объект шлюза приложения, который содержит конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e165f-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="e165f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e165f-115">-DefaultProfile</span></span>
<span data-ttu-id="e165f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e165f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e165f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e165f-117">-Name</span></span>
<span data-ttu-id="e165f-118">Указывает имя ip-конфигурации переднего ip-адреса, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e165f-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e165f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e165f-119">CommonParameters</span></span>
<span data-ttu-id="e165f-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e165f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e165f-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e165f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e165f-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e165f-122">INPUTS</span></span>

### <span data-ttu-id="e165f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e165f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e165f-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e165f-124">OUTPUTS</span></span>

### <span data-ttu-id="e165f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e165f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="e165f-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e165f-126">NOTES</span></span>

## <span data-ttu-id="e165f-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e165f-127">RELATED LINKS</span></span>

[<span data-ttu-id="e165f-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e165f-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e165f-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e165f-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e165f-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e165f-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="e165f-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="e165f-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


