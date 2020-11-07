---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 5cf1e01be8d0a76ba8dc319c5241f40613ad4304
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909746"
---
# <span data-ttu-id="b9ea1-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9ea1-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="b9ea1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ea1-103">Создание конфигурации перенаправления для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b9ea1-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="b9ea1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9ea1-104">SYNTAX</span></span>

### <span data-ttu-id="b9ea1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b9ea1-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9ea1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b9ea1-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9ea1-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="b9ea1-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9ea1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9ea1-108">DESCRIPTION</span></span>
<span data-ttu-id="b9ea1-109">Командлет **New-AzApplicationGatewayRedirectConfiguration** создает конфигурацию перенаправления для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b9ea1-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="b9ea1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9ea1-110">EXAMPLES</span></span>

### <span data-ttu-id="b9ea1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9ea1-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="b9ea1-112">Эта команда создает конфигурацию перенаправления с именем Redirect01 и сохраняет результат в переменной с именем $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="b9ea1-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="b9ea1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9ea1-113">PARAMETERS</span></span>

### <span data-ttu-id="b9ea1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ea1-114">-DefaultProfile</span></span>
<span data-ttu-id="b9ea1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ea1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9ea1-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="b9ea1-116">-IncludePath</span></span>
<span data-ttu-id="b9ea1-117">Включите путь в перенаправленный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="b9ea1-117">Include path in the redirected url.</span></span>
<span data-ttu-id="b9ea1-118">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="b9ea1-118">Default is true.</span></span>

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

### <span data-ttu-id="b9ea1-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="b9ea1-119">-IncludeQueryString</span></span>
<span data-ttu-id="b9ea1-120">Включите строку запроса в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="b9ea1-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="b9ea1-121">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="b9ea1-121">Default is true.</span></span>

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

### <span data-ttu-id="b9ea1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b9ea1-122">-Name</span></span>
<span data-ttu-id="b9ea1-123">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="b9ea1-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="b9ea1-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="b9ea1-124">-RedirectType</span></span>
<span data-ttu-id="b9ea1-125">Тип перенаправления</span><span class="sxs-lookup"><span data-stu-id="b9ea1-125">The type of redirect</span></span>

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

### <span data-ttu-id="b9ea1-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="b9ea1-126">-TargetListener</span></span>
<span data-ttu-id="b9ea1-127">HTTPListener перенаправить запрос на</span><span class="sxs-lookup"><span data-stu-id="b9ea1-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="b9ea1-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="b9ea1-128">-TargetListenerID</span></span>
<span data-ttu-id="b9ea1-129">Идентификатор прослушивателя, на который нужно перенаправить запрос</span><span class="sxs-lookup"><span data-stu-id="b9ea1-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="b9ea1-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="b9ea1-130">-TargetUrl</span></span>
<span data-ttu-id="b9ea1-131">Конечный URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="b9ea1-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="b9ea1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ea1-132">CommonParameters</span></span>
<span data-ttu-id="b9ea1-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9ea1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ea1-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9ea1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ea1-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9ea1-135">INPUTS</span></span>

### <span data-ttu-id="b9ea1-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="b9ea1-136">None</span></span>

## <span data-ttu-id="b9ea1-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9ea1-137">OUTPUTS</span></span>

### <span data-ttu-id="b9ea1-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9ea1-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="b9ea1-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9ea1-139">NOTES</span></span>

## <span data-ttu-id="b9ea1-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9ea1-140">RELATED LINKS</span></span>

