---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 1b6e5c2c2a28333e51c74d9621a3fd607f6a652d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913859"
---
# <span data-ttu-id="4aef3-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4aef3-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4aef3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4aef3-102">SYNOPSIS</span></span>
<span data-ttu-id="4aef3-103">Добавляет массив сопоставлений URL-путей в пул серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="4aef3-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aef3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4aef3-104">SYNTAX</span></span>

### <span data-ttu-id="4aef3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4aef3-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aef3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4aef3-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aef3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4aef3-107">DESCRIPTION</span></span>
<span data-ttu-id="4aef3-108">Командлет **Add-AzureRmApplicationGatewayUrlPathMapConfig** Добавляет массив сопоставлений URL-путей в пул серверов заднего уровня.</span><span class="sxs-lookup"><span data-stu-id="4aef3-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="4aef3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4aef3-109">EXAMPLES</span></span>

### <span data-ttu-id="4aef3-110">1:</span><span class="sxs-lookup"><span data-stu-id="4aef3-110">1:</span></span>
```

```

## <span data-ttu-id="4aef3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4aef3-111">PARAMETERS</span></span>

### <span data-ttu-id="4aef3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4aef3-112">-ApplicationGateway</span></span>
<span data-ttu-id="4aef3-113">Указывает шлюз приложений, с которым этот командлет добавляет конфигурацию карты URL-пути.</span><span class="sxs-lookup"><span data-stu-id="4aef3-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="4aef3-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4aef3-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="4aef3-115">Указывает используемый по умолчанию пул серверных адресов для маршрутизации на случай, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="4aef3-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="4aef3-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4aef3-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="4aef3-117">Указывает идентификатор пула адресных адресов сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4aef3-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="4aef3-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4aef3-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="4aef3-119">Задает параметры HTTP по умолчанию для использования в случае, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="4aef3-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="4aef3-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="4aef3-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="4aef3-121">Указывает идентификатор HTTP-параметров по умолчанию для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="4aef3-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="4aef3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aef3-122">-DefaultProfile</span></span>
<span data-ttu-id="4aef3-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4aef3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4aef3-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4aef3-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="4aef3-125">RedirectConfiguration для шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4aef3-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="4aef3-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4aef3-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="4aef3-127">Идентификатор RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4aef3-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="4aef3-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4aef3-128">-Name</span></span>
<span data-ttu-id="4aef3-129">Указывает имя карты URL-пути, которое этот командлет добавляет в пул внутренних серверов.</span><span class="sxs-lookup"><span data-stu-id="4aef3-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="4aef3-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="4aef3-130">-PathRules</span></span>
<span data-ttu-id="4aef3-131">Задает список правил пути.</span><span class="sxs-lookup"><span data-stu-id="4aef3-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="4aef3-132">Правила путей зависят от порядка, они применяются в порядке их указания.</span><span class="sxs-lookup"><span data-stu-id="4aef3-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="4aef3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aef3-133">CommonParameters</span></span>
<span data-ttu-id="4aef3-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4aef3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aef3-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aef3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aef3-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4aef3-136">INPUTS</span></span>

### <span data-ttu-id="4aef3-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4aef3-137">PSApplicationGateway</span></span>
<span data-ttu-id="4aef3-138">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4aef3-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="4aef3-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4aef3-139">OUTPUTS</span></span>

### <span data-ttu-id="4aef3-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4aef3-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4aef3-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="4aef3-141">NOTES</span></span>

## <span data-ttu-id="4aef3-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4aef3-142">RELATED LINKS</span></span>

[<span data-ttu-id="4aef3-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4aef3-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4aef3-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4aef3-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4aef3-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4aef3-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4aef3-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4aef3-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


