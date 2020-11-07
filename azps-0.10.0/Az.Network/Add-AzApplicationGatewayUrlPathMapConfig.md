---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: eedf03e2468be36fadc519fc2e6b931c82433fc0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910150"
---
# <span data-ttu-id="09b44-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="09b44-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="09b44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09b44-102">SYNOPSIS</span></span>
<span data-ttu-id="09b44-103">Добавляет массив сопоставлений URL-путей в пул серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="09b44-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="09b44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09b44-104">SYNTAX</span></span>

### <span data-ttu-id="09b44-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="09b44-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09b44-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="09b44-106">SetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09b44-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09b44-107">DESCRIPTION</span></span>
<span data-ttu-id="09b44-108">Командлет **Add-AzApplicationGatewayUrlPathMapConfig** Добавляет массив сопоставлений URL-путей в пул серверов заднего уровня.</span><span class="sxs-lookup"><span data-stu-id="09b44-108">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="09b44-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09b44-109">EXAMPLES</span></span>

### <span data-ttu-id="09b44-110">1:</span><span class="sxs-lookup"><span data-stu-id="09b44-110">1:</span></span>
```

```

## <span data-ttu-id="09b44-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09b44-111">PARAMETERS</span></span>

### <span data-ttu-id="09b44-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09b44-112">-ApplicationGateway</span></span>
<span data-ttu-id="09b44-113">Указывает шлюз приложений, с которым этот командлет добавляет конфигурацию карты URL-пути.</span><span class="sxs-lookup"><span data-stu-id="09b44-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="09b44-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="09b44-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="09b44-115">Указывает используемый по умолчанию пул серверных адресов для маршрутизации на случай, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="09b44-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="09b44-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="09b44-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="09b44-117">Указывает идентификатор пула адресных адресов сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="09b44-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="09b44-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="09b44-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="09b44-119">Задает параметры HTTP по умолчанию для использования в случае, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="09b44-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="09b44-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="09b44-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="09b44-121">Указывает идентификатор HTTP-параметров по умолчанию для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="09b44-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="09b44-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09b44-122">-DefaultProfile</span></span>
<span data-ttu-id="09b44-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09b44-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09b44-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="09b44-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="09b44-125">RedirectConfiguration для шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="09b44-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="09b44-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="09b44-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="09b44-127">Идентификатор RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="09b44-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="09b44-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="09b44-128">-Name</span></span>
<span data-ttu-id="09b44-129">Указывает имя карты URL-пути, которое этот командлет добавляет в пул внутренних серверов.</span><span class="sxs-lookup"><span data-stu-id="09b44-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="09b44-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="09b44-130">-PathRules</span></span>
<span data-ttu-id="09b44-131">Задает список правил пути.</span><span class="sxs-lookup"><span data-stu-id="09b44-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="09b44-132">Правила путей зависят от порядка, они применяются в порядке их указания.</span><span class="sxs-lookup"><span data-stu-id="09b44-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="09b44-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b44-133">CommonParameters</span></span>
<span data-ttu-id="09b44-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09b44-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b44-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09b44-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b44-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09b44-136">INPUTS</span></span>

### <span data-ttu-id="09b44-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09b44-137">PSApplicationGateway</span></span>
<span data-ttu-id="09b44-138">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="09b44-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="09b44-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09b44-139">OUTPUTS</span></span>

### <span data-ttu-id="09b44-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09b44-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="09b44-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="09b44-141">NOTES</span></span>

## <span data-ttu-id="09b44-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09b44-142">RELATED LINKS</span></span>

[<span data-ttu-id="09b44-143">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="09b44-143">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="09b44-144">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="09b44-144">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="09b44-145">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="09b44-145">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="09b44-146">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="09b44-146">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


