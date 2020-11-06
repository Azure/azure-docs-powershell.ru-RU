---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 62a4859b5a64003956a4975411f809176f2917e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566560"
---
# <span data-ttu-id="b14b4-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b14b4-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="b14b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b14b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b14b4-103">Создание конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="b14b4-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b14b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b14b4-104">SYNTAX</span></span>

### <span data-ttu-id="b14b4-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b14b4-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b14b4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b14b4-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b14b4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b14b4-107">DESCRIPTION</span></span>
<span data-ttu-id="b14b4-108">Командлет **New-AzureRmCdnEndpoint** создает конечную точку сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="b14b4-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b14b4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b14b4-109">EXAMPLES</span></span>

## <span data-ttu-id="b14b4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b14b4-110">PARAMETERS</span></span>

### <span data-ttu-id="b14b4-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b14b4-111">-CdnProfile</span></span>
<span data-ttu-id="b14b4-112">Указывает объект профиля CDN, в который добавляется конечная точка.</span><span class="sxs-lookup"><span data-stu-id="b14b4-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="b14b4-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="b14b4-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="b14b4-114">Задает массив типов контента для сжатия между узлом EDGE и клиентом.</span><span class="sxs-lookup"><span data-stu-id="b14b4-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="b14b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b14b4-115">-DefaultProfile</span></span>
<span data-ttu-id="b14b4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b14b4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b14b4-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="b14b4-117">-DeliveryPolicy</span></span>
<span data-ttu-id="b14b4-118">Политика доставки для этой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b14b4-118">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="b14b4-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b14b4-119">-EndpointName</span></span>
<span data-ttu-id="b14b4-120">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b14b4-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="b14b4-121">-Геофильтры</span><span class="sxs-lookup"><span data-stu-id="b14b4-121">-GeoFilters</span></span>
<span data-ttu-id="b14b4-122">Список географических фильтров, которые применяются к этой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="b14b4-122">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="b14b4-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="b14b4-123">-HttpPort</span></span>
<span data-ttu-id="b14b4-124">Указывает номер HTTP-порта на исходном сервере.</span><span class="sxs-lookup"><span data-stu-id="b14b4-124">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="b14b4-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="b14b4-125">-HttpsPort</span></span>
<span data-ttu-id="b14b4-126">Задает номер HTTPS порта на исходном сервере.</span><span class="sxs-lookup"><span data-stu-id="b14b4-126">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="b14b4-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="b14b4-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="b14b4-128">Указывает, включено ли сжатие для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b14b4-128">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="b14b4-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="b14b4-129">-IsHttpAllowed</span></span>
<span data-ttu-id="b14b4-130">Указывает, включит ли конечную точку трафик HTTP.</span><span class="sxs-lookup"><span data-stu-id="b14b4-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="b14b4-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="b14b4-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="b14b4-132">Указывает, включит ли конечную точку трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b14b4-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="b14b4-133">-Location</span><span class="sxs-lookup"><span data-stu-id="b14b4-133">-Location</span></span>
<span data-ttu-id="b14b4-134">Указывает расположение ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b14b4-134">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="b14b4-135">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="b14b4-135">-OptimizationType</span></span>
<span data-ttu-id="b14b4-136">Указывает любую оптимизацию, указанную в этой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="b14b4-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="b14b4-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="b14b4-137">-OriginHostHeader</span></span>
<span data-ttu-id="b14b4-138">Задает заголовок исходного узла конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b14b4-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="b14b4-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="b14b4-139">-OriginHostName</span></span>
<span data-ttu-id="b14b4-140">Указывает имя узла исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="b14b4-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="b14b4-141">-OriginName</span><span class="sxs-lookup"><span data-stu-id="b14b4-141">-OriginName</span></span>
<span data-ttu-id="b14b4-142">Указывает имя ресурса исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="b14b4-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="b14b4-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="b14b4-143">-OriginPath</span></span>
<span data-ttu-id="b14b4-144">Указывает путь к исходному серверу.</span><span class="sxs-lookup"><span data-stu-id="b14b4-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="b14b4-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="b14b4-145">-ProbePath</span></span>
<span data-ttu-id="b14b4-146">Указывает путь пробы для ускорения динамического сайта</span><span class="sxs-lookup"><span data-stu-id="b14b4-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="b14b4-147">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="b14b4-147">-ProfileName</span></span>
<span data-ttu-id="b14b4-148">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="b14b4-148">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="b14b4-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="b14b4-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="b14b4-150">Задает поведение конечной точки CDN, если строка запроса находится в URL-адресе запроса.</span><span class="sxs-lookup"><span data-stu-id="b14b4-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="b14b4-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b14b4-151">-ResourceGroupName</span></span>
<span data-ttu-id="b14b4-152">Указывает имя группы ресурсов, к которой принадлежит эта конечная точка.</span><span class="sxs-lookup"><span data-stu-id="b14b4-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="b14b4-153">-Тег</span><span class="sxs-lookup"><span data-stu-id="b14b4-153">-Tag</span></span>
<span data-ttu-id="b14b4-154">Теги, связываемые с конечной точкой CDN в Azure.</span><span class="sxs-lookup"><span data-stu-id="b14b4-154">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="b14b4-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b14b4-155">-Confirm</span></span>
<span data-ttu-id="b14b4-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b14b4-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b14b4-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b14b4-157">-WhatIf</span></span>
<span data-ttu-id="b14b4-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b14b4-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b14b4-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b14b4-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b14b4-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b14b4-160">CommonParameters</span></span>
<span data-ttu-id="b14b4-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b14b4-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b14b4-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b14b4-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b14b4-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b14b4-163">INPUTS</span></span>

### <span data-ttu-id="b14b4-164">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="b14b4-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="b14b4-165">Параметры: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b14b4-165">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="b14b4-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b14b4-166">OUTPUTS</span></span>

### <span data-ttu-id="b14b4-167">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b14b4-167">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="b14b4-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="b14b4-168">NOTES</span></span>

## <span data-ttu-id="b14b4-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b14b4-169">RELATED LINKS</span></span>

[<span data-ttu-id="b14b4-170">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b14b4-170">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b14b4-171">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b14b4-171">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b14b4-172">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b14b4-172">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b14b4-173">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b14b4-173">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="b14b4-174">Остановить-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b14b4-174">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


