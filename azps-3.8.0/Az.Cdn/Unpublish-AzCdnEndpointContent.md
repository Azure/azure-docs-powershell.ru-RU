---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: eb108e665bce54d2b94fc4ab4a56c9573248289a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064792"
---
# <span data-ttu-id="d0e7b-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="d0e7b-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="d0e7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e7b-103">Очистка конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="d0e7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0e7b-104">SYNTAX</span></span>

### <span data-ttu-id="d0e7b-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0e7b-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0e7b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0e7b-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0e7b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0e7b-107">DESCRIPTION</span></span>
<span data-ttu-id="d0e7b-108">Командлет **UNPUBLISH-AzCdnEndpointContent** удаляет содержимое из конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d0e7b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0e7b-109">EXAMPLES</span></span>

## <span data-ttu-id="d0e7b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0e7b-110">PARAMETERS</span></span>

### <span data-ttu-id="d0e7b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0e7b-111">-CdnEndpoint</span></span>
<span data-ttu-id="d0e7b-112">Задает конечную точку, из которой удаляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-112">Specifies the endpoint that this cmdlet purges.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e7b-113">-DefaultProfile</span></span>
<span data-ttu-id="d0e7b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d0e7b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0e7b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d0e7b-115">-EndpointName</span></span>
<span data-ttu-id="d0e7b-116">Указывает имя конечной точки, очищенной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="d0e7b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0e7b-117">-PassThru</span></span>
<span data-ttu-id="d0e7b-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d0e7b-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e7b-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="d0e7b-120">-ProfileName</span></span>
<span data-ttu-id="d0e7b-121">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d0e7b-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="d0e7b-122">-PurgeContent</span></span>
<span data-ttu-id="d0e7b-123">Задает массив относительных путей для содержимого на исходном сервере, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0e7b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0e7b-124">-ResourceGroupName</span></span>
<span data-ttu-id="d0e7b-125">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="d0e7b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0e7b-126">-Confirm</span></span>
<span data-ttu-id="d0e7b-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0e7b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0e7b-128">-WhatIf</span></span>
<span data-ttu-id="d0e7b-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0e7b-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0e7b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e7b-131">CommonParameters</span></span>
<span data-ttu-id="d0e7b-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0e7b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e7b-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0e7b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e7b-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0e7b-134">INPUTS</span></span>

### <span data-ttu-id="d0e7b-135">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0e7b-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="d0e7b-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d0e7b-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d0e7b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0e7b-137">OUTPUTS</span></span>

### <span data-ttu-id="d0e7b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0e7b-138">System.Boolean</span></span>

## <span data-ttu-id="d0e7b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0e7b-139">NOTES</span></span>

## <span data-ttu-id="d0e7b-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0e7b-140">RELATED LINKS</span></span>

[<span data-ttu-id="d0e7b-141">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="d0e7b-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


