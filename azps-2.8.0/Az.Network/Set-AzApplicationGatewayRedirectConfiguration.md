---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 746d1bb37bd49acfdc0a353c9985508f50514073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901830"
---
# <span data-ttu-id="4f566-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f566-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="4f566-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f566-102">SYNOPSIS</span></span>
<span data-ttu-id="4f566-103">Задает конфигурацию перенаправления на существующем шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="4f566-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="4f566-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f566-104">SYNTAX</span></span>

### <span data-ttu-id="4f566-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f566-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f566-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4f566-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f566-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="4f566-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f566-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f566-108">DESCRIPTION</span></span>
<span data-ttu-id="4f566-109">Командлет **Set-AzApplicationGatewayRequestRoutingRule** изменяет конфигурацию перенаправления.</span><span class="sxs-lookup"><span data-stu-id="4f566-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="4f566-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f566-110">EXAMPLES</span></span>

### <span data-ttu-id="4f566-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4f566-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="4f566-112">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4f566-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4f566-113">Вторая команда изменяет конфигурацию перенаправления для шлюза приложения, чтобы переадресовать тип как фиксированный и использовать конечный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="4f566-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="4f566-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f566-114">PARAMETERS</span></span>

### <span data-ttu-id="4f566-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4f566-115">-ApplicationGateway</span></span>
<span data-ttu-id="4f566-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4f566-116">The applicationGateway</span></span>

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

### <span data-ttu-id="4f566-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f566-117">-DefaultProfile</span></span>
<span data-ttu-id="4f566-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f566-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f566-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="4f566-119">-IncludePath</span></span>
<span data-ttu-id="4f566-120">Включите путь в перенаправленный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="4f566-120">Include path in the redirected url.</span></span>
<span data-ttu-id="4f566-121">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="4f566-121">Default is true.</span></span>

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

### <span data-ttu-id="4f566-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="4f566-122">-IncludeQueryString</span></span>
<span data-ttu-id="4f566-123">Включите строку запроса в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="4f566-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="4f566-124">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="4f566-124">Default is true.</span></span>

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

### <span data-ttu-id="4f566-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4f566-125">-Name</span></span>
<span data-ttu-id="4f566-126">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="4f566-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="4f566-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="4f566-127">-RedirectType</span></span>
<span data-ttu-id="4f566-128">Тип перенаправления</span><span class="sxs-lookup"><span data-stu-id="4f566-128">The type of redirect</span></span>

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

### <span data-ttu-id="4f566-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="4f566-129">-TargetListener</span></span>
<span data-ttu-id="4f566-130">Прослушиватель HTTP для перенаправления запроса на</span><span class="sxs-lookup"><span data-stu-id="4f566-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="4f566-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="4f566-131">-TargetListenerID</span></span>
<span data-ttu-id="4f566-132">Идентификатор прослушивателя HTTP, на который нужно перенаправить запрос</span><span class="sxs-lookup"><span data-stu-id="4f566-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="4f566-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="4f566-133">-TargetUrl</span></span>
<span data-ttu-id="4f566-134">Конечный URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="4f566-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="4f566-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f566-135">CommonParameters</span></span>
<span data-ttu-id="4f566-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f566-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f566-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f566-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f566-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f566-138">INPUTS</span></span>

### <span data-ttu-id="4f566-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4f566-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4f566-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f566-140">OUTPUTS</span></span>

### <span data-ttu-id="4f566-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4f566-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4f566-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f566-142">NOTES</span></span>

## <span data-ttu-id="4f566-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f566-143">RELATED LINKS</span></span>

[<span data-ttu-id="4f566-144">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f566-144">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="4f566-145">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f566-145">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="4f566-146">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f566-146">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="4f566-147">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f566-147">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)
