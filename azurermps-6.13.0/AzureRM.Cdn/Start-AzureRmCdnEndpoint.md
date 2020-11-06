---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/start-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
ms.openlocfilehash: 4a6f7b86d16e5b82cf6bf9e869ed74f688fc5950
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565883"
---
# <span data-ttu-id="5ddcc-101">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ddcc-101">Start-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="5ddcc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ddcc-102">SYNOPSIS</span></span>
<span data-ttu-id="5ddcc-103">Запускает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="5ddcc-103">Starts a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ddcc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ddcc-104">SYNTAX</span></span>

### <span data-ttu-id="5ddcc-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ddcc-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ddcc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ddcc-106">ByObjectParameterSet</span></span>
```
Start-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ddcc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ddcc-107">DESCRIPTION</span></span>
<span data-ttu-id="5ddcc-108">Командлет **Start-AzureRmCdnEndpoint** запускает конечную точку сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="5ddcc-108">The **Start-AzureRmCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="5ddcc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ddcc-109">EXAMPLES</span></span>

## <span data-ttu-id="5ddcc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ddcc-110">PARAMETERS</span></span>

### <span data-ttu-id="5ddcc-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ddcc-111">-CdnEndpoint</span></span>
<span data-ttu-id="5ddcc-112">Задает конечную точку, которую запускает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5ddcc-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="5ddcc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ddcc-113">-DefaultProfile</span></span>
<span data-ttu-id="5ddcc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ddcc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ddcc-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5ddcc-115">-EndpointName</span></span>
<span data-ttu-id="5ddcc-116">Указывает имя конечной точки, с которой начинается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5ddcc-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="5ddcc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ddcc-117">-PassThru</span></span>
<span data-ttu-id="5ddcc-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5ddcc-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5ddcc-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5ddcc-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5ddcc-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="5ddcc-120">-ProfileName</span></span>
<span data-ttu-id="5ddcc-121">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="5ddcc-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="5ddcc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ddcc-122">-ResourceGroupName</span></span>
<span data-ttu-id="5ddcc-123">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="5ddcc-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="5ddcc-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ddcc-124">-Confirm</span></span>
<span data-ttu-id="5ddcc-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ddcc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ddcc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ddcc-126">-WhatIf</span></span>
<span data-ttu-id="5ddcc-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ddcc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ddcc-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ddcc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ddcc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ddcc-129">CommonParameters</span></span>
<span data-ttu-id="5ddcc-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ddcc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ddcc-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ddcc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ddcc-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ddcc-132">INPUTS</span></span>

### <span data-ttu-id="5ddcc-133">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ddcc-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="5ddcc-134">Параметры: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5ddcc-134">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="5ddcc-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5ddcc-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5ddcc-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ddcc-136">OUTPUTS</span></span>

### <span data-ttu-id="5ddcc-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ddcc-137">System.Boolean</span></span>

## <span data-ttu-id="5ddcc-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ddcc-138">NOTES</span></span>

## <span data-ttu-id="5ddcc-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ddcc-139">RELATED LINKS</span></span>

[<span data-ttu-id="5ddcc-140">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ddcc-140">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5ddcc-141">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ddcc-141">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5ddcc-142">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ddcc-142">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5ddcc-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ddcc-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5ddcc-144">Остановить-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ddcc-144">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


