---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 2cb7455d5a902882fdd98dd5fea47ae5a28e1dc9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913294"
---
# <span data-ttu-id="5420d-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5420d-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="5420d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5420d-102">SYNOPSIS</span></span>
<span data-ttu-id="5420d-103">Создание конфигурации перенаправления для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="5420d-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5420d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5420d-104">SYNTAX</span></span>

### <span data-ttu-id="5420d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5420d-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5420d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5420d-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5420d-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="5420d-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5420d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5420d-108">DESCRIPTION</span></span>
<span data-ttu-id="5420d-109">Командлет **New-AzureRmApplicationGatewayRedirectConfiguration** создает конфигурацию перенаправления для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="5420d-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="5420d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5420d-110">EXAMPLES</span></span>

### <span data-ttu-id="5420d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5420d-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="5420d-112">Эта команда создает конфигурацию перенаправления с именем Redirect01 и сохраняет результат в переменной с именем $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="5420d-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="5420d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5420d-113">PARAMETERS</span></span>

### <span data-ttu-id="5420d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5420d-114">-DefaultProfile</span></span>
<span data-ttu-id="5420d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5420d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5420d-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="5420d-116">-IncludePath</span></span>
<span data-ttu-id="5420d-117">Включите путь в перенаправленный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5420d-117">Include path in the redirected url.</span></span>
<span data-ttu-id="5420d-118">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="5420d-118">Default is true.</span></span>

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

### <span data-ttu-id="5420d-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="5420d-119">-IncludeQueryString</span></span>
<span data-ttu-id="5420d-120">Включите строку запроса в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="5420d-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="5420d-121">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="5420d-121">Default is true.</span></span>

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

### <span data-ttu-id="5420d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5420d-122">-Name</span></span>
<span data-ttu-id="5420d-123">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="5420d-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="5420d-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="5420d-124">-RedirectType</span></span>
<span data-ttu-id="5420d-125">Тип перенаправления</span><span class="sxs-lookup"><span data-stu-id="5420d-125">The type of redirect</span></span>

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

### <span data-ttu-id="5420d-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="5420d-126">-TargetListener</span></span>
<span data-ttu-id="5420d-127">HTTPListener перенаправить запрос на</span><span class="sxs-lookup"><span data-stu-id="5420d-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="5420d-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="5420d-128">-TargetListenerID</span></span>
<span data-ttu-id="5420d-129">Идентификатор прослушивателя, на который нужно перенаправить запрос</span><span class="sxs-lookup"><span data-stu-id="5420d-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="5420d-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="5420d-130">-TargetUrl</span></span>
<span data-ttu-id="5420d-131">Конечный URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="5420d-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="5420d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5420d-132">CommonParameters</span></span>
<span data-ttu-id="5420d-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5420d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5420d-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5420d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5420d-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5420d-135">INPUTS</span></span>

### <span data-ttu-id="5420d-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="5420d-136">None</span></span>

## <span data-ttu-id="5420d-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5420d-137">OUTPUTS</span></span>

### <span data-ttu-id="5420d-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5420d-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="5420d-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="5420d-139">NOTES</span></span>

## <span data-ttu-id="5420d-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5420d-140">RELATED LINKS</span></span>

