---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e768c8f5e557954dd6e932726f38b9844699de9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730394"
---
# <span data-ttu-id="2be19-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2be19-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="2be19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2be19-102">SYNOPSIS</span></span>
<span data-ttu-id="2be19-103">Создание конфигурации перенаправления для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2be19-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="2be19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2be19-104">SYNTAX</span></span>

### <span data-ttu-id="2be19-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2be19-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2be19-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2be19-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2be19-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="2be19-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2be19-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2be19-108">DESCRIPTION</span></span>
<span data-ttu-id="2be19-109">Командлет **New-AzApplicationGatewayRedirectConfiguration** создает конфигурацию перенаправления для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2be19-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="2be19-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2be19-110">EXAMPLES</span></span>

### <span data-ttu-id="2be19-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2be19-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="2be19-112">Эта команда создает конфигурацию перенаправления с именем Redirect01 и сохраняет результат в переменной с именем $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="2be19-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="2be19-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2be19-113">PARAMETERS</span></span>

### <span data-ttu-id="2be19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be19-114">-DefaultProfile</span></span>
<span data-ttu-id="2be19-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2be19-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2be19-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="2be19-116">-IncludePath</span></span>
<span data-ttu-id="2be19-117">Включите путь в перенаправленный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="2be19-117">Include path in the redirected url.</span></span>
<span data-ttu-id="2be19-118">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="2be19-118">Default is true.</span></span>

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

### <span data-ttu-id="2be19-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="2be19-119">-IncludeQueryString</span></span>
<span data-ttu-id="2be19-120">Включите строку запроса в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="2be19-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="2be19-121">Значение по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="2be19-121">Default is true.</span></span>

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

### <span data-ttu-id="2be19-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2be19-122">-Name</span></span>
<span data-ttu-id="2be19-123">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="2be19-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="2be19-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="2be19-124">-RedirectType</span></span>
<span data-ttu-id="2be19-125">Тип перенаправления</span><span class="sxs-lookup"><span data-stu-id="2be19-125">The type of redirect</span></span>

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

### <span data-ttu-id="2be19-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="2be19-126">-TargetListener</span></span>
<span data-ttu-id="2be19-127">Прослушиватель HTTP для перенаправления запроса на</span><span class="sxs-lookup"><span data-stu-id="2be19-127">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="2be19-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="2be19-128">-TargetListenerID</span></span>
<span data-ttu-id="2be19-129">Идентификатор прослушивателя HTTP, на который нужно перенаправить запрос</span><span class="sxs-lookup"><span data-stu-id="2be19-129">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="2be19-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="2be19-130">-TargetUrl</span></span>
<span data-ttu-id="2be19-131">Конечный URL-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="2be19-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="2be19-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be19-132">CommonParameters</span></span>
<span data-ttu-id="2be19-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2be19-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be19-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2be19-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be19-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2be19-135">INPUTS</span></span>

### <span data-ttu-id="2be19-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="2be19-136">None</span></span>

## <span data-ttu-id="2be19-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2be19-137">OUTPUTS</span></span>

### <span data-ttu-id="2be19-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2be19-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="2be19-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="2be19-139">NOTES</span></span>

## <span data-ttu-id="2be19-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2be19-140">RELATED LINKS</span></span>

[<span data-ttu-id="2be19-141">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2be19-141">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="2be19-142">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2be19-142">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="2be19-143">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2be19-143">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="2be19-144">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2be19-144">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
