---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9c902070ad71048c625115ba2803352a3b1132bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956008"
---
# <span data-ttu-id="297c1-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="297c1-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="297c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="297c1-102">SYNOPSIS</span></span>
<span data-ttu-id="297c1-103">Создает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="297c1-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="297c1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="297c1-104">SYNTAX</span></span>

### <span data-ttu-id="297c1-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="297c1-105">ByFieldsParameterSet (Default)</span></span>
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

### <span data-ttu-id="297c1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="297c1-106">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="297c1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="297c1-107">DESCRIPTION</span></span>
<span data-ttu-id="297c1-108">Для **этого создается** конечная точка сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="297c1-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="297c1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="297c1-109">EXAMPLES</span></span>

## <span data-ttu-id="297c1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="297c1-110">PARAMETERS</span></span>

### <span data-ttu-id="297c1-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="297c1-111">-CdnProfile</span></span>
<span data-ttu-id="297c1-112">Определяет объект профиля CDN, к которому добавляется конечная точка.</span><span class="sxs-lookup"><span data-stu-id="297c1-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="297c1-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="297c1-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="297c1-114">Указывает массив типов контента для сжатия от edge node до клиента.</span><span class="sxs-lookup"><span data-stu-id="297c1-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="297c1-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="297c1-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="297c1-116">Группа источник по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="297c1-116">The default origin group.</span></span>

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

