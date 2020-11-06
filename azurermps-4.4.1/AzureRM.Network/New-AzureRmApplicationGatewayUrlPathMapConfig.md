---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 5c3a59b497208c761ffcf7a24bc12b5ab2c50f27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563884"
---
# <span data-ttu-id="0033c-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0033c-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="0033c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0033c-102">SYNOPSIS</span></span>
<span data-ttu-id="0033c-103">Создает массив сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="0033c-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0033c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0033c-104">SYNTAX</span></span>

### <span data-ttu-id="0033c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0033c-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0033c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0033c-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0033c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0033c-107">DESCRIPTION</span></span>
<span data-ttu-id="0033c-108">Командлет **New-AzureRmApplicationGatewayUrlPathMapConfig** создает массив сопоставлений URL-путей с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="0033c-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="0033c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0033c-109">EXAMPLES</span></span>

### <span data-ttu-id="0033c-110">Пример 1: создание массива сопоставлений URL-путей с серверным пулом серверов</span><span class="sxs-lookup"><span data-stu-id="0033c-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="0033c-111">Эта команда создает массив сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="0033c-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="0033c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0033c-112">PARAMETERS</span></span>

### <span data-ttu-id="0033c-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0033c-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="0033c-114">Указывает используемый по умолчанию пул серверных адресов для маршрутизации на случай, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="0033c-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="0033c-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0033c-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="0033c-116">Указывает идентификатор пула адресных адресов сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0033c-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="0033c-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0033c-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="0033c-118">Задает параметры HTTP по умолчанию для использования в случае, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="0033c-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="0033c-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="0033c-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="0033c-120">Указывает идентификатор HTTP-параметров по умолчанию для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="0033c-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="0033c-121">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0033c-121">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="0033c-122">RedirectConfiguration для шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0033c-122">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="0033c-123">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0033c-123">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="0033c-124">Идентификатор RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0033c-124">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="0033c-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0033c-125">-Name</span></span>
<span data-ttu-id="0033c-126">Указывает имя карты URL-пути, которое создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0033c-126">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0033c-127">-PathRules</span><span class="sxs-lookup"><span data-stu-id="0033c-127">-PathRules</span></span>
<span data-ttu-id="0033c-128">Задает список правил пути.</span><span class="sxs-lookup"><span data-stu-id="0033c-128">Specifies a list of path rules.</span></span>
<span data-ttu-id="0033c-129">Обратите внимание, что правила путей зависят от порядка, они применяются в порядке их указания.</span><span class="sxs-lookup"><span data-stu-id="0033c-129">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="0033c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0033c-130">-DefaultProfile</span></span>
<span data-ttu-id="0033c-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0033c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0033c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0033c-132">CommonParameters</span></span>
<span data-ttu-id="0033c-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0033c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0033c-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0033c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0033c-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0033c-135">INPUTS</span></span>

## <span data-ttu-id="0033c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0033c-136">OUTPUTS</span></span>

### <span data-ttu-id="0033c-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="0033c-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="0033c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="0033c-138">NOTES</span></span>

## <span data-ttu-id="0033c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0033c-139">RELATED LINKS</span></span>

[<span data-ttu-id="0033c-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0033c-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0033c-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0033c-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0033c-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0033c-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0033c-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0033c-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


