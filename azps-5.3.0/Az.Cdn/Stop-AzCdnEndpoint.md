---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: e1afa87d1ab21222987a4eeecf68a3786934ef57
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509333"
---
# <span data-ttu-id="b54f3-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b54f3-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="b54f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b54f3-102">SYNOPSIS</span></span>
<span data-ttu-id="b54f3-103">Остановка конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="b54f3-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="b54f3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b54f3-104">SYNTAX</span></span>

### <span data-ttu-id="b54f3-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b54f3-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b54f3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b54f3-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b54f3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b54f3-107">DESCRIPTION</span></span>
<span data-ttu-id="b54f3-108">Для остановки конечной точки сети доставки содержимого (CDN) Azure будет выбрана конечная точка **Stop-AzCdnEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="b54f3-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b54f3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b54f3-109">EXAMPLES</span></span>

## <span data-ttu-id="b54f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b54f3-110">PARAMETERS</span></span>

### <span data-ttu-id="b54f3-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b54f3-111">-CdnEndpoint</span></span>
<span data-ttu-id="b54f3-112">Определяет объект конечной точки, который останавливает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b54f3-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b54f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b54f3-113">-DefaultProfile</span></span>
<span data-ttu-id="b54f3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b54f3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b54f3-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b54f3-115">-EndpointName</span></span>
<span data-ttu-id="b54f3-116">Указывает имя конечной точки, которая останавливается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b54f3-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b54f3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b54f3-117">-PassThru</span></span>
<span data-ttu-id="b54f3-118">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b54f3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b54f3-119">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b54f3-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b54f3-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b54f3-120">-ProfileName</span></span>
<span data-ttu-id="b54f3-121">Имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="b54f3-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b54f3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b54f3-122">-ResourceGroupName</span></span>
<span data-ttu-id="b54f3-123">Имя группы ресурсов, к которой относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="b54f3-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b54f3-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b54f3-124">-Confirm</span></span>
<span data-ttu-id="b54f3-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b54f3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b54f3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b54f3-126">-WhatIf</span></span>
<span data-ttu-id="b54f3-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b54f3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b54f3-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b54f3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b54f3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b54f3-129">CommonParameters</span></span>
<span data-ttu-id="b54f3-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b54f3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b54f3-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b54f3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b54f3-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b54f3-132">INPUTS</span></span>

### <span data-ttu-id="b54f3-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b54f3-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="b54f3-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b54f3-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b54f3-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b54f3-135">OUTPUTS</span></span>

### <span data-ttu-id="b54f3-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b54f3-136">System.Boolean</span></span>

## <span data-ttu-id="b54f3-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b54f3-137">NOTES</span></span>

## <span data-ttu-id="b54f3-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b54f3-138">RELATED LINKS</span></span>

[<span data-ttu-id="b54f3-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b54f3-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="b54f3-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b54f3-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="b54f3-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b54f3-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="b54f3-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b54f3-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="b54f3-143">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b54f3-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


