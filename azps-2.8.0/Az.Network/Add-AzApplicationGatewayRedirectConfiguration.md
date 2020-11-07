---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 6db510e79d2c1796cf62a1fd00e55e7860164af9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903130"
---
# <span data-ttu-id="9b7b6-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b7b6-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="9b7b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="9b7b6-103">Добавляет конфигурацию перенаправления в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="9b7b6-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="9b7b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b7b6-104">SYNTAX</span></span>

### <span data-ttu-id="9b7b6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b7b6-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b7b6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9b7b6-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b7b6-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="9b7b6-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b7b6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b7b6-108">DESCRIPTION</span></span>
<span data-ttu-id="9b7b6-109">Командлет **Add-AzApplicationGatewayRedirectConfiguration** добавляет конфигурацию перенаправления в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="9b7b6-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="9b7b6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b7b6-110">EXAMPLES</span></span>

### <span data-ttu-id="9b7b6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9b7b6-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="9b7b6-112">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9b7b6-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9b7b6-113">Вторая команда добавляет конфигурацию перенаправления к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="9b7b6-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="9b7b6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b7b6-114">PARAMETERS</span></span>

### <span data-ttu-id="9b7b6-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b7b6-115">-ApplicationGateway</span></span>
<span data-ttu-id="9b7b6-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b7b6-116">The applicationGateway</span></span>

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

### <span data-ttu-id="9b7b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b7b6-117">-DefaultProfile</span></span>
<span data-ttu-id="9b7b6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b7b6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b7b6-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="9b7b6-119">-IncludePath</span></span>
<span data-ttu-id="9b7b6-120">Включите путь в перенаправленный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="9b7b6-120">Include path in the redirected url.</span></span>
<span data-ttu-id="9b7b6-121">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="9b7b6-121">Default is true.</span></span>

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

### <span data-ttu-id="9b7b6-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="9b7b6-122">-IncludeQueryString</span></span>
<span data-ttu-id="9b7b6-123">Включите строку запроса в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="9b7b6-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="9b7b6-124">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="9b7b6-124">Default is true.</span></span>

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

### <span data-ttu-id="9b7b6-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b7b6-125">-Name</span></span>
<span data-ttu-id="9b7b6-126">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="9b7b6-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="9b7b6-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="9b7b6-127">-RedirectType</span></span>
<span data-ttu-id="9b7b6-128">Тип перенаправления</span><span class="sxs-lookup"><span data-stu-id="9b7b6-128">The type of redirect</span></span>

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

### <span data-ttu-id="9b7b6-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="9b7b6-129">-TargetListener</span></span>
<span data-ttu-id="9b7b6-130">Прослушиватель HTTP для перенаправления запроса на</span><span class="sxs-lookup"><span data-stu-id="9b7b6-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="9b7b6-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="9b7b6-131">-TargetListenerID</span></span>
<span data-ttu-id="9b7b6-132">Идентификатор прослушивателя HTTP, на который нужно перенаправить запрос</span><span class="sxs-lookup"><span data-stu-id="9b7b6-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="9b7b6-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="9b7b6-133">-TargetUrl</span></span>
<span data-ttu-id="9b7b6-134">Конечный URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="9b7b6-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="9b7b6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b7b6-135">CommonParameters</span></span>
<span data-ttu-id="9b7b6-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b7b6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b7b6-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b7b6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b7b6-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b7b6-138">INPUTS</span></span>

### <span data-ttu-id="9b7b6-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b7b6-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b7b6-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b7b6-140">OUTPUTS</span></span>

### <span data-ttu-id="9b7b6-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b7b6-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b7b6-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b7b6-142">NOTES</span></span>

## <span data-ttu-id="9b7b6-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b7b6-143">RELATED LINKS</span></span>

[<span data-ttu-id="9b7b6-144">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b7b6-144">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="9b7b6-145">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b7b6-145">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="9b7b6-146">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b7b6-146">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="9b7b6-147">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b7b6-147">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
