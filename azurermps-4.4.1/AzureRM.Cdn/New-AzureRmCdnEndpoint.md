---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 5d2bfdf2bf5f87ccb0213c006de8612b5eaf0730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567161"
---
# <span data-ttu-id="2d637-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d637-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="2d637-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d637-102">SYNOPSIS</span></span>
<span data-ttu-id="2d637-103">Создание конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="2d637-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d637-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d637-104">SYNTAX</span></span>

### <span data-ttu-id="2d637-105">Параметры, заданные для параметров полей (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d637-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d637-106">Параметр, заданный для параметров объекта</span><span class="sxs-lookup"><span data-stu-id="2d637-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d637-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d637-107">DESCRIPTION</span></span>
<span data-ttu-id="2d637-108">Командлет **New-AzureRmCdnEndpoint** создает конечную точку сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="2d637-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2d637-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d637-109">EXAMPLES</span></span>

## <span data-ttu-id="2d637-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d637-110">PARAMETERS</span></span>

### <span data-ttu-id="2d637-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="2d637-111">-CdnProfile</span></span>
<span data-ttu-id="2d637-112">Указывает объект профиля CDN, в который добавляется конечная точка.</span><span class="sxs-lookup"><span data-stu-id="2d637-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d637-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="2d637-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="2d637-114">Задает массив типов контента для сжатия между узлом EDGE и клиентом.</span><span class="sxs-lookup"><span data-stu-id="2d637-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="2d637-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2d637-115">-EndpointName</span></span>
<span data-ttu-id="2d637-116">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2d637-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="2d637-117">-Геофильтры</span><span class="sxs-lookup"><span data-stu-id="2d637-117">-GeoFilters</span></span>
<span data-ttu-id="2d637-118">Список географических фильтров, которые применяются к этой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2d637-118">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="2d637-119">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="2d637-119">-HttpPort</span></span>
<span data-ttu-id="2d637-120">Указывает номер HTTP-порта на исходном сервере.</span><span class="sxs-lookup"><span data-stu-id="2d637-120">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="2d637-121">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="2d637-121">-HttpsPort</span></span>
<span data-ttu-id="2d637-122">Задает номер HTTPS порта на исходном сервере.</span><span class="sxs-lookup"><span data-stu-id="2d637-122">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="2d637-123">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="2d637-123">-IsCompressionEnabled</span></span>
<span data-ttu-id="2d637-124">Указывает, включено ли сжатие для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2d637-124">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="2d637-125">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="2d637-125">-IsHttpAllowed</span></span>
<span data-ttu-id="2d637-126">Указывает, включит ли конечную точку трафик HTTP.</span><span class="sxs-lookup"><span data-stu-id="2d637-126">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="2d637-127">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="2d637-127">-IsHttpsAllowed</span></span>
<span data-ttu-id="2d637-128">Указывает, включит ли конечную точку трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2d637-128">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="2d637-129">-Location</span><span class="sxs-lookup"><span data-stu-id="2d637-129">-Location</span></span>
<span data-ttu-id="2d637-130">Указывает расположение ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2d637-130">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d637-131">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="2d637-131">-OptimizationType</span></span>
<span data-ttu-id="2d637-132">Указывает любую оптимизацию, указанную в этой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="2d637-132">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="2d637-133">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="2d637-133">-OriginHostHeader</span></span>
<span data-ttu-id="2d637-134">Задает заголовок исходного узла конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2d637-134">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="2d637-135">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="2d637-135">-OriginHostName</span></span>
<span data-ttu-id="2d637-136">Указывает имя узла исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="2d637-136">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="2d637-137">-OriginName</span><span class="sxs-lookup"><span data-stu-id="2d637-137">-OriginName</span></span>
<span data-ttu-id="2d637-138">Указывает имя ресурса исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="2d637-138">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="2d637-139">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="2d637-139">-OriginPath</span></span>
<span data-ttu-id="2d637-140">Указывает путь к исходному серверу.</span><span class="sxs-lookup"><span data-stu-id="2d637-140">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="2d637-141">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="2d637-141">-ProfileName</span></span>
<span data-ttu-id="2d637-142">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="2d637-142">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d637-143">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="2d637-143">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="2d637-144">Задает поведение конечной точки CDN, если строка запроса находится в URL-адресе запроса.</span><span class="sxs-lookup"><span data-stu-id="2d637-144">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="2d637-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d637-145">-ResourceGroupName</span></span>
<span data-ttu-id="2d637-146">Указывает имя группы ресурсов, к которой принадлежит эта конечная точка.</span><span class="sxs-lookup"><span data-stu-id="2d637-146">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d637-147">-Теги</span><span class="sxs-lookup"><span data-stu-id="2d637-147">-Tags</span></span>
<span data-ttu-id="2d637-148">Указывает хэш-таблицу тегов, связанных с этим ресурсом.</span><span class="sxs-lookup"><span data-stu-id="2d637-148">Specifies a hash table of the tags that associated with this resource.</span></span>

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

### <span data-ttu-id="2d637-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d637-149">-Confirm</span></span>
<span data-ttu-id="2d637-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d637-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d637-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d637-151">-WhatIf</span></span>
<span data-ttu-id="2d637-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d637-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d637-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d637-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d637-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d637-154">-DefaultProfile</span></span>
<span data-ttu-id="2d637-155">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d637-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d637-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d637-156">CommonParameters</span></span>
<span data-ttu-id="2d637-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d637-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d637-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d637-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d637-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d637-159">INPUTS</span></span>

### <span data-ttu-id="2d637-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="2d637-160">PSProfile</span></span>
<span data-ttu-id="2d637-161">Параметр "CdnProfile" принимает значение типа "PSProfile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="2d637-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="2d637-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d637-162">OUTPUTS</span></span>

### <span data-ttu-id="2d637-163">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d637-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="2d637-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d637-164">NOTES</span></span>

## <span data-ttu-id="2d637-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d637-165">RELATED LINKS</span></span>

[<span data-ttu-id="2d637-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d637-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="2d637-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d637-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="2d637-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d637-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="2d637-169">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d637-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="2d637-170">Остановить-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d637-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


