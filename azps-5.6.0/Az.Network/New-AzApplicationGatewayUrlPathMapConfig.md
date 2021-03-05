---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ebb73225a8afa7bb4c1061326aa9262dd46d9dc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011891"
---
# <span data-ttu-id="ad025-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ad025-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="ad025-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad025-102">SYNOPSIS</span></span>
<span data-ttu-id="ad025-103">Создает массив сопоставлений URL-путей с пулом серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="ad025-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ad025-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad025-104">SYNTAX</span></span>

### <span data-ttu-id="ad025-105">BackendSetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad025-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad025-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad025-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad025-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="ad025-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad025-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad025-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad025-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad025-109">DESCRIPTION</span></span>
<span data-ttu-id="ad025-110">Для создания массива сопоставлений URL-путей с пулом серверов создается массив сопоставлений **URL-адресовGatewayUrlPathMapConfig.**</span><span class="sxs-lookup"><span data-stu-id="ad025-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ad025-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad025-111">EXAMPLES</span></span>

### <span data-ttu-id="ad025-112">Пример 1. Создание массива сопоставлений URL-путей с пулом серверов серверов</span><span class="sxs-lookup"><span data-stu-id="ad025-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="ad025-113">Эта команда создает массив сопоставлений URL-путей с пулом серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="ad025-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ad025-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad025-114">PARAMETERS</span></span>

### <span data-ttu-id="ad025-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ad025-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="ad025-116">Определяет пул адресов для маршрутов по умолчанию на случай, если ни одно из правил, указанных в параметре *pathRules.*</span><span class="sxs-lookup"><span data-stu-id="ad025-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="ad025-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ad025-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="ad025-118">Определяет стандартный ИД пула адресов для backend.</span><span class="sxs-lookup"><span data-stu-id="ad025-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="ad025-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ad025-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="ad025-120">Определяет параметры HTTP по умолчанию, которые будут применяться, если ни одно из правил, указанных в *параметре pathRules.*</span><span class="sxs-lookup"><span data-stu-id="ad025-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="ad025-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="ad025-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="ad025-122">Определяет стандартный ИД параметров HTTP по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad025-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="ad025-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad025-123">-DefaultProfile</span></span>
<span data-ttu-id="ad025-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad025-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad025-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad025-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="ad025-126">Перенаправление RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad025-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="ad025-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ad025-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="ad025-128">ID of the application gateway default RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad025-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="ad025-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ad025-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="ad025-130">Набор правил переописи шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad025-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="ad025-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="ad025-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="ad025-132">ID of the application gateway default rewrite rule set</span><span class="sxs-lookup"><span data-stu-id="ad025-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="ad025-133">-Name</span><span class="sxs-lookup"><span data-stu-id="ad025-133">-Name</span></span>
<span data-ttu-id="ad025-134">Указывает имя карты URL-адреса, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad025-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ad025-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="ad025-135">-PathRules</span></span>
<span data-ttu-id="ad025-136">Определяет список правил пути.</span><span class="sxs-lookup"><span data-stu-id="ad025-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="ad025-137">Обратите внимание на то, что правила пути в порядке с конфиденциальной порядок они применяются в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="ad025-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="ad025-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad025-138">CommonParameters</span></span>
<span data-ttu-id="ad025-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad025-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad025-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad025-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad025-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad025-141">INPUTS</span></span>

### <span data-ttu-id="ad025-142">Нет</span><span class="sxs-lookup"><span data-stu-id="ad025-142">None</span></span>

## <span data-ttu-id="ad025-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad025-143">OUTPUTS</span></span>

### <span data-ttu-id="ad025-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="ad025-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="ad025-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad025-145">NOTES</span></span>

## <span data-ttu-id="ad025-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad025-146">RELATED LINKS</span></span>

[<span data-ttu-id="ad025-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ad025-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ad025-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ad025-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ad025-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ad025-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ad025-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ad025-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


