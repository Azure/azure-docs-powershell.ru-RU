---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 590793e8a2caeb360b88a7d41d91dcea07baacfd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909721"
---
# <span data-ttu-id="9e7ff-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e7ff-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="9e7ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="9e7ff-103">Создает массив сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="9e7ff-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9e7ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e7ff-104">SYNTAX</span></span>

### <span data-ttu-id="9e7ff-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e7ff-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e7ff-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9e7ff-106">SetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e7ff-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e7ff-107">DESCRIPTION</span></span>
<span data-ttu-id="9e7ff-108">Командлет **New-AzApplicationGatewayUrlPathMapConfig** создает массив сопоставлений URL-путей с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="9e7ff-108">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9e7ff-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e7ff-109">EXAMPLES</span></span>

### <span data-ttu-id="9e7ff-110">Пример 1: создание массива сопоставлений URL-путей с серверным пулом серверов</span><span class="sxs-lookup"><span data-stu-id="9e7ff-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="9e7ff-111">Эта команда создает массив сопоставлений URL-путей с пулом серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="9e7ff-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="9e7ff-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e7ff-112">PARAMETERS</span></span>

### <span data-ttu-id="9e7ff-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9e7ff-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="9e7ff-114">Указывает используемый по умолчанию пул серверных адресов для маршрутизации на случай, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="9e7ff-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="9e7ff-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9e7ff-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="9e7ff-116">Указывает идентификатор пула адресных адресов сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9e7ff-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="9e7ff-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9e7ff-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="9e7ff-118">Задает параметры HTTP по умолчанию для использования в случае, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="9e7ff-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="9e7ff-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="9e7ff-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="9e7ff-120">Указывает идентификатор HTTP-параметров по умолчанию для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="9e7ff-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="9e7ff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e7ff-121">-DefaultProfile</span></span>
<span data-ttu-id="9e7ff-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e7ff-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e7ff-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e7ff-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="9e7ff-124">RedirectConfiguration для шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9e7ff-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="9e7ff-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9e7ff-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="9e7ff-126">Идентификатор RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9e7ff-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="9e7ff-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e7ff-127">-Name</span></span>
<span data-ttu-id="9e7ff-128">Указывает имя карты URL-пути, которое создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9e7ff-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9e7ff-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="9e7ff-129">-PathRules</span></span>
<span data-ttu-id="9e7ff-130">Задает список правил пути.</span><span class="sxs-lookup"><span data-stu-id="9e7ff-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="9e7ff-131">Обратите внимание, что правила путей зависят от порядка, они применяются в порядке их указания.</span><span class="sxs-lookup"><span data-stu-id="9e7ff-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="9e7ff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e7ff-132">CommonParameters</span></span>
<span data-ttu-id="9e7ff-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e7ff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e7ff-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e7ff-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e7ff-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e7ff-135">INPUTS</span></span>

## <span data-ttu-id="9e7ff-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e7ff-136">OUTPUTS</span></span>

### <span data-ttu-id="9e7ff-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="9e7ff-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="9e7ff-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e7ff-138">NOTES</span></span>

## <span data-ttu-id="9e7ff-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e7ff-139">RELATED LINKS</span></span>

[<span data-ttu-id="9e7ff-140">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e7ff-140">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9e7ff-141">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e7ff-141">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9e7ff-142">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e7ff-142">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9e7ff-143">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e7ff-143">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


