---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 780765ea56cd13ee7cbd09b64dc20db896234aec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249097"
---
# <span data-ttu-id="2dc50-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc50-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="2dc50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2dc50-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc50-103">Удаляет конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="2dc50-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="2dc50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2dc50-104">SYNTAX</span></span>

### <span data-ttu-id="2dc50-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dc50-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dc50-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dc50-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dc50-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dc50-107">DESCRIPTION</span></span>
<span data-ttu-id="2dc50-108">Командлет **Remove-AzCdnEndpoint** удаляет конечную точку сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="2dc50-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2dc50-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2dc50-109">EXAMPLES</span></span>

## <span data-ttu-id="2dc50-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2dc50-110">PARAMETERS</span></span>

### <span data-ttu-id="2dc50-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc50-111">-CdnEndpoint</span></span>
<span data-ttu-id="2dc50-112">Указывает конечную точку, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2dc50-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2dc50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc50-113">-DefaultProfile</span></span>
<span data-ttu-id="2dc50-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2dc50-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dc50-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2dc50-115">-EndpointName</span></span>
<span data-ttu-id="2dc50-116">Указывает имя конечной точки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2dc50-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2dc50-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2dc50-117">-Force</span></span>
<span data-ttu-id="2dc50-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2dc50-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2dc50-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dc50-119">-PassThru</span></span>
<span data-ttu-id="2dc50-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2dc50-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2dc50-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2dc50-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2dc50-122">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="2dc50-122">-ProfileName</span></span>
<span data-ttu-id="2dc50-123">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="2dc50-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="2dc50-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dc50-124">-ResourceGroupName</span></span>
<span data-ttu-id="2dc50-125">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="2dc50-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="2dc50-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2dc50-126">-Confirm</span></span>
<span data-ttu-id="2dc50-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2dc50-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dc50-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dc50-128">-WhatIf</span></span>
<span data-ttu-id="2dc50-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2dc50-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dc50-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2dc50-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dc50-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc50-131">CommonParameters</span></span>
<span data-ttu-id="2dc50-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2dc50-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc50-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dc50-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc50-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2dc50-134">INPUTS</span></span>

### <span data-ttu-id="2dc50-135">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc50-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="2dc50-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2dc50-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2dc50-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dc50-137">OUTPUTS</span></span>

### <span data-ttu-id="2dc50-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2dc50-138">System.Boolean</span></span>

## <span data-ttu-id="2dc50-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="2dc50-139">NOTES</span></span>

## <span data-ttu-id="2dc50-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dc50-140">RELATED LINKS</span></span>

[<span data-ttu-id="2dc50-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc50-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="2dc50-142">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc50-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="2dc50-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc50-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="2dc50-144">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc50-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="2dc50-145">Остановить-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dc50-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


