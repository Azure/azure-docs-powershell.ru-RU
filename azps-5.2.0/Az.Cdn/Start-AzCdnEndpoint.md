---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403796"
---
# <span data-ttu-id="92e6c-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="92e6c-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="92e6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="92e6c-103">Запускает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="92e6c-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="92e6c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92e6c-104">SYNTAX</span></span>

### <span data-ttu-id="92e6c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92e6c-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92e6c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e6c-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92e6c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92e6c-107">DESCRIPTION</span></span>
<span data-ttu-id="92e6c-108">Для запуска конечной точки сети доставки содержимого (CDN) Azure запускается конечная точка **Start-AzCdnEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="92e6c-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="92e6c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92e6c-109">EXAMPLES</span></span>

## <span data-ttu-id="92e6c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92e6c-110">PARAMETERS</span></span>

### <span data-ttu-id="92e6c-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="92e6c-111">-CdnEndpoint</span></span>
<span data-ttu-id="92e6c-112">Указывает конечную точку, с которую запускается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92e6c-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="92e6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e6c-113">-DefaultProfile</span></span>
<span data-ttu-id="92e6c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="92e6c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92e6c-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="92e6c-115">-EndpointName</span></span>
<span data-ttu-id="92e6c-116">Указывает имя конечной точки, с которую запускается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92e6c-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="92e6c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92e6c-117">-PassThru</span></span>
<span data-ttu-id="92e6c-118">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="92e6c-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="92e6c-119">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="92e6c-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="92e6c-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="92e6c-120">-ProfileName</span></span>
<span data-ttu-id="92e6c-121">Имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="92e6c-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="92e6c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e6c-122">-ResourceGroupName</span></span>
<span data-ttu-id="92e6c-123">Имя группы ресурсов, к которой относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="92e6c-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="92e6c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92e6c-124">-Confirm</span></span>
<span data-ttu-id="92e6c-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="92e6c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92e6c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92e6c-126">-WhatIf</span></span>
<span data-ttu-id="92e6c-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92e6c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92e6c-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="92e6c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92e6c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e6c-129">CommonParameters</span></span>
<span data-ttu-id="92e6c-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e6c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e6c-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92e6c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e6c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92e6c-132">INPUTS</span></span>

### <span data-ttu-id="92e6c-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="92e6c-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="92e6c-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="92e6c-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="92e6c-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92e6c-135">OUTPUTS</span></span>

### <span data-ttu-id="92e6c-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92e6c-136">System.Boolean</span></span>

## <span data-ttu-id="92e6c-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92e6c-137">NOTES</span></span>

## <span data-ttu-id="92e6c-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92e6c-138">RELATED LINKS</span></span>

[<span data-ttu-id="92e6c-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="92e6c-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="92e6c-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="92e6c-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="92e6c-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="92e6c-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="92e6c-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="92e6c-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="92e6c-143">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="92e6c-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


