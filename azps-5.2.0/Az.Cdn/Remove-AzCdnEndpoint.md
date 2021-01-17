---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 780765ea56cd13ee7cbd09b64dc20db896234aec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404812"
---
# <span data-ttu-id="b4b4d-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4b4d-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="b4b4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b4d-103">Удаляет конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="b4b4d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4b4d-104">SYNTAX</span></span>

### <span data-ttu-id="b4b4d-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4b4d-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4b4d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4b4d-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4b4d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4b4d-107">DESCRIPTION</span></span>
<span data-ttu-id="b4b4d-108">При **этом удаляется** конечная точка сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b4b4d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4b4d-109">EXAMPLES</span></span>

## <span data-ttu-id="b4b4d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4b4d-110">PARAMETERS</span></span>

### <span data-ttu-id="b4b4d-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4b4d-111">-CdnEndpoint</span></span>
<span data-ttu-id="b4b4d-112">Указывает конечную точку, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b4b4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b4d-113">-DefaultProfile</span></span>
<span data-ttu-id="b4b4d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b4b4d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4b4d-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b4b4d-115">-EndpointName</span></span>
<span data-ttu-id="b4b4d-116">Указывает имя конечной точки, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b4b4d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b4b4d-117">-Force</span></span>
<span data-ttu-id="b4b4d-118">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4b4d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4b4d-119">-PassThru</span></span>
<span data-ttu-id="b4b4d-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b4b4d-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4b4d-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b4b4d-122">-ProfileName</span></span>
<span data-ttu-id="b4b4d-123">Имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b4b4d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4b4d-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4b4d-125">Имя группы ресурсов, к которой относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b4b4d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4b4d-126">-Confirm</span></span>
<span data-ttu-id="b4b4d-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b4d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b4d-128">-WhatIf</span></span>
<span data-ttu-id="b4b4d-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4b4d-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b4d-131">CommonParameters</span></span>
<span data-ttu-id="b4b4d-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b4d-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4b4d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b4d-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4b4d-134">INPUTS</span></span>

### <span data-ttu-id="b4b4d-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4b4d-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="b4b4d-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b4b4d-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b4b4d-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4b4d-137">OUTPUTS</span></span>

### <span data-ttu-id="b4b4d-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4b4d-138">System.Boolean</span></span>

## <span data-ttu-id="b4b4d-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4b4d-139">NOTES</span></span>

## <span data-ttu-id="b4b4d-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4b4d-140">RELATED LINKS</span></span>

[<span data-ttu-id="b4b4d-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4b4d-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="b4b4d-142">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4b4d-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="b4b4d-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4b4d-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="b4b4d-144">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4b4d-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="b4b4d-145">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4b4d-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


