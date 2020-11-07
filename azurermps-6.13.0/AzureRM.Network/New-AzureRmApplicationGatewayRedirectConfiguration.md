---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 06f8b64e1f79a4c024c56d834e09d374ce201cfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733158"
---
# <span data-ttu-id="146bd-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="146bd-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="146bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="146bd-102">SYNOPSIS</span></span>
<span data-ttu-id="146bd-103">Создание конфигурации перенаправления для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="146bd-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="146bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="146bd-104">SYNTAX</span></span>

### <span data-ttu-id="146bd-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="146bd-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="146bd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="146bd-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="146bd-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="146bd-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="146bd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="146bd-108">DESCRIPTION</span></span>
<span data-ttu-id="146bd-109">Командлет **New-AzureRmApplicationGatewayRedirectConfiguration** создает конфигурацию перенаправления для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="146bd-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="146bd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="146bd-110">EXAMPLES</span></span>

### <span data-ttu-id="146bd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="146bd-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="146bd-112">Эта команда создает конфигурацию перенаправления с именем Redirect01 и сохраняет результат в переменной с именем $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="146bd-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="146bd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="146bd-113">PARAMETERS</span></span>

### <span data-ttu-id="146bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="146bd-114">-DefaultProfile</span></span>
<span data-ttu-id="146bd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="146bd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="146bd-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="146bd-116">-IncludePath</span></span>
<span data-ttu-id="146bd-117">Включите путь в перенаправленный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="146bd-117">Include path in the redirected url.</span></span>
<span data-ttu-id="146bd-118">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="146bd-118">Default is true.</span></span>

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

### <span data-ttu-id="146bd-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="146bd-119">-IncludeQueryString</span></span>
<span data-ttu-id="146bd-120">Включите строку запроса в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="146bd-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="146bd-121">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="146bd-121">Default is true.</span></span>

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

### <span data-ttu-id="146bd-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="146bd-122">-Name</span></span>
<span data-ttu-id="146bd-123">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="146bd-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="146bd-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="146bd-124">-RedirectType</span></span>
<span data-ttu-id="146bd-125">Тип перенаправления</span><span class="sxs-lookup"><span data-stu-id="146bd-125">The type of redirect</span></span>

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

### <span data-ttu-id="146bd-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="146bd-126">-TargetListener</span></span>
<span data-ttu-id="146bd-127">HTTPListener перенаправить запрос на</span><span class="sxs-lookup"><span data-stu-id="146bd-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="146bd-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="146bd-128">-TargetListenerID</span></span>
<span data-ttu-id="146bd-129">Идентификатор прослушивателя, на который нужно перенаправить запрос</span><span class="sxs-lookup"><span data-stu-id="146bd-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="146bd-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="146bd-130">-TargetUrl</span></span>
<span data-ttu-id="146bd-131">Конечный URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="146bd-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="146bd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="146bd-132">CommonParameters</span></span>
<span data-ttu-id="146bd-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="146bd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="146bd-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="146bd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="146bd-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="146bd-135">INPUTS</span></span>

### <span data-ttu-id="146bd-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="146bd-136">None</span></span>

## <span data-ttu-id="146bd-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="146bd-137">OUTPUTS</span></span>

### <span data-ttu-id="146bd-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="146bd-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="146bd-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="146bd-139">NOTES</span></span>

## <span data-ttu-id="146bd-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="146bd-140">RELATED LINKS</span></span>
