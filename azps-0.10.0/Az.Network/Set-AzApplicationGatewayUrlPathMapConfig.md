---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 5eb4fb0f036331fe68755a3a8ebddcd7e1b6e424
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911056"
---
# <span data-ttu-id="94bb4-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="94bb4-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="94bb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="94bb4-103">Задает конфигурацию для массива сопоставлений URL-путей с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="94bb4-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="94bb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94bb4-104">SYNTAX</span></span>

### <span data-ttu-id="94bb4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="94bb4-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94bb4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="94bb4-106">SetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94bb4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94bb4-107">DESCRIPTION</span></span>
<span data-ttu-id="94bb4-108">Командлет **Set-AzApplicationGatewayUrlPathMapConfig** задает конфигурацию для массива сопоставлений URL-путей с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="94bb4-108">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="94bb4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94bb4-109">EXAMPLES</span></span>

### <span data-ttu-id="94bb4-110">1:</span><span class="sxs-lookup"><span data-stu-id="94bb4-110">1:</span></span>
```

```

## <span data-ttu-id="94bb4-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94bb4-111">PARAMETERS</span></span>

### <span data-ttu-id="94bb4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94bb4-112">-ApplicationGateway</span></span>
<span data-ttu-id="94bb4-113">Указывает шлюз приложений, для которого этот командлет задает конфигурацию карты URL-пути.</span><span class="sxs-lookup"><span data-stu-id="94bb4-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="94bb4-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="94bb4-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="94bb4-115">Указывает используемый по умолчанию пул серверных адресов для маршрутизации на случай, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="94bb4-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94bb4-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="94bb4-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="94bb4-117">Указывает идентификатор пула адресных адресов сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="94bb4-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="94bb4-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="94bb4-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="94bb4-119">Задает параметры HTTP по умолчанию для использования в случае, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="94bb4-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94bb4-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="94bb4-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="94bb4-121">Указывает идентификатор HTTP-параметров по умолчанию для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="94bb4-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="94bb4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94bb4-122">-DefaultProfile</span></span>
<span data-ttu-id="94bb4-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94bb4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94bb4-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="94bb4-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="94bb4-125">RedirectConfiguration для шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="94bb4-125">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94bb4-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="94bb4-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="94bb4-127">Идентификатор RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="94bb4-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="94bb4-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="94bb4-128">-Name</span></span>
<span data-ttu-id="94bb4-129">Указывает имя карты URL-пути, для которого этот командлет задает конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="94bb4-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="94bb4-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="94bb4-130">-PathRules</span></span>
<span data-ttu-id="94bb4-131">Задает список правил пути.</span><span class="sxs-lookup"><span data-stu-id="94bb4-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="94bb4-132">Обратите внимание, что правила путей зависят от порядка, они применяются в порядке их указания.</span><span class="sxs-lookup"><span data-stu-id="94bb4-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94bb4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94bb4-133">CommonParameters</span></span>
<span data-ttu-id="94bb4-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94bb4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94bb4-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94bb4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94bb4-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94bb4-136">INPUTS</span></span>

### <span data-ttu-id="94bb4-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94bb4-137">PSApplicationGateway</span></span>
<span data-ttu-id="94bb4-138">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="94bb4-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="94bb4-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94bb4-139">OUTPUTS</span></span>

### <span data-ttu-id="94bb4-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94bb4-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="94bb4-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="94bb4-141">NOTES</span></span>

## <span data-ttu-id="94bb4-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94bb4-142">RELATED LINKS</span></span>

[<span data-ttu-id="94bb4-143">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="94bb4-143">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="94bb4-144">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="94bb4-144">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="94bb4-145">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="94bb4-145">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="94bb4-146">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="94bb4-146">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


