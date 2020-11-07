---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: a606bbcb630ab4868e64221b9bcaa8f471327977
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901433"
---
# <span data-ttu-id="15a54-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a54-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="15a54-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15a54-102">SYNOPSIS</span></span>
<span data-ttu-id="15a54-103">Останавливает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="15a54-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="15a54-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15a54-104">SYNTAX</span></span>

### <span data-ttu-id="15a54-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15a54-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15a54-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15a54-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15a54-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15a54-107">DESCRIPTION</span></span>
<span data-ttu-id="15a54-108">Командлет **Stop-AzCdnEndpoint** останавливает конечную точку сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="15a54-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="15a54-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15a54-109">EXAMPLES</span></span>

## <span data-ttu-id="15a54-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15a54-110">PARAMETERS</span></span>

### <span data-ttu-id="15a54-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a54-111">-CdnEndpoint</span></span>
<span data-ttu-id="15a54-112">Указывает объект конечной точки, который останавливается для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="15a54-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="15a54-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a54-113">-DefaultProfile</span></span>
<span data-ttu-id="15a54-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="15a54-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15a54-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="15a54-115">-EndpointName</span></span>
<span data-ttu-id="15a54-116">Указывает имя конечной точки, которую завершает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="15a54-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="15a54-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15a54-117">-PassThru</span></span>
<span data-ttu-id="15a54-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="15a54-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="15a54-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="15a54-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="15a54-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="15a54-120">-ProfileName</span></span>
<span data-ttu-id="15a54-121">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="15a54-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="15a54-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a54-122">-ResourceGroupName</span></span>
<span data-ttu-id="15a54-123">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="15a54-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="15a54-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15a54-124">-Confirm</span></span>
<span data-ttu-id="15a54-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15a54-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a54-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a54-126">-WhatIf</span></span>
<span data-ttu-id="15a54-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15a54-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a54-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15a54-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a54-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a54-129">CommonParameters</span></span>
<span data-ttu-id="15a54-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15a54-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a54-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a54-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a54-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15a54-132">INPUTS</span></span>

### <span data-ttu-id="15a54-133">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a54-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="15a54-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="15a54-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="15a54-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15a54-135">OUTPUTS</span></span>

### <span data-ttu-id="15a54-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15a54-136">System.Boolean</span></span>

## <span data-ttu-id="15a54-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="15a54-137">NOTES</span></span>

## <span data-ttu-id="15a54-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15a54-138">RELATED LINKS</span></span>

[<span data-ttu-id="15a54-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a54-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="15a54-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a54-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="15a54-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a54-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="15a54-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a54-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="15a54-143">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a54-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


