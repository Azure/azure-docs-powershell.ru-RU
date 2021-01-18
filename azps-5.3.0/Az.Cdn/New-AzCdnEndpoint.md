---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519700"
---
# <span data-ttu-id="62045-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="62045-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="62045-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62045-102">SYNOPSIS</span></span>
<span data-ttu-id="62045-103">Создает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="62045-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="62045-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62045-104">SYNTAX</span></span>

### <span data-ttu-id="62045-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62045-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62045-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62045-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62045-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62045-107">DESCRIPTION</span></span>
<span data-ttu-id="62045-108">Для **этого создается** конечная точка сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="62045-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="62045-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62045-109">EXAMPLES</span></span>

## <span data-ttu-id="62045-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62045-110">PARAMETERS</span></span>

### <span data-ttu-id="62045-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="62045-111">-CdnProfile</span></span>
<span data-ttu-id="62045-112">Определяет объект профиля CDN, к которому добавляется конечная точка.</span><span class="sxs-lookup"><span data-stu-id="62045-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62045-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="62045-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="62045-114">Указывает массив типов контента для сжатия от edge node до клиента.</span><span class="sxs-lookup"><span data-stu-id="62045-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="62045-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="62045-116">Группа источник по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="62045-116">The default origin group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62045-117">-DefaultProfile</span></span>
<span data-ttu-id="62045-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="62045-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62045-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="62045-119">-DeliveryPolicy</span></span>
<span data-ttu-id="62045-120">Политика доставки для этой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="62045-120">The delivery policy for this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="62045-121">-EndpointName</span></span>
<span data-ttu-id="62045-122">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="62045-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="62045-123">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="62045-123">-GeoFilters</span></span>
<span data-ttu-id="62045-124">Список геофильтров, которые применяются к данной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="62045-124">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-125">-httpPort</span><span class="sxs-lookup"><span data-stu-id="62045-125">-HttpPort</span></span>
<span data-ttu-id="62045-126">Указывает номер порта HTTP на сервере-источнике.</span><span class="sxs-lookup"><span data-stu-id="62045-126">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="62045-127">-HttpsPort</span></span>
<span data-ttu-id="62045-128">Указывает номер порта HTTPS на сервере-источнике.</span><span class="sxs-lookup"><span data-stu-id="62045-128">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="62045-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="62045-130">Указывает, включено ли сжатие для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="62045-130">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="62045-131">-IsHttpAllowed</span></span>
<span data-ttu-id="62045-132">Указывает, включает ли конечная точка трафик HTTP.</span><span class="sxs-lookup"><span data-stu-id="62045-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="62045-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="62045-134">Указывает, включает ли конечная точка трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="62045-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-135">-Location</span><span class="sxs-lookup"><span data-stu-id="62045-135">-Location</span></span>
<span data-ttu-id="62045-136">Определяет расположение ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="62045-136">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="62045-137">-OptimizationType</span></span>
<span data-ttu-id="62045-138">Указывает оптимизацию, установленную этой конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="62045-138">Specifies any optimization this endpoint has.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="62045-139">-OriginGroupName</span></span>
<span data-ttu-id="62045-140">Имя группы источника.</span><span class="sxs-lookup"><span data-stu-id="62045-140">The name of the origin group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="62045-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="62045-142">Количество секунд между проверками здоровья.</span><span class="sxs-lookup"><span data-stu-id="62045-142">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="62045-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="62045-144">Путь относительно источника, используемого для определения его состояния.</span><span class="sxs-lookup"><span data-stu-id="62045-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="62045-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="62045-146">Протокол для использования в медицинских организациях.</span><span class="sxs-lookup"><span data-stu-id="62045-146">Protocol to use for health probe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="62045-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="62045-148">Тип запроса на проверку состояния здоровья.</span><span class="sxs-lookup"><span data-stu-id="62045-148">The type of health probe request that is made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="62045-149">-OriginHostHeader</span></span>
<span data-ttu-id="62045-150">Определяет начало хоста источника для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="62045-150">Specifies the origin host head of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="62045-151">-OriginHostName</span></span>
<span data-ttu-id="62045-152">Указывает имя хоста сервера-источника.</span><span class="sxs-lookup"><span data-stu-id="62045-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="62045-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="62045-153">-OriginId</span></span>
<span data-ttu-id="62045-154">Azure CDN origin ids.</span><span class="sxs-lookup"><span data-stu-id="62045-154">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="62045-155">-OriginName</span></span>
<span data-ttu-id="62045-156">Указывает имя ресурса сервера-источника.</span><span class="sxs-lookup"><span data-stu-id="62045-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="62045-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="62045-157">-OriginPath</span></span>
<span data-ttu-id="62045-158">Путь к серверу-источнику.</span><span class="sxs-lookup"><span data-stu-id="62045-158">Specifies the path of the origin server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-159">-Priority</span><span class="sxs-lookup"><span data-stu-id="62045-159">-Priority</span></span>
<span data-ttu-id="62045-160">Приоритет источника через CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="62045-160">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="62045-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="62045-162">Пользовательское сообщение, которое будет включено в запрос на утверждение для подключения к личной ссылке.</span><span class="sxs-lookup"><span data-stu-id="62045-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="62045-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="62045-164">Расположение закрытой ссылки в источнике Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="62045-164">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="62045-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="62045-166">Azure CDN origin private link resource id.</span><span class="sxs-lookup"><span data-stu-id="62045-166">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-167">-СкайпPath</span><span class="sxs-lookup"><span data-stu-id="62045-167">-ProbePath</span></span>
<span data-ttu-id="62045-168">Путь в динамическом ускорении сайта.</span><span class="sxs-lookup"><span data-stu-id="62045-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-169">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="62045-169">-ProfileName</span></span>
<span data-ttu-id="62045-170">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="62045-170">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="62045-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="62045-172">Определяет поведение конечной точки CDN, если строка запроса находится в URL-адресе запроса.</span><span class="sxs-lookup"><span data-stu-id="62045-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSQueryStringCachingBehavior]
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62045-173">-ResourceGroupName</span></span>
<span data-ttu-id="62045-174">Имя группы ресурсов, к которой относится эта конечная точка.</span><span class="sxs-lookup"><span data-stu-id="62045-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="62045-175">-Tag</span></span>
<span data-ttu-id="62045-176">Теги, которые нужно связать с конечной точкой CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="62045-176">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-177">-Weight</span><span class="sxs-lookup"><span data-stu-id="62045-177">-Weight</span></span>
<span data-ttu-id="62045-178">Вес источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="62045-178">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62045-179">-Confirm</span></span>
<span data-ttu-id="62045-180">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="62045-180">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62045-181">-WhatIf</span></span>
<span data-ttu-id="62045-182">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62045-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62045-183">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="62045-183">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62045-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62045-184">CommonParameters</span></span>
<span data-ttu-id="62045-185">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62045-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62045-186">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62045-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62045-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62045-187">INPUTS</span></span>

### <span data-ttu-id="62045-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="62045-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="62045-189">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62045-189">OUTPUTS</span></span>

### <span data-ttu-id="62045-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="62045-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="62045-191">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62045-191">NOTES</span></span>

## <span data-ttu-id="62045-192">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62045-192">RELATED LINKS</span></span>

[<span data-ttu-id="62045-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="62045-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="62045-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="62045-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="62045-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="62045-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="62045-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="62045-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="62045-197">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="62045-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


