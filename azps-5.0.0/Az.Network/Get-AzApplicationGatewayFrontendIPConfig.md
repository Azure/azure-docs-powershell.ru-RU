---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 1efce67698ca6d2e3a8bc9eeab3d89e00e1833f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250005"
---
# <span data-ttu-id="89dbc-101">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89dbc-101">Get-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="89dbc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="89dbc-103">Получает интерфейсную конфигурацию IP-конфигурации для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="89dbc-103">Gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="89dbc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89dbc-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89dbc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89dbc-105">DESCRIPTION</span></span>
<span data-ttu-id="89dbc-106">Командлет **Get-AzApplicationGatewayFrontendIPConfig** получает интерфейсную конфигурацию IP-конфигурации для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="89dbc-106">The **Get-AzApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="89dbc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89dbc-107">EXAMPLES</span></span>

### <span data-ttu-id="89dbc-108">Пример 1: получение указанной переднего плана IP-конфигурации</span><span class="sxs-lookup"><span data-stu-id="89dbc-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="89dbc-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw. Вторая команда получает клиентскую IP-конфигурацию с именем FrontEndIP01 from $AppGw и сохраняет ее в переменной $FrontEndIP.</span><span class="sxs-lookup"><span data-stu-id="89dbc-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="89dbc-110">Пример 2: получение списка конфигураций IP-адресов интерфейсов</span><span class="sxs-lookup"><span data-stu-id="89dbc-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="89dbc-111">Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw. Вторая команда получает список IP-конфигураций переднего плана из $AppGw и сохраняет их в переменной $FrontEndIPs.</span><span class="sxs-lookup"><span data-stu-id="89dbc-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="89dbc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89dbc-112">PARAMETERS</span></span>

### <span data-ttu-id="89dbc-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89dbc-113">-ApplicationGateway</span></span>
<span data-ttu-id="89dbc-114">Указывает объект шлюза приложения, который содержит интерфейсную конфигурацию IP.</span><span class="sxs-lookup"><span data-stu-id="89dbc-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="89dbc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89dbc-115">-DefaultProfile</span></span>
<span data-ttu-id="89dbc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89dbc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89dbc-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89dbc-117">-Name</span></span>
<span data-ttu-id="89dbc-118">Задает имя интерфейса IP-конфигурации, который получает интерфейсный командлет.</span><span class="sxs-lookup"><span data-stu-id="89dbc-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="89dbc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89dbc-119">CommonParameters</span></span>
<span data-ttu-id="89dbc-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89dbc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89dbc-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89dbc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89dbc-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89dbc-122">INPUTS</span></span>

### <span data-ttu-id="89dbc-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89dbc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="89dbc-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89dbc-124">OUTPUTS</span></span>

### <span data-ttu-id="89dbc-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89dbc-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="89dbc-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="89dbc-126">NOTES</span></span>

## <span data-ttu-id="89dbc-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89dbc-127">RELATED LINKS</span></span>

[<span data-ttu-id="89dbc-128">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89dbc-128">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="89dbc-129">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89dbc-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="89dbc-130">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89dbc-130">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="89dbc-131">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="89dbc-131">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)

