---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 780765ea56cd13ee7cbd09b64dc20db896234aec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519696"
---
# <span data-ttu-id="391f8-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="391f8-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="391f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="391f8-102">SYNOPSIS</span></span>
<span data-ttu-id="391f8-103">Удаляет конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="391f8-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="391f8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="391f8-104">SYNTAX</span></span>

### <span data-ttu-id="391f8-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="391f8-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="391f8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="391f8-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="391f8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="391f8-107">DESCRIPTION</span></span>
<span data-ttu-id="391f8-108">При **этом удаляется** конечная точка сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="391f8-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="391f8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="391f8-109">EXAMPLES</span></span>

## <span data-ttu-id="391f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="391f8-110">PARAMETERS</span></span>

### <span data-ttu-id="391f8-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="391f8-111">-CdnEndpoint</span></span>
<span data-ttu-id="391f8-112">Указывает конечную точку, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="391f8-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="391f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="391f8-113">-DefaultProfile</span></span>
<span data-ttu-id="391f8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="391f8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="391f8-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="391f8-115">-EndpointName</span></span>
<span data-ttu-id="391f8-116">Указывает имя конечной точки, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="391f8-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="391f8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="391f8-117">-Force</span></span>
<span data-ttu-id="391f8-118">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="391f8-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391f8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="391f8-119">-PassThru</span></span>
<span data-ttu-id="391f8-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="391f8-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="391f8-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="391f8-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="391f8-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="391f8-122">-ProfileName</span></span>
<span data-ttu-id="391f8-123">Имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="391f8-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="391f8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="391f8-124">-ResourceGroupName</span></span>
<span data-ttu-id="391f8-125">Имя группы ресурсов, к которой относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="391f8-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="391f8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="391f8-126">-Confirm</span></span>
<span data-ttu-id="391f8-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="391f8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="391f8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="391f8-128">-WhatIf</span></span>
<span data-ttu-id="391f8-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="391f8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="391f8-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="391f8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="391f8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="391f8-131">CommonParameters</span></span>
<span data-ttu-id="391f8-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="391f8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="391f8-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="391f8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="391f8-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="391f8-134">INPUTS</span></span>

### <span data-ttu-id="391f8-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="391f8-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="391f8-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="391f8-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="391f8-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="391f8-137">OUTPUTS</span></span>

### <span data-ttu-id="391f8-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="391f8-138">System.Boolean</span></span>

## <span data-ttu-id="391f8-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="391f8-139">NOTES</span></span>

## <span data-ttu-id="391f8-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="391f8-140">RELATED LINKS</span></span>

[<span data-ttu-id="391f8-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="391f8-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="391f8-142">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="391f8-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="391f8-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="391f8-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="391f8-144">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="391f8-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="391f8-145">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="391f8-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


