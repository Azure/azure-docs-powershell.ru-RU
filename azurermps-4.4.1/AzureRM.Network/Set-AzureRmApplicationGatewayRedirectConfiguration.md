---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 23b27fc0b8b2a8d55a2af91d808b846e4de324a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732700"
---
# <span data-ttu-id="14869-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="14869-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="14869-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14869-102">SYNOPSIS</span></span>
<span data-ttu-id="14869-103">Задает конфигурацию перенаправления на существующем шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="14869-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14869-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14869-104">SYNTAX</span></span>

### <span data-ttu-id="14869-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="14869-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14869-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="14869-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14869-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="14869-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14869-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14869-108">DESCRIPTION</span></span>
<span data-ttu-id="14869-109">Командлет **Set-AzureRmApplicationGatewayRequestRoutingRule** изменяет конфигурацию перенаправления.</span><span class="sxs-lookup"><span data-stu-id="14869-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="14869-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14869-110">EXAMPLES</span></span>

### <span data-ttu-id="14869-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14869-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="14869-112">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="14869-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="14869-113">Вторая команда изменяет конфигурацию перенаправления для шлюза приложения, чтобы переадресовать тип как фиксированный и использовать конечный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="14869-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="14869-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14869-114">PARAMETERS</span></span>

### <span data-ttu-id="14869-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14869-115">-ApplicationGateway</span></span>
<span data-ttu-id="14869-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14869-116">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14869-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="14869-117">-IncludePath</span></span>
<span data-ttu-id="14869-118">Включите путь в перенаправленный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="14869-118">Include path in the redirected url.</span></span>
<span data-ttu-id="14869-119">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="14869-119">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14869-120">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="14869-120">-IncludeQueryString</span></span>
<span data-ttu-id="14869-121">Включите строку запроса в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="14869-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="14869-122">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="14869-122">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14869-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="14869-123">-Name</span></span>
<span data-ttu-id="14869-124">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="14869-124">The name of the Redirect Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14869-125">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="14869-125">-RedirectType</span></span>
<span data-ttu-id="14869-126">Тип перенаправления</span><span class="sxs-lookup"><span data-stu-id="14869-126">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14869-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="14869-127">-TargetListener</span></span>
<span data-ttu-id="14869-128">HTTPListener перенаправить запрос на</span><span class="sxs-lookup"><span data-stu-id="14869-128">HTTPListener to redirect the request to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14869-129">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="14869-129">-TargetListenerID</span></span>
<span data-ttu-id="14869-130">Идентификатор прослушивателя, на который нужно перенаправить запрос</span><span class="sxs-lookup"><span data-stu-id="14869-130">ID of  listener to redirect the request to</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14869-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="14869-131">-TargetUrl</span></span>
<span data-ttu-id="14869-132">Конечный URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="14869-132">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14869-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14869-133">-DefaultProfile</span></span>
<span data-ttu-id="14869-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14869-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14869-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14869-135">CommonParameters</span></span>
<span data-ttu-id="14869-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14869-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14869-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14869-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14869-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14869-138">INPUTS</span></span>

### <span data-ttu-id="14869-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14869-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14869-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14869-140">OUTPUTS</span></span>

### <span data-ttu-id="14869-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="14869-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="14869-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="14869-142">NOTES</span></span>

## <span data-ttu-id="14869-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14869-143">RELATED LINKS</span></span>

