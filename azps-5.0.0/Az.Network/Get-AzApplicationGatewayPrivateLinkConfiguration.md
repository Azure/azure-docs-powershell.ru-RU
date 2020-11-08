---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249995"
---
# <span data-ttu-id="a84b9-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a84b9-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="a84b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a84b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a84b9-103">Возвращает конфигурацию частной ссылки для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a84b9-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="a84b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a84b9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a84b9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a84b9-105">DESCRIPTION</span></span>
<span data-ttu-id="a84b9-106">Командлет **Get-AzApplicationGatewayPrivateLinkConfiguration** получает конфигурацию частной ссылки для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a84b9-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="a84b9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a84b9-107">EXAMPLES</span></span>

### <span data-ttu-id="a84b9-108">Пример 1: получение указанной конфигурации частной ссылки</span><span class="sxs-lookup"><span data-stu-id="a84b9-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="a84b9-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a84b9-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a84b9-110">Вторая команда получает конфигурацию частной ссылки с именем privateLinkConfig01 from $AppGw и сохраняет ее в переменной $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a84b9-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="a84b9-111">Пример 2: получение списка конфигураций личных ссылок</span><span class="sxs-lookup"><span data-stu-id="a84b9-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="a84b9-112">Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a84b9-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a84b9-113">Вторая команда получает все конфигурации частных ссылок из $AppGw и сохраняет их в переменной $PrivateLinkConfigurations.</span><span class="sxs-lookup"><span data-stu-id="a84b9-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="a84b9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a84b9-114">PARAMETERS</span></span>

### <span data-ttu-id="a84b9-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a84b9-115">-ApplicationGateway</span></span>
<span data-ttu-id="a84b9-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a84b9-116">The applicationGateway</span></span>

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

### <span data-ttu-id="a84b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a84b9-117">-DefaultProfile</span></span>
<span data-ttu-id="a84b9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a84b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a84b9-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a84b9-119">-Name</span></span>
<span data-ttu-id="a84b9-120">Имя конфигурации privateLink шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="a84b9-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="a84b9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a84b9-121">CommonParameters</span></span>
<span data-ttu-id="a84b9-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a84b9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a84b9-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a84b9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a84b9-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a84b9-124">INPUTS</span></span>

### <span data-ttu-id="a84b9-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a84b9-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a84b9-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a84b9-126">OUTPUTS</span></span>

### <span data-ttu-id="a84b9-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a84b9-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="a84b9-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a84b9-128">NOTES</span></span>

## <span data-ttu-id="a84b9-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a84b9-129">RELATED LINKS</span></span>

[<span data-ttu-id="a84b9-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a84b9-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a84b9-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a84b9-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a84b9-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a84b9-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a84b9-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a84b9-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)