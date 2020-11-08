---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246265"
---
# <span data-ttu-id="93d43-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="93d43-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="93d43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93d43-102">SYNOPSIS</span></span>
<span data-ttu-id="93d43-103">Создание нового источника сети CDN</span><span class="sxs-lookup"><span data-stu-id="93d43-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="93d43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93d43-104">SYNTAX</span></span>

### <span data-ttu-id="93d43-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="93d43-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93d43-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="93d43-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93d43-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93d43-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93d43-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93d43-108">DESCRIPTION</span></span>
<span data-ttu-id="93d43-109">New-AzCdnOrigin создаст новый источник CDN в пределах указанной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="93d43-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="93d43-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93d43-110">EXAMPLES</span></span>

### <span data-ttu-id="93d43-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="93d43-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="93d43-112">Этот командлет создаст новый источник CDN для указанной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="93d43-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="93d43-113">Он будет использовать предоставленное имя узла в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="93d43-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="93d43-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93d43-114">PARAMETERS</span></span>

### <span data-ttu-id="93d43-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="93d43-115">-CdnOrigin</span></span>
<span data-ttu-id="93d43-116">Объект источника CDN.</span><span class="sxs-lookup"><span data-stu-id="93d43-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="93d43-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d43-117">-DefaultProfile</span></span>
<span data-ttu-id="93d43-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93d43-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93d43-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="93d43-119">-EndpointName</span></span>
<span data-ttu-id="93d43-120">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="93d43-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="93d43-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="93d43-121">-HostName</span></span>
<span data-ttu-id="93d43-122">Имя узла источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="93d43-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="93d43-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="93d43-123">-HttpPort</span></span>
<span data-ttu-id="93d43-124">HTTP-порт источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="93d43-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="93d43-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="93d43-125">-HttpsPort</span></span>
<span data-ttu-id="93d43-126">HTTPS порт источника Azure.</span><span class="sxs-lookup"><span data-stu-id="93d43-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="93d43-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="93d43-127">-OriginHostHeader</span></span>
<span data-ttu-id="93d43-128">Заголовок узла источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="93d43-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="93d43-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="93d43-129">-OriginName</span></span>
<span data-ttu-id="93d43-130">Имя источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="93d43-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="93d43-131">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="93d43-131">-Priority</span></span>
<span data-ttu-id="93d43-132">Приоритет источника для Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="93d43-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="93d43-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="93d43-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="93d43-134">Настраиваемое сообщение, которое должно быть включено в запрос на утверждение для подключения к частной ссылке.</span><span class="sxs-lookup"><span data-stu-id="93d43-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="93d43-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="93d43-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="93d43-136">Расположение частной ссылки источника CDN в Azure.</span><span class="sxs-lookup"><span data-stu-id="93d43-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="93d43-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="93d43-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="93d43-138">Идентификатор ресурса частной ссылки источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="93d43-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="93d43-139">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="93d43-139">-ProfileName</span></span>
<span data-ttu-id="93d43-140">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="93d43-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="93d43-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93d43-141">-ResourceGroupName</span></span>
<span data-ttu-id="93d43-142">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="93d43-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="93d43-143">-Weight</span><span class="sxs-lookup"><span data-stu-id="93d43-143">-Weight</span></span>
<span data-ttu-id="93d43-144">Вес источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="93d43-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="93d43-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93d43-145">-Confirm</span></span>
<span data-ttu-id="93d43-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="93d43-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93d43-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93d43-147">-WhatIf</span></span>
<span data-ttu-id="93d43-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="93d43-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93d43-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="93d43-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93d43-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d43-150">CommonParameters</span></span>
<span data-ttu-id="93d43-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93d43-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d43-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93d43-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d43-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93d43-153">INPUTS</span></span>

### <span data-ttu-id="93d43-154">Ничего</span><span class="sxs-lookup"><span data-stu-id="93d43-154">None</span></span>

## <span data-ttu-id="93d43-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93d43-155">OUTPUTS</span></span>

### <span data-ttu-id="93d43-156">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="93d43-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="93d43-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="93d43-157">NOTES</span></span>

## <span data-ttu-id="93d43-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93d43-158">RELATED LINKS</span></span>
