---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: b63f1b350daad55a26dc91f46e89b28675622fbb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249124"
---
# <span data-ttu-id="61f08-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="61f08-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="61f08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61f08-102">SYNOPSIS</span></span>
<span data-ttu-id="61f08-103">Удаление ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="61f08-103">Remove an application insights resource</span></span>

## <span data-ttu-id="61f08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61f08-104">SYNTAX</span></span>

### <span data-ttu-id="61f08-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61f08-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f08-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61f08-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f08-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61f08-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61f08-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61f08-108">DESCRIPTION</span></span>
<span data-ttu-id="61f08-109">Удаление ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="61f08-109">Remove an application insights resource</span></span>

## <span data-ttu-id="61f08-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61f08-110">EXAMPLES</span></span>

### <span data-ttu-id="61f08-111">Пример 1. Удалите ресурс Application Insights</span><span class="sxs-lookup"><span data-stu-id="61f08-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="61f08-112">Удаление ресурса Application Insights с именем "Test" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="61f08-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="61f08-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61f08-113">PARAMETERS</span></span>

### <span data-ttu-id="61f08-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="61f08-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="61f08-115">Объект компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="61f08-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61f08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f08-116">-DefaultProfile</span></span>
<span data-ttu-id="61f08-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61f08-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f08-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61f08-118">-Name</span></span>
<span data-ttu-id="61f08-119">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="61f08-119">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f08-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61f08-120">-PassThru</span></span>
<span data-ttu-id="61f08-121">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="61f08-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="61f08-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="61f08-122">This parameter is optional.</span></span> <span data-ttu-id="61f08-123">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="61f08-123">Default value is false.</span></span>

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

### <span data-ttu-id="61f08-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f08-124">-ResourceGroupName</span></span>
<span data-ttu-id="61f08-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61f08-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f08-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61f08-126">-ResourceId</span></span>
<span data-ttu-id="61f08-127">Идентификатор ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="61f08-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f08-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61f08-128">-Confirm</span></span>
<span data-ttu-id="61f08-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61f08-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f08-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f08-130">-WhatIf</span></span>
<span data-ttu-id="61f08-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61f08-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f08-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61f08-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f08-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f08-133">CommonParameters</span></span>
<span data-ttu-id="61f08-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61f08-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f08-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61f08-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f08-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61f08-136">INPUTS</span></span>

### <span data-ttu-id="61f08-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="61f08-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="61f08-138">System. String</span><span class="sxs-lookup"><span data-stu-id="61f08-138">System.String</span></span>

## <span data-ttu-id="61f08-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61f08-139">OUTPUTS</span></span>

### <span data-ttu-id="61f08-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61f08-140">System.Boolean</span></span>

## <span data-ttu-id="61f08-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="61f08-141">NOTES</span></span>

## <span data-ttu-id="61f08-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61f08-142">RELATED LINKS</span></span>
