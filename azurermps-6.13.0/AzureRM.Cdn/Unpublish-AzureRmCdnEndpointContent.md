---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/unpublish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 15ab6c6974924458e6a206dac3d3629f3f4c48a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733469"
---
# <span data-ttu-id="59fd0-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="59fd0-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="59fd0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="59fd0-103">Очистка конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="59fd0-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59fd0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59fd0-104">SYNTAX</span></span>

### <span data-ttu-id="59fd0-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59fd0-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59fd0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59fd0-106">ByObjectParameterSet</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59fd0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59fd0-107">DESCRIPTION</span></span>
<span data-ttu-id="59fd0-108">Командлет **UNPUBLISH-AzureRmCdnEndpointContent** удаляет содержимое из конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="59fd0-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="59fd0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59fd0-109">EXAMPLES</span></span>

## <span data-ttu-id="59fd0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59fd0-110">PARAMETERS</span></span>

### <span data-ttu-id="59fd0-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="59fd0-111">-CdnEndpoint</span></span>
<span data-ttu-id="59fd0-112">Задает конечную точку, из которой удаляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="59fd0-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="59fd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fd0-113">-DefaultProfile</span></span>
<span data-ttu-id="59fd0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="59fd0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59fd0-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="59fd0-115">-EndpointName</span></span>
<span data-ttu-id="59fd0-116">Указывает имя конечной точки, очищенной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="59fd0-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="59fd0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59fd0-117">-PassThru</span></span>
<span data-ttu-id="59fd0-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="59fd0-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="59fd0-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="59fd0-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59fd0-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="59fd0-120">-ProfileName</span></span>
<span data-ttu-id="59fd0-121">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="59fd0-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="59fd0-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="59fd0-122">-PurgeContent</span></span>
<span data-ttu-id="59fd0-123">Задает массив относительных путей для содержимого на исходном сервере, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="59fd0-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="59fd0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59fd0-124">-ResourceGroupName</span></span>
<span data-ttu-id="59fd0-125">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="59fd0-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="59fd0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59fd0-126">-Confirm</span></span>
<span data-ttu-id="59fd0-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="59fd0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59fd0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59fd0-128">-WhatIf</span></span>
<span data-ttu-id="59fd0-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="59fd0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59fd0-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="59fd0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59fd0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fd0-131">CommonParameters</span></span>
<span data-ttu-id="59fd0-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59fd0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fd0-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59fd0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fd0-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59fd0-134">INPUTS</span></span>

### <span data-ttu-id="59fd0-135">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="59fd0-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="59fd0-136">Параметры: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="59fd0-136">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="59fd0-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="59fd0-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="59fd0-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59fd0-138">OUTPUTS</span></span>

### <span data-ttu-id="59fd0-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59fd0-139">System.Boolean</span></span>

## <span data-ttu-id="59fd0-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="59fd0-140">NOTES</span></span>

## <span data-ttu-id="59fd0-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59fd0-141">RELATED LINKS</span></span>

[<span data-ttu-id="59fd0-142">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="59fd0-142">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)


