---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246266"
---
# <span data-ttu-id="f6e4c-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6e4c-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="f6e4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e4c-103">Создание конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="f6e4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6e4c-104">SYNTAX</span></span>

### <span data-ttu-id="f6e4c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f6e4c-105">ByFieldsParameterSet (Default)</span></span>
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

### <span data-ttu-id="f6e4c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6e4c-106">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="f6e4c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6e4c-107">DESCRIPTION</span></span>
<span data-ttu-id="f6e4c-108">Командлет **New-AzCdnEndpoint** создает конечную точку сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f6e4c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6e4c-109">EXAMPLES</span></span>

## <span data-ttu-id="f6e4c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6e4c-110">PARAMETERS</span></span>

### <span data-ttu-id="f6e4c-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="f6e4c-111">-CdnProfile</span></span>
<span data-ttu-id="f6e4c-112">Указывает объект профиля CDN, в который добавляется конечная точка.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="f6e4c-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="f6e4c-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="f6e4c-114">Задает массив типов контента для сжатия между узлом EDGE и клиентом.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="f6e4c-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="f6e4c-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="f6e4c-116">Группа "источник по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="f6e4c-116">The default origin group.</span></span>

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

### <span data-ttu-id="f6e4c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e4c-117">-DefaultProfile</span></span>
<span data-ttu-id="f6e4c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6e4c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6e4c-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f6e4c-119">-DeliveryPolicy</span></span>
<span data-ttu-id="f6e4c-120">Политика доставки для этой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="f6e4c-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f6e4c-121">-EndpointName</span></span>
<span data-ttu-id="f6e4c-122">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="f6e4c-123">-Геофильтры</span><span class="sxs-lookup"><span data-stu-id="f6e4c-123">-GeoFilters</span></span>
<span data-ttu-id="f6e4c-124">Список географических фильтров, которые применяются к этой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="f6e4c-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="f6e4c-125">-HttpPort</span></span>
<span data-ttu-id="f6e4c-126">Указывает номер HTTP-порта на исходном сервере.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="f6e4c-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="f6e4c-127">-HttpsPort</span></span>
<span data-ttu-id="f6e4c-128">Задает номер HTTPS порта на исходном сервере.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="f6e4c-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="f6e4c-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="f6e4c-130">Указывает, включено ли сжатие для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="f6e4c-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="f6e4c-131">-IsHttpAllowed</span></span>
<span data-ttu-id="f6e4c-132">Указывает, включит ли конечную точку трафик HTTP.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="f6e4c-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="f6e4c-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="f6e4c-134">Указывает, включит ли конечную точку трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="f6e4c-135">-Location</span><span class="sxs-lookup"><span data-stu-id="f6e4c-135">-Location</span></span>
<span data-ttu-id="f6e4c-136">Указывает расположение ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="f6e4c-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="f6e4c-137">-OptimizationType</span></span>
<span data-ttu-id="f6e4c-138">Указывает любую оптимизацию, указанную в этой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="f6e4c-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e4c-139">-OriginGroupName</span></span>
<span data-ttu-id="f6e4c-140">Имя исходной группы.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="f6e4c-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f6e4c-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="f6e4c-142">Количество секунд между зондами проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="f6e4c-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="f6e4c-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="f6e4c-144">Относительный путь к источнику, который используется для определения работоспособности источника.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="f6e4c-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="f6e4c-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="f6e4c-146">Протокол, используемый для проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="f6e4c-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="f6e4c-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="f6e4c-148">Тип выполняемого запроса проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="f6e4c-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="f6e4c-149">-OriginHostHeader</span></span>
<span data-ttu-id="f6e4c-150">Задает заголовок исходного узла конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="f6e4c-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="f6e4c-151">-OriginHostName</span></span>
<span data-ttu-id="f6e4c-152">Указывает имя узла исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="f6e4c-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="f6e4c-153">-OriginId</span></span>
<span data-ttu-id="f6e4c-154">Идентификаторы группы источников Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="f6e4c-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="f6e4c-155">-OriginName</span></span>
<span data-ttu-id="f6e4c-156">Указывает имя ресурса исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="f6e4c-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="f6e4c-157">-OriginPath</span></span>
<span data-ttu-id="f6e4c-158">Указывает путь к исходному серверу.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="f6e4c-159">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="f6e4c-159">-Priority</span></span>
<span data-ttu-id="f6e4c-160">Приоритет источника для Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="f6e4c-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="f6e4c-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="f6e4c-162">Настраиваемое сообщение, которое должно быть включено в запрос на утверждение для подключения к частной ссылке.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="f6e4c-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="f6e4c-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="f6e4c-164">Расположение частной ссылки источника CDN в Azure.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="f6e4c-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f6e4c-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="f6e4c-166">Идентификатор ресурса частной ссылки источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="f6e4c-167">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="f6e4c-167">-ProbePath</span></span>
<span data-ttu-id="f6e4c-168">Указывает путь пробы для ускорения динамического сайта</span><span class="sxs-lookup"><span data-stu-id="f6e4c-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="f6e4c-169">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="f6e4c-169">-ProfileName</span></span>
<span data-ttu-id="f6e4c-170">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="f6e4c-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="f6e4c-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="f6e4c-172">Задает поведение конечной точки CDN, если строка запроса находится в URL-адресе запроса.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="f6e4c-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e4c-173">-ResourceGroupName</span></span>
<span data-ttu-id="f6e4c-174">Указывает имя группы ресурсов, к которой принадлежит эта конечная точка.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="f6e4c-175">-Тег</span><span class="sxs-lookup"><span data-stu-id="f6e4c-175">-Tag</span></span>
<span data-ttu-id="f6e4c-176">Теги, связываемые с конечной точкой CDN в Azure.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="f6e4c-177">-Weight</span><span class="sxs-lookup"><span data-stu-id="f6e4c-177">-Weight</span></span>
<span data-ttu-id="f6e4c-178">Вес источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="f6e4c-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6e4c-179">-Confirm</span></span>
<span data-ttu-id="f6e4c-180">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6e4c-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6e4c-181">-WhatIf</span></span>
<span data-ttu-id="f6e4c-182">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6e4c-183">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6e4c-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e4c-184">CommonParameters</span></span>
<span data-ttu-id="f6e4c-185">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6e4c-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e4c-186">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6e4c-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e4c-187">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6e4c-187">INPUTS</span></span>

### <span data-ttu-id="f6e4c-188">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="f6e4c-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="f6e4c-189">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6e4c-189">OUTPUTS</span></span>

### <span data-ttu-id="f6e4c-190">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6e4c-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="f6e4c-191">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6e4c-191">NOTES</span></span>

## <span data-ttu-id="f6e4c-192">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6e4c-192">RELATED LINKS</span></span>

[<span data-ttu-id="f6e4c-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6e4c-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="f6e4c-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6e4c-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="f6e4c-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6e4c-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="f6e4c-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6e4c-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="f6e4c-197">Остановить-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6e4c-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


