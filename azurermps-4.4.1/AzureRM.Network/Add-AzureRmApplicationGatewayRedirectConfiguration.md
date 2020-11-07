---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 449c3999a3041be819b9f5f665054969223c1557
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734051"
---
# <span data-ttu-id="1eb20-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1eb20-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="1eb20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1eb20-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb20-103">Добавляет конфигурацию перенаправления в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="1eb20-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eb20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1eb20-104">SYNTAX</span></span>

### <span data-ttu-id="1eb20-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1eb20-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eb20-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1eb20-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eb20-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="1eb20-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eb20-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eb20-108">DESCRIPTION</span></span>
<span data-ttu-id="1eb20-109">Командлет **Add-AzureRmApplicationGatewayRedirectConfiguration** добавляет конфигурацию перенаправления в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="1eb20-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="1eb20-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1eb20-110">EXAMPLES</span></span>

### <span data-ttu-id="1eb20-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1eb20-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="1eb20-112">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1eb20-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1eb20-113">Вторая команда добавляет конфигурацию перенаправления к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="1eb20-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="1eb20-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1eb20-114">PARAMETERS</span></span>

### <span data-ttu-id="1eb20-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1eb20-115">-ApplicationGateway</span></span>
<span data-ttu-id="1eb20-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1eb20-116">The applicationGateway</span></span>

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

### <span data-ttu-id="1eb20-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="1eb20-117">-IncludePath</span></span>
<span data-ttu-id="1eb20-118">Включите путь в перенаправленный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="1eb20-118">Include path in the redirected url.</span></span>
<span data-ttu-id="1eb20-119">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="1eb20-119">Default is true.</span></span>

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

### <span data-ttu-id="1eb20-120">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="1eb20-120">-IncludeQueryString</span></span>
<span data-ttu-id="1eb20-121">Включите строку запроса в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="1eb20-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="1eb20-122">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="1eb20-122">Default is true.</span></span>

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

### <span data-ttu-id="1eb20-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1eb20-123">-Name</span></span>
<span data-ttu-id="1eb20-124">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="1eb20-124">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="1eb20-125">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="1eb20-125">-RedirectType</span></span>
<span data-ttu-id="1eb20-126">Тип перенаправления</span><span class="sxs-lookup"><span data-stu-id="1eb20-126">The type of redirect</span></span>

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

### <span data-ttu-id="1eb20-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="1eb20-127">-TargetListener</span></span>
<span data-ttu-id="1eb20-128">HTTPListener перенаправить запрос на</span><span class="sxs-lookup"><span data-stu-id="1eb20-128">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="1eb20-129">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="1eb20-129">-TargetListenerID</span></span>
<span data-ttu-id="1eb20-130">Идентификатор прослушивателя, на который нужно перенаправить запрос</span><span class="sxs-lookup"><span data-stu-id="1eb20-130">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="1eb20-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="1eb20-131">-TargetUrl</span></span>
<span data-ttu-id="1eb20-132">Конечный URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="1eb20-132">Target URL fo redirection</span></span>

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

### <span data-ttu-id="1eb20-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb20-133">-DefaultProfile</span></span>
<span data-ttu-id="1eb20-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb20-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1eb20-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb20-135">CommonParameters</span></span>
<span data-ttu-id="1eb20-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1eb20-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb20-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eb20-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb20-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1eb20-138">INPUTS</span></span>

### <span data-ttu-id="1eb20-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1eb20-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1eb20-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1eb20-140">OUTPUTS</span></span>

### <span data-ttu-id="1eb20-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1eb20-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1eb20-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="1eb20-142">NOTES</span></span>

## <span data-ttu-id="1eb20-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1eb20-143">RELATED LINKS</span></span>

