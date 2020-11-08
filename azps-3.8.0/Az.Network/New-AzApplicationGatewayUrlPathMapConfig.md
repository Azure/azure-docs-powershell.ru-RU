---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cf65e93f1dc2026c0fc973d694fe1f44718df12e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074769"
---
# <span data-ttu-id="f4032-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f4032-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="f4032-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4032-102">SYNOPSIS</span></span>
<span data-ttu-id="f4032-103">Создает массив сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="f4032-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f4032-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4032-104">SYNTAX</span></span>

### <span data-ttu-id="f4032-105">BackendSetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4032-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4032-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4032-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4032-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="f4032-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4032-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4032-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4032-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4032-109">DESCRIPTION</span></span>
<span data-ttu-id="f4032-110">Командлет **New-AzApplicationGatewayUrlPathMapConfig** создает массив сопоставлений URL-путей с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="f4032-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f4032-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4032-111">EXAMPLES</span></span>

### <span data-ttu-id="f4032-112">Пример 1: создание массива сопоставлений URL-путей с серверным пулом серверов</span><span class="sxs-lookup"><span data-stu-id="f4032-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="f4032-113">Эта команда создает массив сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="f4032-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f4032-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4032-114">PARAMETERS</span></span>

### <span data-ttu-id="f4032-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f4032-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="f4032-116">Указывает используемый по умолчанию пул серверных адресов для маршрутизации на случай, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="f4032-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="f4032-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f4032-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="f4032-118">Указывает идентификатор пула адресных адресов сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4032-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="f4032-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f4032-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="f4032-120">Задает параметры HTTP по умолчанию для использования в случае, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="f4032-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="f4032-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="f4032-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="f4032-122">Указывает идентификатор HTTP-параметров по умолчанию для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="f4032-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="f4032-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4032-123">-DefaultProfile</span></span>
<span data-ttu-id="f4032-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4032-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4032-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4032-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="f4032-126">RedirectConfiguration для шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f4032-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="f4032-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f4032-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="f4032-128">Идентификатор RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f4032-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="f4032-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f4032-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="f4032-130">Наборы правил перезаписи по умолчанию для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="f4032-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="f4032-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="f4032-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="f4032-132">Идентификатор набора правил перезаписи по умолчанию для шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="f4032-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="f4032-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4032-133">-Name</span></span>
<span data-ttu-id="f4032-134">Указывает имя карты URL-пути, которое создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f4032-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f4032-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="f4032-135">-PathRules</span></span>
<span data-ttu-id="f4032-136">Задает список правил пути.</span><span class="sxs-lookup"><span data-stu-id="f4032-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="f4032-137">Обратите внимание, что правила путей зависят от порядка, они применяются в порядке их указания.</span><span class="sxs-lookup"><span data-stu-id="f4032-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="f4032-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4032-138">CommonParameters</span></span>
<span data-ttu-id="f4032-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4032-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4032-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4032-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4032-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4032-141">INPUTS</span></span>

### <span data-ttu-id="f4032-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="f4032-142">None</span></span>

## <span data-ttu-id="f4032-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4032-143">OUTPUTS</span></span>

### <span data-ttu-id="f4032-144">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="f4032-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="f4032-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4032-145">NOTES</span></span>

## <span data-ttu-id="f4032-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4032-146">RELATED LINKS</span></span>

[<span data-ttu-id="f4032-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f4032-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f4032-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f4032-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f4032-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f4032-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f4032-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f4032-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


