---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236238"
---
# <span data-ttu-id="5c47a-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c47a-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="5c47a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c47a-102">SYNOPSIS</span></span>
<span data-ttu-id="5c47a-103">Запускает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="5c47a-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="5c47a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c47a-104">SYNTAX</span></span>

### <span data-ttu-id="5c47a-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c47a-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c47a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c47a-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c47a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c47a-107">DESCRIPTION</span></span>
<span data-ttu-id="5c47a-108">Командлет **Start-AzCdnEndpoint** запускает конечную точку сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="5c47a-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="5c47a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c47a-109">EXAMPLES</span></span>

## <span data-ttu-id="5c47a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c47a-110">PARAMETERS</span></span>

### <span data-ttu-id="5c47a-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c47a-111">-CdnEndpoint</span></span>
<span data-ttu-id="5c47a-112">Задает конечную точку, которую запускает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5c47a-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="5c47a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c47a-113">-DefaultProfile</span></span>
<span data-ttu-id="5c47a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5c47a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c47a-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5c47a-115">-EndpointName</span></span>
<span data-ttu-id="5c47a-116">Указывает имя конечной точки, с которой начинается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5c47a-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="5c47a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c47a-117">-PassThru</span></span>
<span data-ttu-id="5c47a-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5c47a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5c47a-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5c47a-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5c47a-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="5c47a-120">-ProfileName</span></span>
<span data-ttu-id="5c47a-121">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="5c47a-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="5c47a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c47a-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c47a-123">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="5c47a-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="5c47a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c47a-124">-Confirm</span></span>
<span data-ttu-id="5c47a-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5c47a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c47a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c47a-126">-WhatIf</span></span>
<span data-ttu-id="5c47a-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5c47a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c47a-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5c47a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c47a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c47a-129">CommonParameters</span></span>
<span data-ttu-id="5c47a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c47a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c47a-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c47a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c47a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c47a-132">INPUTS</span></span>

### <span data-ttu-id="5c47a-133">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c47a-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="5c47a-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5c47a-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5c47a-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c47a-135">OUTPUTS</span></span>

### <span data-ttu-id="5c47a-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c47a-136">System.Boolean</span></span>

## <span data-ttu-id="5c47a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c47a-137">NOTES</span></span>

## <span data-ttu-id="5c47a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c47a-138">RELATED LINKS</span></span>

[<span data-ttu-id="5c47a-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c47a-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="5c47a-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c47a-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="5c47a-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c47a-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="5c47a-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c47a-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="5c47a-143">Остановить-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c47a-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


