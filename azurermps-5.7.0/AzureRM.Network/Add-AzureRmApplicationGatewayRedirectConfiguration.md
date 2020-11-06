---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 73d60d86110893005e72152c08e82d4152b1c482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559035"
---
# <span data-ttu-id="e5e36-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5e36-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e5e36-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5e36-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e36-103">Добавляет конфигурацию перенаправления в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="e5e36-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5e36-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5e36-104">SYNTAX</span></span>

### <span data-ttu-id="e5e36-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5e36-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5e36-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e5e36-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5e36-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="e5e36-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5e36-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5e36-108">DESCRIPTION</span></span>
<span data-ttu-id="e5e36-109">Командлет **Add-AzureRmApplicationGatewayRedirectConfiguration** добавляет конфигурацию перенаправления в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="e5e36-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="e5e36-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5e36-110">EXAMPLES</span></span>

### <span data-ttu-id="e5e36-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5e36-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="e5e36-112">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e5e36-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e5e36-113">Вторая команда добавляет конфигурацию перенаправления к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="e5e36-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="e5e36-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5e36-114">PARAMETERS</span></span>

### <span data-ttu-id="e5e36-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5e36-115">-ApplicationGateway</span></span>
<span data-ttu-id="e5e36-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5e36-116">The applicationGateway</span></span>

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

### <span data-ttu-id="e5e36-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e36-117">-DefaultProfile</span></span>
<span data-ttu-id="e5e36-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e36-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5e36-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="e5e36-119">-IncludePath</span></span>
<span data-ttu-id="e5e36-120">Включите путь в перенаправленный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="e5e36-120">Include path in the redirected url.</span></span>
<span data-ttu-id="e5e36-121">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="e5e36-121">Default is true.</span></span>

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

### <span data-ttu-id="e5e36-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="e5e36-122">-IncludeQueryString</span></span>
<span data-ttu-id="e5e36-123">Включите строку запроса в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="e5e36-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="e5e36-124">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="e5e36-124">Default is true.</span></span>

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

### <span data-ttu-id="e5e36-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5e36-125">-Name</span></span>
<span data-ttu-id="e5e36-126">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="e5e36-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="e5e36-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="e5e36-127">-RedirectType</span></span>
<span data-ttu-id="e5e36-128">Тип перенаправления</span><span class="sxs-lookup"><span data-stu-id="e5e36-128">The type of redirect</span></span>

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

### <span data-ttu-id="e5e36-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="e5e36-129">-TargetListener</span></span>
<span data-ttu-id="e5e36-130">HTTPListener перенаправить запрос на</span><span class="sxs-lookup"><span data-stu-id="e5e36-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="e5e36-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="e5e36-131">-TargetListenerID</span></span>
<span data-ttu-id="e5e36-132">Идентификатор прослушивателя, на который нужно перенаправить запрос</span><span class="sxs-lookup"><span data-stu-id="e5e36-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="e5e36-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="e5e36-133">-TargetUrl</span></span>
<span data-ttu-id="e5e36-134">Конечный URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="e5e36-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="e5e36-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e36-135">CommonParameters</span></span>
<span data-ttu-id="e5e36-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5e36-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e36-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e36-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e36-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5e36-138">INPUTS</span></span>

### <span data-ttu-id="e5e36-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5e36-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e5e36-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5e36-140">OUTPUTS</span></span>

### <span data-ttu-id="e5e36-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5e36-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e5e36-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5e36-142">NOTES</span></span>

## <span data-ttu-id="e5e36-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5e36-143">RELATED LINKS</span></span>

