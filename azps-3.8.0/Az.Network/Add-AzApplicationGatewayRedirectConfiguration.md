---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: bf187375ba625e40c147f7862d9faf4e0706f844
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912734"
---
# <span data-ttu-id="4b27d-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b27d-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="4b27d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b27d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b27d-103">Добавляет конфигурацию перенаправления в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="4b27d-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="4b27d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b27d-104">SYNTAX</span></span>

### <span data-ttu-id="4b27d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b27d-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b27d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4b27d-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b27d-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="4b27d-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b27d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b27d-108">DESCRIPTION</span></span>
<span data-ttu-id="4b27d-109">Командлет **Add-AzApplicationGatewayRedirectConfiguration** добавляет конфигурацию перенаправления в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="4b27d-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="4b27d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b27d-110">EXAMPLES</span></span>

### <span data-ttu-id="4b27d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b27d-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="4b27d-112">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4b27d-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4b27d-113">Вторая команда добавляет конфигурацию перенаправления к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="4b27d-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="4b27d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b27d-114">PARAMETERS</span></span>

### <span data-ttu-id="4b27d-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b27d-115">-ApplicationGateway</span></span>
<span data-ttu-id="4b27d-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b27d-116">The applicationGateway</span></span>

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

### <span data-ttu-id="4b27d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b27d-117">-DefaultProfile</span></span>
<span data-ttu-id="4b27d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b27d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b27d-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="4b27d-119">-IncludePath</span></span>
<span data-ttu-id="4b27d-120">Включите путь в перенаправленный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="4b27d-120">Include path in the redirected url.</span></span>
<span data-ttu-id="4b27d-121">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="4b27d-121">Default is true.</span></span>

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

### <span data-ttu-id="4b27d-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="4b27d-122">-IncludeQueryString</span></span>
<span data-ttu-id="4b27d-123">Включите строку запроса в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="4b27d-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="4b27d-124">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="4b27d-124">Default is true.</span></span>

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

### <span data-ttu-id="4b27d-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4b27d-125">-Name</span></span>
<span data-ttu-id="4b27d-126">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="4b27d-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="4b27d-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="4b27d-127">-RedirectType</span></span>
<span data-ttu-id="4b27d-128">Тип перенаправления</span><span class="sxs-lookup"><span data-stu-id="4b27d-128">The type of redirect</span></span>

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

### <span data-ttu-id="4b27d-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="4b27d-129">-TargetListener</span></span>
<span data-ttu-id="4b27d-130">Прослушиватель HTTP для перенаправления запроса на</span><span class="sxs-lookup"><span data-stu-id="4b27d-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="4b27d-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="4b27d-131">-TargetListenerID</span></span>
<span data-ttu-id="4b27d-132">Идентификатор прослушивателя HTTP, на который нужно перенаправить запрос</span><span class="sxs-lookup"><span data-stu-id="4b27d-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="4b27d-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="4b27d-133">-TargetUrl</span></span>
<span data-ttu-id="4b27d-134">Конечный URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="4b27d-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="4b27d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b27d-135">CommonParameters</span></span>
<span data-ttu-id="4b27d-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b27d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b27d-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b27d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b27d-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b27d-138">INPUTS</span></span>

### <span data-ttu-id="4b27d-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b27d-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4b27d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b27d-140">OUTPUTS</span></span>

### <span data-ttu-id="4b27d-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b27d-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4b27d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b27d-142">NOTES</span></span>

## <span data-ttu-id="4b27d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b27d-143">RELATED LINKS</span></span>

[<span data-ttu-id="4b27d-144">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b27d-144">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="4b27d-145">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b27d-145">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="4b27d-146">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b27d-146">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="4b27d-147">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b27d-147">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
