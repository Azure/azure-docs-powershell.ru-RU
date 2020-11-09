---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cf65e93f1dc2026c0fc973d694fe1f44718df12e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318002"
---
# <span data-ttu-id="280cd-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="280cd-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="280cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="280cd-102">SYNOPSIS</span></span>
<span data-ttu-id="280cd-103">Создает массив сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="280cd-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="280cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="280cd-104">SYNTAX</span></span>

### <span data-ttu-id="280cd-105">BackendSetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="280cd-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="280cd-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="280cd-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="280cd-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="280cd-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="280cd-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="280cd-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="280cd-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="280cd-109">DESCRIPTION</span></span>
<span data-ttu-id="280cd-110">Командлет **New-AzApplicationGatewayUrlPathMapConfig** создает массив сопоставлений URL-путей с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="280cd-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="280cd-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="280cd-111">EXAMPLES</span></span>

### <span data-ttu-id="280cd-112">Пример 1: создание массива сопоставлений URL-путей с серверным пулом серверов</span><span class="sxs-lookup"><span data-stu-id="280cd-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="280cd-113">Эта команда создает массив сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="280cd-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="280cd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="280cd-114">PARAMETERS</span></span>

### <span data-ttu-id="280cd-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="280cd-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="280cd-116">Указывает используемый по умолчанию пул серверных адресов для маршрутизации на случай, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="280cd-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280cd-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="280cd-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="280cd-118">Указывает идентификатор пула адресных адресов сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="280cd-118">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280cd-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="280cd-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="280cd-120">Задает параметры HTTP по умолчанию для использования в случае, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="280cd-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280cd-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="280cd-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="280cd-122">Указывает идентификатор HTTP-параметров по умолчанию для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="280cd-122">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280cd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="280cd-123">-DefaultProfile</span></span>
<span data-ttu-id="280cd-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="280cd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="280cd-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="280cd-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="280cd-126">RedirectConfiguration для шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="280cd-126">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280cd-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="280cd-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="280cd-128">Идентификатор RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="280cd-128">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280cd-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="280cd-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="280cd-130">Наборы правил перезаписи по умолчанию для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="280cd-130">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280cd-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="280cd-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="280cd-132">Идентификатор набора правил перезаписи по умолчанию для шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="280cd-132">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280cd-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="280cd-133">-Name</span></span>
<span data-ttu-id="280cd-134">Указывает имя карты URL-пути, которое создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="280cd-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="280cd-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="280cd-135">-PathRules</span></span>
<span data-ttu-id="280cd-136">Задает список правил пути.</span><span class="sxs-lookup"><span data-stu-id="280cd-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="280cd-137">Обратите внимание, что правила путей зависят от порядка, они применяются в порядке их указания.</span><span class="sxs-lookup"><span data-stu-id="280cd-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="280cd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="280cd-138">CommonParameters</span></span>
<span data-ttu-id="280cd-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="280cd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="280cd-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="280cd-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="280cd-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="280cd-141">INPUTS</span></span>

### <span data-ttu-id="280cd-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="280cd-142">None</span></span>

## <span data-ttu-id="280cd-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="280cd-143">OUTPUTS</span></span>

### <span data-ttu-id="280cd-144">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="280cd-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="280cd-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="280cd-145">NOTES</span></span>

## <span data-ttu-id="280cd-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="280cd-146">RELATED LINKS</span></span>

[<span data-ttu-id="280cd-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="280cd-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="280cd-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="280cd-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="280cd-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="280cd-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="280cd-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="280cd-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


