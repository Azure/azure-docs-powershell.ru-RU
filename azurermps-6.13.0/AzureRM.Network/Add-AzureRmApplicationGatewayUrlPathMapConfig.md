---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 321c7272c02b4e5555f731d3a9dbaa7d806c0727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564312"
---
# <span data-ttu-id="d5381-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d5381-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d5381-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5381-102">SYNOPSIS</span></span>
<span data-ttu-id="d5381-103">Добавляет массив сопоставлений URL-путей в пул серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="d5381-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5381-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5381-104">SYNTAX</span></span>

### <span data-ttu-id="d5381-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5381-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5381-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d5381-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5381-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5381-107">DESCRIPTION</span></span>
<span data-ttu-id="d5381-108">Командлет **Add-AzureRmApplicationGatewayUrlPathMapConfig** Добавляет массив сопоставлений URL-путей в пул серверов заднего уровня.</span><span class="sxs-lookup"><span data-stu-id="d5381-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="d5381-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5381-109">EXAMPLES</span></span>

## <span data-ttu-id="d5381-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5381-110">PARAMETERS</span></span>

### <span data-ttu-id="d5381-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5381-111">-ApplicationGateway</span></span>
<span data-ttu-id="d5381-112">Указывает шлюз приложений, с которым этот командлет добавляет конфигурацию карты URL-пути.</span><span class="sxs-lookup"><span data-stu-id="d5381-112">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5381-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d5381-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="d5381-114">Указывает используемый по умолчанию пул серверных адресов для маршрутизации на случай, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="d5381-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5381-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d5381-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="d5381-116">Указывает идентификатор пула адресных адресов сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d5381-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="d5381-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d5381-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="d5381-118">Задает параметры HTTP по умолчанию для использования в случае, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="d5381-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5381-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d5381-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="d5381-120">Указывает идентификатор HTTP-параметров по умолчанию для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="d5381-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="d5381-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5381-121">-DefaultProfile</span></span>
<span data-ttu-id="d5381-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5381-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5381-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5381-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="d5381-124">RedirectConfiguration для шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d5381-124">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5381-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d5381-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="d5381-126">Идентификатор RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d5381-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d5381-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5381-127">-Name</span></span>
<span data-ttu-id="d5381-128">Указывает имя карты URL-пути, которое этот командлет добавляет в пул внутренних серверов.</span><span class="sxs-lookup"><span data-stu-id="d5381-128">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="d5381-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="d5381-129">-PathRules</span></span>
<span data-ttu-id="d5381-130">Задает список правил пути.</span><span class="sxs-lookup"><span data-stu-id="d5381-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="d5381-131">Правила путей зависят от порядка, они применяются в порядке их указания.</span><span class="sxs-lookup"><span data-stu-id="d5381-131">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="d5381-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5381-132">CommonParameters</span></span>
<span data-ttu-id="d5381-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5381-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5381-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5381-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5381-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5381-135">INPUTS</span></span>

### <span data-ttu-id="d5381-136">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5381-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="d5381-137">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d5381-137">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="d5381-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5381-138">OUTPUTS</span></span>

### <span data-ttu-id="d5381-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5381-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d5381-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5381-140">NOTES</span></span>

## <span data-ttu-id="d5381-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5381-141">RELATED LINKS</span></span>

[<span data-ttu-id="d5381-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d5381-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d5381-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d5381-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d5381-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d5381-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d5381-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d5381-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


