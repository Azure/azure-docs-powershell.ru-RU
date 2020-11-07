---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 2f4b1abc5d6cd6d55eef3c45c01a2939842e32c6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914422"
---
# <span data-ttu-id="8d5df-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8d5df-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="8d5df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d5df-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5df-103">Создание правила маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8d5df-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d5df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d5df-104">SYNTAX</span></span>

### <span data-ttu-id="8d5df-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d5df-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d5df-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8d5df-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d5df-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d5df-107">DESCRIPTION</span></span>
<span data-ttu-id="8d5df-108">Командлет **Add-AzureRmApplicationGatewayRequestRoutingRule** создает правило маршрутизации запросов для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="8d5df-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="8d5df-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d5df-109">EXAMPLES</span></span>

### <span data-ttu-id="8d5df-110">Пример 1: Создание правила маршрутизации запросов для шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="8d5df-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="8d5df-111">Эта команда создает базовое правило маршрутизации запросов с именем Rule01 и сохраняет результат в переменной с именем $Rule.</span><span class="sxs-lookup"><span data-stu-id="8d5df-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="8d5df-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d5df-112">PARAMETERS</span></span>

### <span data-ttu-id="8d5df-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8d5df-113">-BackendAddressPool</span></span>
<span data-ttu-id="8d5df-114">Задает пул серверных адресов (объект) для создаваемого правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="8d5df-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="8d5df-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8d5df-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="8d5df-116">Указывает идентификатор пула серверного адреса для правила маршрутизации запросов, которое нужно создать.</span><span class="sxs-lookup"><span data-stu-id="8d5df-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="8d5df-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8d5df-117">-BackendHttpSettings</span></span>
<span data-ttu-id="8d5df-118">Задает серверные параметры HTTP, как объект, для создаваемого правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="8d5df-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="8d5df-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="8d5df-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="8d5df-120">Указывает идентификатор HTTP-параметров для правила маршрутизации запросов, которое нужно создать.</span><span class="sxs-lookup"><span data-stu-id="8d5df-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="8d5df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5df-121">-DefaultProfile</span></span>
<span data-ttu-id="8d5df-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d5df-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d5df-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="8d5df-123">-HttpListener</span></span>
<span data-ttu-id="8d5df-124">Задает прослушиватель HTTP для создаваемого правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="8d5df-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5df-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="8d5df-125">-HttpListenerId</span></span>
<span data-ttu-id="8d5df-126">Задает идентификатор HTTP-прослушивателя для создаваемого правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="8d5df-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="8d5df-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8d5df-127">-Name</span></span>
<span data-ttu-id="8d5df-128">Указывает имя правила маршрутизации запросов, которое создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8d5df-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8d5df-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d5df-129">-RedirectConfiguration</span></span>
<span data-ttu-id="8d5df-130">RedirectConfiguration шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="8d5df-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="8d5df-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8d5df-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="8d5df-132">Идентификатор RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="8d5df-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="8d5df-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="8d5df-133">-RuleType</span></span>
<span data-ttu-id="8d5df-134">Указывает тип правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="8d5df-134">Specifies type of the request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5df-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="8d5df-135">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d5df-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="8d5df-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="8d5df-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5df-137">CommonParameters</span></span>
<span data-ttu-id="8d5df-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d5df-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5df-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d5df-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5df-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d5df-140">INPUTS</span></span>

### <span data-ttu-id="8d5df-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8d5df-141">System.String</span></span>

## <span data-ttu-id="8d5df-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d5df-142">OUTPUTS</span></span>

### <span data-ttu-id="8d5df-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8d5df-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="8d5df-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d5df-144">NOTES</span></span>

## <span data-ttu-id="8d5df-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d5df-145">RELATED LINKS</span></span>

[<span data-ttu-id="8d5df-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8d5df-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8d5df-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8d5df-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8d5df-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8d5df-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8d5df-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8d5df-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


