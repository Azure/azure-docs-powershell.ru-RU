---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: cc7350fb76091d3bf2f8bdab5c037a5afbe8b57a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983416"
---
# <span data-ttu-id="e73c0-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e73c0-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="e73c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e73c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e73c0-103">Создание источника CDN</span><span class="sxs-lookup"><span data-stu-id="e73c0-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="e73c0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e73c0-104">SYNTAX</span></span>

### <span data-ttu-id="e73c0-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e73c0-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e73c0-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="e73c0-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e73c0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e73c0-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e73c0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e73c0-108">DESCRIPTION</span></span>
<span data-ttu-id="e73c0-109">После New-AzCdnOrigin будет создаваться новый источник CDN в пределах указанной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="e73c0-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="e73c0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e73c0-110">EXAMPLES</span></span>

### <span data-ttu-id="e73c0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e73c0-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="e73c0-112">Этот cmdlet создаст новый источник CDN для указанной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="e73c0-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="e73c0-113">В качестве источника будет использовать предоставленное имя хознаб.</span><span class="sxs-lookup"><span data-stu-id="e73c0-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="e73c0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e73c0-114">PARAMETERS</span></span>

### <span data-ttu-id="e73c0-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e73c0-115">-CdnOrigin</span></span>
<span data-ttu-id="e73c0-116">Источник CDN.</span><span class="sxs-lookup"><span data-stu-id="e73c0-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e73c0-117">-DefaultProfile</span></span>
<span data-ttu-id="e73c0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e73c0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e73c0-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e73c0-119">-EndpointName</span></span>
<span data-ttu-id="e73c0-120">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="e73c0-120">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="e73c0-121">-HostName</span></span>
<span data-ttu-id="e73c0-122">Имя хоста в источнике CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="e73c0-122">Azure CDN origin host name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-123">-httpPort</span><span class="sxs-lookup"><span data-stu-id="e73c0-123">-HttpPort</span></span>
<span data-ttu-id="e73c0-124">Источник CDN Azure http.</span><span class="sxs-lookup"><span data-stu-id="e73c0-124">Azure CDN origin http port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="e73c0-125">-HttpsPort</span></span>
<span data-ttu-id="e73c0-126">Источник CDN Azure https.</span><span class="sxs-lookup"><span data-stu-id="e73c0-126">Azure CDN origin https port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="e73c0-127">-OriginHostHeader</span></span>
<span data-ttu-id="e73c0-128">Задав источник хоста Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e73c0-128">Azure CDN origin host header.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="e73c0-129">-OriginName</span></span>
<span data-ttu-id="e73c0-130">Название источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="e73c0-130">Azure CDN origin name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="e73c0-131">-Priority</span></span>
<span data-ttu-id="e73c0-132">Приоритет источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="e73c0-132">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="e73c0-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="e73c0-134">Пользовательское сообщение, которое будет включено в запрос на утверждение для подключения к личной ссылке.</span><span class="sxs-lookup"><span data-stu-id="e73c0-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="e73c0-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="e73c0-136">Расположение закрытой ссылки в источнике Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e73c0-136">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="e73c0-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="e73c0-138">Azure CDN origin private link resource id.</span><span class="sxs-lookup"><span data-stu-id="e73c0-138">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e73c0-139">-ProfileName</span></span>
<span data-ttu-id="e73c0-140">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="e73c0-140">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e73c0-141">-ResourceGroupName</span></span>
<span data-ttu-id="e73c0-142">Группа ресурсов профиля Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="e73c0-142">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-143">-Weight</span><span class="sxs-lookup"><span data-stu-id="e73c0-143">-Weight</span></span>
<span data-ttu-id="e73c0-144">Вес источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="e73c0-144">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e73c0-145">-Confirm</span></span>
<span data-ttu-id="e73c0-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e73c0-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e73c0-147">-WhatIf</span></span>
<span data-ttu-id="e73c0-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e73c0-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e73c0-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e73c0-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e73c0-150">CommonParameters</span></span>
<span data-ttu-id="e73c0-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e73c0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e73c0-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e73c0-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e73c0-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e73c0-153">INPUTS</span></span>

### <span data-ttu-id="e73c0-154">Нет</span><span class="sxs-lookup"><span data-stu-id="e73c0-154">None</span></span>

## <span data-ttu-id="e73c0-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e73c0-155">OUTPUTS</span></span>

### <span data-ttu-id="e73c0-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="e73c0-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="e73c0-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e73c0-157">NOTES</span></span>

## <span data-ttu-id="e73c0-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e73c0-158">RELATED LINKS</span></span>
