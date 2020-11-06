---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 682c12270608f9c75e86cea742fd411e0eb657a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559248"
---
# <span data-ttu-id="91ec2-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="91ec2-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="91ec2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="91ec2-103">Создание конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="91ec2-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91ec2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91ec2-104">SYNTAX</span></span>

### <span data-ttu-id="91ec2-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="91ec2-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ec2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91ec2-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91ec2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91ec2-107">DESCRIPTION</span></span>
<span data-ttu-id="91ec2-108">Командлет **New-AzureRmCdnEndpoint** создает конечную точку сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="91ec2-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="91ec2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91ec2-109">EXAMPLES</span></span>

## <span data-ttu-id="91ec2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91ec2-110">PARAMETERS</span></span>

### <span data-ttu-id="91ec2-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="91ec2-111">-CdnProfile</span></span>
<span data-ttu-id="91ec2-112">Указывает объект профиля CDN, в который добавляется конечная точка.</span><span class="sxs-lookup"><span data-stu-id="91ec2-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="91ec2-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="91ec2-114">Задает массив типов контента для сжатия между узлом EDGE и клиентом.</span><span class="sxs-lookup"><span data-stu-id="91ec2-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ec2-115">-DefaultProfile</span></span>
<span data-ttu-id="91ec2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="91ec2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91ec2-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="91ec2-117">-EndpointName</span></span>
<span data-ttu-id="91ec2-118">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="91ec2-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="91ec2-119">-Геофильтры</span><span class="sxs-lookup"><span data-stu-id="91ec2-119">-GeoFilters</span></span>
<span data-ttu-id="91ec2-120">Список географических фильтров, которые применяются к этой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="91ec2-120">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="91ec2-121">-HttpPort</span></span>
<span data-ttu-id="91ec2-122">Указывает номер HTTP-порта на исходном сервере.</span><span class="sxs-lookup"><span data-stu-id="91ec2-122">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-123">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="91ec2-123">-HttpsPort</span></span>
<span data-ttu-id="91ec2-124">Задает номер HTTPS порта на исходном сервере.</span><span class="sxs-lookup"><span data-stu-id="91ec2-124">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-125">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="91ec2-125">-IsCompressionEnabled</span></span>
<span data-ttu-id="91ec2-126">Указывает, включено ли сжатие для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="91ec2-126">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-127">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="91ec2-127">-IsHttpAllowed</span></span>
<span data-ttu-id="91ec2-128">Указывает, включит ли конечную точку трафик HTTP.</span><span class="sxs-lookup"><span data-stu-id="91ec2-128">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-129">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="91ec2-129">-IsHttpsAllowed</span></span>
<span data-ttu-id="91ec2-130">Указывает, включит ли конечную точку трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="91ec2-130">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-131">-Location</span><span class="sxs-lookup"><span data-stu-id="91ec2-131">-Location</span></span>
<span data-ttu-id="91ec2-132">Указывает расположение ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="91ec2-132">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-133">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="91ec2-133">-OptimizationType</span></span>
<span data-ttu-id="91ec2-134">Указывает любую оптимизацию, указанную в этой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="91ec2-134">Specifies any optimization this endpoint has.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-135">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="91ec2-135">-OriginHostHeader</span></span>
<span data-ttu-id="91ec2-136">Задает заголовок исходного узла конечной точки.</span><span class="sxs-lookup"><span data-stu-id="91ec2-136">Specifies the origin host head of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-137">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="91ec2-137">-OriginHostName</span></span>
<span data-ttu-id="91ec2-138">Указывает имя узла исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="91ec2-138">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="91ec2-139">-OriginName</span><span class="sxs-lookup"><span data-stu-id="91ec2-139">-OriginName</span></span>
<span data-ttu-id="91ec2-140">Указывает имя ресурса исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="91ec2-140">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="91ec2-141">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="91ec2-141">-OriginPath</span></span>
<span data-ttu-id="91ec2-142">Указывает путь к исходному серверу.</span><span class="sxs-lookup"><span data-stu-id="91ec2-142">Specifies the path of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-143">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="91ec2-143">-ProfileName</span></span>
<span data-ttu-id="91ec2-144">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="91ec2-144">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-145">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="91ec2-145">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="91ec2-146">Задает поведение конечной точки CDN, если строка запроса находится в URL-адресе запроса.</span><span class="sxs-lookup"><span data-stu-id="91ec2-146">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: PSQueryStringCachingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91ec2-147">-ResourceGroupName</span></span>
<span data-ttu-id="91ec2-148">Указывает имя группы ресурсов, к которой принадлежит эта конечная точка.</span><span class="sxs-lookup"><span data-stu-id="91ec2-148">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-149">-Тег</span><span class="sxs-lookup"><span data-stu-id="91ec2-149">-Tag</span></span>
<span data-ttu-id="91ec2-150">Теги, связываемые с конечной точкой CDN в Azure.</span><span class="sxs-lookup"><span data-stu-id="91ec2-150">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91ec2-151">-Confirm</span></span>
<span data-ttu-id="91ec2-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="91ec2-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91ec2-153">-WhatIf</span></span>
<span data-ttu-id="91ec2-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="91ec2-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91ec2-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="91ec2-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ec2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ec2-156">CommonParameters</span></span>
<span data-ttu-id="91ec2-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91ec2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ec2-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91ec2-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ec2-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91ec2-159">INPUTS</span></span>

### <span data-ttu-id="91ec2-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="91ec2-160">PSProfile</span></span>
<span data-ttu-id="91ec2-161">Параметр "CdnProfile" принимает значение типа "PSProfile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="91ec2-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="91ec2-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91ec2-162">OUTPUTS</span></span>

### <span data-ttu-id="91ec2-163">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="91ec2-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="91ec2-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="91ec2-164">NOTES</span></span>

## <span data-ttu-id="91ec2-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91ec2-165">RELATED LINKS</span></span>

[<span data-ttu-id="91ec2-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="91ec2-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="91ec2-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="91ec2-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="91ec2-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="91ec2-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="91ec2-169">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="91ec2-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="91ec2-170">Остановить-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="91ec2-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


