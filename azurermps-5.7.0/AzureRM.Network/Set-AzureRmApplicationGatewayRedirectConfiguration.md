---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 9a37bd3769fa7078e0d215b2d6c2452c4fc64bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735101"
---
# <span data-ttu-id="522be-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="522be-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="522be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="522be-102">SYNOPSIS</span></span>
<span data-ttu-id="522be-103">Задает конфигурацию перенаправления на существующем шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="522be-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="522be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="522be-104">SYNTAX</span></span>

### <span data-ttu-id="522be-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="522be-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="522be-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="522be-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="522be-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="522be-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="522be-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="522be-108">DESCRIPTION</span></span>
<span data-ttu-id="522be-109">Командлет **Set-AzureRmApplicationGatewayRequestRoutingRule** изменяет конфигурацию перенаправления.</span><span class="sxs-lookup"><span data-stu-id="522be-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="522be-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="522be-110">EXAMPLES</span></span>

### <span data-ttu-id="522be-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="522be-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="522be-112">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="522be-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="522be-113">Вторая команда изменяет конфигурацию перенаправления для шлюза приложения, чтобы переадресовать тип как фиксированный и использовать конечный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="522be-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="522be-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="522be-114">PARAMETERS</span></span>

### <span data-ttu-id="522be-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="522be-115">-ApplicationGateway</span></span>
<span data-ttu-id="522be-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="522be-116">The applicationGateway</span></span>

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

### <span data-ttu-id="522be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="522be-117">-DefaultProfile</span></span>
<span data-ttu-id="522be-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="522be-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522be-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="522be-119">-IncludePath</span></span>
<span data-ttu-id="522be-120">Включите путь в перенаправленный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="522be-120">Include path in the redirected url.</span></span>
<span data-ttu-id="522be-121">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="522be-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522be-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="522be-122">-IncludeQueryString</span></span>
<span data-ttu-id="522be-123">Включите строку запроса в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="522be-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="522be-124">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="522be-124">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522be-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="522be-125">-Name</span></span>
<span data-ttu-id="522be-126">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="522be-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="522be-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="522be-127">-RedirectType</span></span>
<span data-ttu-id="522be-128">Тип перенаправления</span><span class="sxs-lookup"><span data-stu-id="522be-128">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522be-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="522be-129">-TargetListener</span></span>
<span data-ttu-id="522be-130">HTTPListener перенаправить запрос на</span><span class="sxs-lookup"><span data-stu-id="522be-130">HTTPListener to redirect the request to</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522be-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="522be-131">-TargetListenerID</span></span>
<span data-ttu-id="522be-132">Идентификатор прослушивателя, на который нужно перенаправить запрос</span><span class="sxs-lookup"><span data-stu-id="522be-132">ID of  listener to redirect the request to</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522be-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="522be-133">-TargetUrl</span></span>
<span data-ttu-id="522be-134">Конечный URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="522be-134">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="522be-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522be-135">CommonParameters</span></span>
<span data-ttu-id="522be-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="522be-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522be-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="522be-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522be-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="522be-138">INPUTS</span></span>

### <span data-ttu-id="522be-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="522be-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="522be-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="522be-140">OUTPUTS</span></span>

### <span data-ttu-id="522be-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="522be-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="522be-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="522be-142">NOTES</span></span>

## <span data-ttu-id="522be-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="522be-143">RELATED LINKS</span></span>