### <span data-ttu-id="297c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="297c1-117">-DefaultProfile</span></span>
<span data-ttu-id="297c1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="297c1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="297c1-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="297c1-119">-DeliveryPolicy</span></span>
<span data-ttu-id="297c1-120">Политика доставки для этой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="297c1-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="297c1-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="297c1-121">-EndpointName</span></span>
<span data-ttu-id="297c1-122">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="297c1-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="297c1-123">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="297c1-123">-GeoFilters</span></span>
<span data-ttu-id="297c1-124">Список геофильтров, которые применяются к этой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="297c1-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="297c1-125">-httpPort</span><span class="sxs-lookup"><span data-stu-id="297c1-125">-HttpPort</span></span>
<span data-ttu-id="297c1-126">Указывает номер порта HTTP на сервере-источнике.</span><span class="sxs-lookup"><span data-stu-id="297c1-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="297c1-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="297c1-127">-HttpsPort</span></span>
<span data-ttu-id="297c1-128">Указывает номер порта HTTPS на сервере-источнике.</span><span class="sxs-lookup"><span data-stu-id="297c1-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="297c1-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="297c1-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="297c1-130">Указывает, включено ли сжатие для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="297c1-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="297c1-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="297c1-131">-IsHttpAllowed</span></span>
<span data-ttu-id="297c1-132">Указывает, включает ли конечная точка трафик HTTP.</span><span class="sxs-lookup"><span data-stu-id="297c1-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="297c1-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="297c1-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="297c1-134">Указывает, включает ли конечная точка трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="297c1-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="297c1-135">-Location</span><span class="sxs-lookup"><span data-stu-id="297c1-135">-Location</span></span>
<span data-ttu-id="297c1-136">Определяет расположение ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="297c1-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="297c1-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="297c1-137">-OptimizationType</span></span>
<span data-ttu-id="297c1-138">Указывает оптимизацию, установленную этой конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="297c1-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="297c1-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="297c1-139">-OriginGroupName</span></span>
<span data-ttu-id="297c1-140">Имя группы источника.</span><span class="sxs-lookup"><span data-stu-id="297c1-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="297c1-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="297c1-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="297c1-142">Количество секунд между проверками здоровья.</span><span class="sxs-lookup"><span data-stu-id="297c1-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="297c1-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="297c1-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="297c1-144">Путь относительно источника, используемого для определения его состояния.</span><span class="sxs-lookup"><span data-stu-id="297c1-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="297c1-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="297c1-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="297c1-146">Протокол для использования в медицинских организациях.</span><span class="sxs-lookup"><span data-stu-id="297c1-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="297c1-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="297c1-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="297c1-148">Тип запроса на проверку состояния здоровья.</span><span class="sxs-lookup"><span data-stu-id="297c1-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="297c1-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="297c1-149">-OriginHostHeader</span></span>
<span data-ttu-id="297c1-150">Определяет начало хоста источника для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="297c1-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="297c1-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="297c1-151">-OriginHostName</span></span>
<span data-ttu-id="297c1-152">Указывает имя хоста сервера-источника.</span><span class="sxs-lookup"><span data-stu-id="297c1-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="297c1-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="297c1-153">-OriginId</span></span>
<span data-ttu-id="297c1-154">Azure CDN origin ids.</span><span class="sxs-lookup"><span data-stu-id="297c1-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="297c1-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="297c1-155">-OriginName</span></span>
<span data-ttu-id="297c1-156">Указывает имя ресурса сервера-источника.</span><span class="sxs-lookup"><span data-stu-id="297c1-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="297c1-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="297c1-157">-OriginPath</span></span>
<span data-ttu-id="297c1-158">Путь к серверу-источнику.</span><span class="sxs-lookup"><span data-stu-id="297c1-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="297c1-159">-Priority</span><span class="sxs-lookup"><span data-stu-id="297c1-159">-Priority</span></span>
<span data-ttu-id="297c1-160">Приоритет источника через CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="297c1-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="297c1-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="297c1-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="297c1-162">Пользовательское сообщение, которое будет включено в запрос на утверждение для подключения к личной ссылке.</span><span class="sxs-lookup"><span data-stu-id="297c1-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="297c1-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="297c1-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="297c1-164">Расположение закрытой ссылки в источнике Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="297c1-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="297c1-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="297c1-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="297c1-166">Azure CDN origin private link resource id.</span><span class="sxs-lookup"><span data-stu-id="297c1-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="297c1-167">-СкайпPath</span><span class="sxs-lookup"><span data-stu-id="297c1-167">-ProbePath</span></span>
<span data-ttu-id="297c1-168">Путь к участкам динамического ускорения сайта.</span><span class="sxs-lookup"><span data-stu-id="297c1-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="297c1-169">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="297c1-169">-ProfileName</span></span>
<span data-ttu-id="297c1-170">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="297c1-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="297c1-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="297c1-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="297c1-172">Определяет поведение конечной точки CDN, если строка запроса находится в URL-адресе запроса.</span><span class="sxs-lookup"><span data-stu-id="297c1-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="297c1-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="297c1-173">-ResourceGroupName</span></span>
<span data-ttu-id="297c1-174">Имя группы ресурсов, к которой относится эта конечная точка.</span><span class="sxs-lookup"><span data-stu-id="297c1-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="297c1-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="297c1-175">-Tag</span></span>
<span data-ttu-id="297c1-176">Теги, которые нужно связать с конечной точкой CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="297c1-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="297c1-177">-Weight</span><span class="sxs-lookup"><span data-stu-id="297c1-177">-Weight</span></span>
<span data-ttu-id="297c1-178">Вес источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="297c1-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="297c1-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="297c1-179">-Confirm</span></span>
<span data-ttu-id="297c1-180">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="297c1-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="297c1-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="297c1-181">-WhatIf</span></span>
<span data-ttu-id="297c1-182">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="297c1-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="297c1-183">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="297c1-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="297c1-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297c1-184">CommonParameters</span></span>
<span data-ttu-id="297c1-185">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="297c1-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297c1-186">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="297c1-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297c1-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="297c1-187">INPUTS</span></span>

### <span data-ttu-id="297c1-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="297c1-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="297c1-189">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="297c1-189">OUTPUTS</span></span>

### <span data-ttu-id="297c1-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="297c1-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="297c1-191">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="297c1-191">NOTES</span></span>

## <span data-ttu-id="297c1-192">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="297c1-192">RELATED LINKS</span></span>

[<span data-ttu-id="297c1-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="297c1-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="297c1-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="297c1-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="297c1-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="297c1-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="297c1-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="297c1-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="297c1-197">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="297c1-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


