---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 60b98db10aab4456ea8ca463f49ee3f7f58ffdd2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910154"
---
# <span data-ttu-id="eb322-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb322-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="eb322-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb322-102">SYNOPSIS</span></span>
<span data-ttu-id="eb322-103">Добавляет конфигурацию перенаправления в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="eb322-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="eb322-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb322-104">SYNTAX</span></span>

### <span data-ttu-id="eb322-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb322-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb322-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="eb322-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb322-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="eb322-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb322-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb322-108">DESCRIPTION</span></span>
<span data-ttu-id="eb322-109">Командлет **Add-AzApplicationGatewayRedirectConfiguration** добавляет конфигурацию перенаправления в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="eb322-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="eb322-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb322-110">EXAMPLES</span></span>

### <span data-ttu-id="eb322-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eb322-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="eb322-112">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="eb322-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="eb322-113">Вторая команда добавляет конфигурацию перенаправления к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="eb322-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="eb322-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb322-114">PARAMETERS</span></span>

### <span data-ttu-id="eb322-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb322-115">-ApplicationGateway</span></span>
<span data-ttu-id="eb322-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb322-116">The applicationGateway</span></span>

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

### <span data-ttu-id="eb322-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb322-117">-DefaultProfile</span></span>
<span data-ttu-id="eb322-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb322-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb322-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="eb322-119">-IncludePath</span></span>
<span data-ttu-id="eb322-120">Включите путь в перенаправленный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="eb322-120">Include path in the redirected url.</span></span>
<span data-ttu-id="eb322-121">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="eb322-121">Default is true.</span></span>

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

### <span data-ttu-id="eb322-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="eb322-122">-IncludeQueryString</span></span>
<span data-ttu-id="eb322-123">Включите строку запроса в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="eb322-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="eb322-124">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="eb322-124">Default is true.</span></span>

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

### <span data-ttu-id="eb322-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eb322-125">-Name</span></span>
<span data-ttu-id="eb322-126">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="eb322-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="eb322-127">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="eb322-127">-RedirectType</span></span>
<span data-ttu-id="eb322-128">Тип перенаправления</span><span class="sxs-lookup"><span data-stu-id="eb322-128">The type of redirect</span></span>

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

### <span data-ttu-id="eb322-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="eb322-129">-TargetListener</span></span>
<span data-ttu-id="eb322-130">HTTPListener перенаправить запрос на</span><span class="sxs-lookup"><span data-stu-id="eb322-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="eb322-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="eb322-131">-TargetListenerID</span></span>
<span data-ttu-id="eb322-132">Идентификатор прослушивателя, на который нужно перенаправить запрос</span><span class="sxs-lookup"><span data-stu-id="eb322-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="eb322-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="eb322-133">-TargetUrl</span></span>
<span data-ttu-id="eb322-134">Конечный URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="eb322-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="eb322-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb322-135">CommonParameters</span></span>
<span data-ttu-id="eb322-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb322-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb322-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb322-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb322-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb322-138">INPUTS</span></span>

### <span data-ttu-id="eb322-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb322-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eb322-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb322-140">OUTPUTS</span></span>

### <span data-ttu-id="eb322-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb322-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eb322-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb322-142">NOTES</span></span>

## <span data-ttu-id="eb322-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb322-143">RELATED LINKS</span></span>

