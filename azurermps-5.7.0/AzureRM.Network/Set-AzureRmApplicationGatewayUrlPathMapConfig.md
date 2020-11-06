---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 949de1a2016ffbecb96a8f10a34435cedd284ec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568229"
---
# <span data-ttu-id="b497c-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b497c-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="b497c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b497c-102">SYNOPSIS</span></span>
<span data-ttu-id="b497c-103">Задает конфигурацию для массива сопоставлений URL-путей с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="b497c-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b497c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b497c-104">SYNTAX</span></span>

### <span data-ttu-id="b497c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b497c-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b497c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b497c-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b497c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b497c-107">DESCRIPTION</span></span>
<span data-ttu-id="b497c-108">Командлет **Set-AzureRmApplicationGatewayUrlPathMapConfig** задает конфигурацию для массива сопоставлений URL-путей с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="b497c-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="b497c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b497c-109">EXAMPLES</span></span>

## <span data-ttu-id="b497c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b497c-110">PARAMETERS</span></span>

### <span data-ttu-id="b497c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b497c-111">-ApplicationGateway</span></span>
<span data-ttu-id="b497c-112">Указывает шлюз приложений, для которого этот командлет задает конфигурацию карты URL-пути.</span><span class="sxs-lookup"><span data-stu-id="b497c-112">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="b497c-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b497c-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="b497c-114">Указывает используемый по умолчанию пул серверных адресов для маршрутизации на случай, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="b497c-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="b497c-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b497c-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="b497c-116">Указывает идентификатор пула адресных адресов сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b497c-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="b497c-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b497c-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="b497c-118">Задает параметры HTTP по умолчанию для использования в случае, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="b497c-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="b497c-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="b497c-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="b497c-120">Указывает идентификатор HTTP-параметров по умолчанию для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="b497c-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="b497c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b497c-121">-DefaultProfile</span></span>
<span data-ttu-id="b497c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b497c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b497c-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b497c-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="b497c-124">RedirectConfiguration для шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b497c-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="b497c-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b497c-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="b497c-126">Идентификатор RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b497c-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="b497c-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b497c-127">-Name</span></span>
<span data-ttu-id="b497c-128">Указывает имя карты URL-пути, для которого этот командлет задает конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b497c-128">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="b497c-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="b497c-129">-PathRules</span></span>
<span data-ttu-id="b497c-130">Задает список правил пути.</span><span class="sxs-lookup"><span data-stu-id="b497c-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="b497c-131">Обратите внимание, что правила путей зависят от порядка, они применяются в порядке их указания.</span><span class="sxs-lookup"><span data-stu-id="b497c-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="b497c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b497c-132">CommonParameters</span></span>
<span data-ttu-id="b497c-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b497c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b497c-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b497c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b497c-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b497c-135">INPUTS</span></span>

### <span data-ttu-id="b497c-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b497c-136">PSApplicationGateway</span></span>
<span data-ttu-id="b497c-137">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b497c-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="b497c-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b497c-138">OUTPUTS</span></span>

### <span data-ttu-id="b497c-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b497c-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b497c-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="b497c-140">NOTES</span></span>

## <span data-ttu-id="b497c-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b497c-141">RELATED LINKS</span></span>

[<span data-ttu-id="b497c-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b497c-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b497c-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b497c-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b497c-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b497c-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b497c-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b497c-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


