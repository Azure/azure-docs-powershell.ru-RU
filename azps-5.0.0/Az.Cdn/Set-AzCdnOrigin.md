---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247644"
---
# <span data-ttu-id="c5411-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="c5411-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="c5411-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5411-102">SYNOPSIS</span></span>
<span data-ttu-id="c5411-103">Обновляет сервер источника CDN.</span><span class="sxs-lookup"><span data-stu-id="c5411-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="c5411-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5411-104">SYNTAX</span></span>

### <span data-ttu-id="c5411-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c5411-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5411-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5411-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5411-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5411-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5411-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5411-108">DESCRIPTION</span></span>
<span data-ttu-id="c5411-109">Командлет **Set-AzCdnOrigin** обновляет сервер происхождения сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="c5411-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="c5411-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5411-110">EXAMPLES</span></span>

## <span data-ttu-id="c5411-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5411-111">PARAMETERS</span></span>

### <span data-ttu-id="c5411-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="c5411-112">-CdnOrigin</span></span>
<span data-ttu-id="c5411-113">Указывает исходный сервер, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c5411-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="c5411-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5411-114">-DefaultProfile</span></span>
<span data-ttu-id="c5411-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c5411-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5411-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c5411-116">-EndpointName</span></span>
<span data-ttu-id="c5411-117">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="c5411-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="c5411-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="c5411-118">-HostName</span></span>
<span data-ttu-id="c5411-119">Имя узла источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="c5411-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="c5411-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="c5411-120">-HttpPort</span></span>
<span data-ttu-id="c5411-121">HTTP-порт источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c5411-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="c5411-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="c5411-122">-HttpsPort</span></span>
<span data-ttu-id="c5411-123">HTTPS порт источника Azure.</span><span class="sxs-lookup"><span data-stu-id="c5411-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="c5411-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="c5411-124">-OriginHostHeader</span></span>
<span data-ttu-id="c5411-125">Заголовок узла источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="c5411-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="c5411-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="c5411-126">-OriginName</span></span>
<span data-ttu-id="c5411-127">Имя источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c5411-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="c5411-128">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="c5411-128">-Priority</span></span>
<span data-ttu-id="c5411-129">Приоритет источника для Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c5411-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="c5411-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="c5411-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="c5411-131">Настраиваемое сообщение, которое должно быть включено в запрос на утверждение для подключения к частной ссылке.</span><span class="sxs-lookup"><span data-stu-id="c5411-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="c5411-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="c5411-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="c5411-133">Расположение частной ссылки источника CDN в Azure.</span><span class="sxs-lookup"><span data-stu-id="c5411-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="c5411-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="c5411-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="c5411-135">Идентификатор ресурса частной ссылки источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="c5411-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="c5411-136">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="c5411-136">-ProfileName</span></span>
<span data-ttu-id="c5411-137">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="c5411-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="c5411-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5411-138">-ResourceGroupName</span></span>
<span data-ttu-id="c5411-139">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="c5411-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="c5411-140">-Weight</span><span class="sxs-lookup"><span data-stu-id="c5411-140">-Weight</span></span>
<span data-ttu-id="c5411-141">Вес источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="c5411-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="c5411-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5411-142">-Confirm</span></span>
<span data-ttu-id="c5411-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c5411-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5411-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5411-144">-WhatIf</span></span>
<span data-ttu-id="c5411-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c5411-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5411-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c5411-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5411-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5411-147">CommonParameters</span></span>
<span data-ttu-id="c5411-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5411-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5411-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5411-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5411-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5411-150">INPUTS</span></span>

### <span data-ttu-id="c5411-151">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="c5411-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="c5411-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5411-152">OUTPUTS</span></span>

### <span data-ttu-id="c5411-153">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="c5411-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="c5411-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5411-154">NOTES</span></span>

## <span data-ttu-id="c5411-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5411-155">RELATED LINKS</span></span>

[<span data-ttu-id="c5411-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="c5411-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


