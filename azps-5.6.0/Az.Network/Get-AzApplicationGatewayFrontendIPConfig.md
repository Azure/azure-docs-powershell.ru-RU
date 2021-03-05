---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: cab20e2b92343549b5138f14f88505c70624effb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996551"
---
# <span data-ttu-id="380b7-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="380b7-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="380b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="380b7-102">SYNOPSIS</span></span>
<span data-ttu-id="380b7-103">Получает конфигурацию ПЕРЕДНЕГО IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="380b7-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="380b7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="380b7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="380b7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="380b7-105">DESCRIPTION</span></span>
<span data-ttu-id="380b7-106">Для шлюза приложения будет задана конфигурация IP-адреса переднего ip-адреса **Get-AzApplicationGatewayFrontendIPConfig.**</span><span class="sxs-lookup"><span data-stu-id="380b7-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="380b7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="380b7-107">EXAMPLES</span></span>

### <span data-ttu-id="380b7-108">Пример 1. Получить указанную конфигурацию переднего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="380b7-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="380b7-109">Первая команда получает шлюз приложения ApplicationGateway01 из группы ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса. Вторая команда получает от имени FrontEndIP01 конфигурацию переднего IP-адреса из $AppGw и сохраняет ее в переменной $FrontEndIP.</span><span class="sxs-lookup"><span data-stu-id="380b7-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="380b7-110">Пример 2. Получить список конфигураций IP-адресов переднего</span><span class="sxs-lookup"><span data-stu-id="380b7-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="380b7-111">Первая команда получает шлюз приложения ApplicationGateway01 из группы ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса. Вторая команда получает список конфигураций IP-адресов переднего $AppGw и сохраняет его в переменной $FrontEndIPs.</span><span class="sxs-lookup"><span data-stu-id="380b7-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="380b7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="380b7-112">PARAMETERS</span></span>

### <span data-ttu-id="380b7-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="380b7-113">-ApplicationGateway</span></span>
<span data-ttu-id="380b7-114">Определяет объект шлюза приложения, который содержит конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="380b7-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="380b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380b7-115">-DefaultProfile</span></span>
<span data-ttu-id="380b7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="380b7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="380b7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="380b7-117">-Name</span></span>
<span data-ttu-id="380b7-118">Указывает имя ip-конфигурации переднего ip-адреса, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="380b7-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="380b7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380b7-119">CommonParameters</span></span>
<span data-ttu-id="380b7-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="380b7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380b7-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="380b7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380b7-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="380b7-122">INPUTS</span></span>

### <span data-ttu-id="380b7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="380b7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="380b7-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="380b7-124">OUTPUTS</span></span>

### <span data-ttu-id="380b7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="380b7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="380b7-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="380b7-126">NOTES</span></span>

## <span data-ttu-id="380b7-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="380b7-127">RELATED LINKS</span></span>

[<span data-ttu-id="380b7-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="380b7-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="380b7-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="380b7-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="380b7-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="380b7-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="380b7-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="380b7-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


