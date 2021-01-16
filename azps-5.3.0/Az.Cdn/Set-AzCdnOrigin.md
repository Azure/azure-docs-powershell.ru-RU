---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509341"
---
# <span data-ttu-id="bb6a8-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="bb6a8-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="bb6a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6a8-103">Обновляет сервер источника CDN.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="bb6a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bb6a8-104">SYNTAX</span></span>

### <span data-ttu-id="bb6a8-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb6a8-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb6a8-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb6a8-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb6a8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb6a8-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb6a8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb6a8-108">DESCRIPTION</span></span>
<span data-ttu-id="bb6a8-109">Для обновления источника источник данных сети доставки содержимого (CDN) Azure обновляется клиент **Set-AzCdnOrigin.**</span><span class="sxs-lookup"><span data-stu-id="bb6a8-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="bb6a8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bb6a8-110">EXAMPLES</span></span>

## <span data-ttu-id="bb6a8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb6a8-111">PARAMETERS</span></span>

### <span data-ttu-id="bb6a8-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="bb6a8-112">-CdnOrigin</span></span>
<span data-ttu-id="bb6a8-113">Определяет сервер источника, который обновляется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="bb6a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6a8-114">-DefaultProfile</span></span>
<span data-ttu-id="bb6a8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bb6a8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb6a8-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bb6a8-116">-EndpointName</span></span>
<span data-ttu-id="bb6a8-117">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="bb6a8-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="bb6a8-118">-HostName</span></span>
<span data-ttu-id="bb6a8-119">Имя хоста в источнике CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="bb6a8-120">-httpPort</span><span class="sxs-lookup"><span data-stu-id="bb6a8-120">-HttpPort</span></span>
<span data-ttu-id="bb6a8-121">Источник CDN Azure http.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="bb6a8-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="bb6a8-122">-HttpsPort</span></span>
<span data-ttu-id="bb6a8-123">Источник CDN Azure https.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="bb6a8-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="bb6a8-124">-OriginHostHeader</span></span>
<span data-ttu-id="bb6a8-125">Задав источник хоста Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="bb6a8-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="bb6a8-126">-OriginName</span></span>
<span data-ttu-id="bb6a8-127">Имя источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="bb6a8-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="bb6a8-128">-Priority</span></span>
<span data-ttu-id="bb6a8-129">Приоритет источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="bb6a8-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="bb6a8-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="bb6a8-131">Пользовательское сообщение, которое будет включено в запрос на утверждение для подключения к личной ссылке.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="bb6a8-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="bb6a8-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="bb6a8-133">Расположение закрытой ссылки в источнике Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="bb6a8-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="bb6a8-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="bb6a8-135">Azure CDN origin private link resource id.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="bb6a8-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bb6a8-136">-ProfileName</span></span>
<span data-ttu-id="bb6a8-137">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="bb6a8-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb6a8-138">-ResourceGroupName</span></span>
<span data-ttu-id="bb6a8-139">Группа ресурсов профиля AZURE CDN.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="bb6a8-140">-Weight</span><span class="sxs-lookup"><span data-stu-id="bb6a8-140">-Weight</span></span>
<span data-ttu-id="bb6a8-141">Вес источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="bb6a8-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb6a8-142">-Confirm</span></span>
<span data-ttu-id="bb6a8-143">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb6a8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb6a8-144">-WhatIf</span></span>
<span data-ttu-id="bb6a8-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb6a8-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb6a8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6a8-147">CommonParameters</span></span>
<span data-ttu-id="bb6a8-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb6a8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6a8-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb6a8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6a8-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb6a8-150">INPUTS</span></span>

### <span data-ttu-id="bb6a8-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="bb6a8-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="bb6a8-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bb6a8-152">OUTPUTS</span></span>

### <span data-ttu-id="bb6a8-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="bb6a8-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="bb6a8-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bb6a8-154">NOTES</span></span>

## <span data-ttu-id="bb6a8-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb6a8-155">RELATED LINKS</span></span>

[<span data-ttu-id="bb6a8-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="bb6a8-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


