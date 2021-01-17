---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cf65e93f1dc2026c0fc973d694fe1f44718df12e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392879"
---
# <span data-ttu-id="ba672-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ba672-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="ba672-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba672-102">SYNOPSIS</span></span>
<span data-ttu-id="ba672-103">Создает массив сопоставлений URL-путей с пулом серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="ba672-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ba672-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ba672-104">SYNTAX</span></span>

### <span data-ttu-id="ba672-105">BackendSetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba672-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba672-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba672-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba672-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="ba672-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba672-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba672-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba672-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba672-109">DESCRIPTION</span></span>
<span data-ttu-id="ba672-110">Для создания массива сопоставлений URL-путей с пулом серверов серверов создается массив сопоставлений **URL-адресов.**</span><span class="sxs-lookup"><span data-stu-id="ba672-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ba672-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ba672-111">EXAMPLES</span></span>

### <span data-ttu-id="ba672-112">Пример 1. Создание массива сопоставлений URL-путей с пулом серверов серверов</span><span class="sxs-lookup"><span data-stu-id="ba672-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="ba672-113">Эта команда создает массив сопоставлений URL-путей с пулом серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="ba672-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ba672-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba672-114">PARAMETERS</span></span>

### <span data-ttu-id="ba672-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ba672-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="ba672-116">Определяет пул адресов для маршрутов по умолчанию на случай, если ни одно из правил, указанных в параметре *pathRules.*</span><span class="sxs-lookup"><span data-stu-id="ba672-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="ba672-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ba672-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="ba672-118">Определяет стандартный ИД пула адресов для backend.</span><span class="sxs-lookup"><span data-stu-id="ba672-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="ba672-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ba672-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="ba672-120">Определяет параметры HTTP по умолчанию, которые будут применяться, если ни одно из правил, указанных в *параметре pathRules.*</span><span class="sxs-lookup"><span data-stu-id="ba672-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="ba672-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="ba672-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="ba672-122">Определяет стандартный ИД параметров HTTP по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ba672-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="ba672-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba672-123">-DefaultProfile</span></span>
<span data-ttu-id="ba672-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba672-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba672-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba672-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="ba672-126">Перенаправление RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ba672-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="ba672-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ba672-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="ba672-128">ID of the application gateway default RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba672-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="ba672-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba672-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="ba672-130">Набор правил переописи шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ba672-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="ba672-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="ba672-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="ba672-132">ID of the application gateway default rewrite rule set</span><span class="sxs-lookup"><span data-stu-id="ba672-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="ba672-133">-Name</span><span class="sxs-lookup"><span data-stu-id="ba672-133">-Name</span></span>
<span data-ttu-id="ba672-134">Указывает имя карты URL-адреса, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba672-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ba672-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="ba672-135">-PathRules</span></span>
<span data-ttu-id="ba672-136">Определяет список правил пути.</span><span class="sxs-lookup"><span data-stu-id="ba672-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="ba672-137">Обратите внимание на то, что правила пути в порядке с конфиденциальной порядок они применяются в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="ba672-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="ba672-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba672-138">CommonParameters</span></span>
<span data-ttu-id="ba672-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba672-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba672-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba672-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba672-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba672-141">INPUTS</span></span>

### <span data-ttu-id="ba672-142">Нет</span><span class="sxs-lookup"><span data-stu-id="ba672-142">None</span></span>

## <span data-ttu-id="ba672-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba672-143">OUTPUTS</span></span>

### <span data-ttu-id="ba672-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="ba672-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="ba672-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ba672-145">NOTES</span></span>

## <span data-ttu-id="ba672-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba672-146">RELATED LINKS</span></span>

[<span data-ttu-id="ba672-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ba672-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ba672-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ba672-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ba672-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ba672-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ba672-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ba672-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


