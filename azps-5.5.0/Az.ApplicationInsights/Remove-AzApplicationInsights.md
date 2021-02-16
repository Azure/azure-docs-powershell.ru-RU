---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: b63f1b350daad55a26dc91f46e89b28675622fbb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216321"
---
# <span data-ttu-id="7f7b2-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7f7b2-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="7f7b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7b2-103">Удаление ресурса статистики приложения</span><span class="sxs-lookup"><span data-stu-id="7f7b2-103">Remove an application insights resource</span></span>

## <span data-ttu-id="7f7b2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f7b2-104">SYNTAX</span></span>

### <span data-ttu-id="7f7b2-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7f7b2-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f7b2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f7b2-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f7b2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f7b2-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f7b2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f7b2-108">DESCRIPTION</span></span>
<span data-ttu-id="7f7b2-109">Удаление ресурса статистики приложения</span><span class="sxs-lookup"><span data-stu-id="7f7b2-109">Remove an application insights resource</span></span>

## <span data-ttu-id="7f7b2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f7b2-110">EXAMPLES</span></span>

### <span data-ttu-id="7f7b2-111">Пример 1. Удаление ресурса статистики приложения</span><span class="sxs-lookup"><span data-stu-id="7f7b2-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="7f7b2-112">Удаление ресурса аналитики приложения с именем "тест" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="7f7b2-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="7f7b2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f7b2-113">PARAMETERS</span></span>

### <span data-ttu-id="7f7b2-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7f7b2-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="7f7b2-115">Компонент "Application Insights".</span><span class="sxs-lookup"><span data-stu-id="7f7b2-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="7f7b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7b2-116">-DefaultProfile</span></span>
<span data-ttu-id="7f7b2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f7b2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f7b2-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7f7b2-118">-Name</span></span>
<span data-ttu-id="7f7b2-119">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7f7b2-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="7f7b2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f7b2-120">-PassThru</span></span>
<span data-ttu-id="7f7b2-121">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="7f7b2-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="7f7b2-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7f7b2-122">This parameter is optional.</span></span> <span data-ttu-id="7f7b2-123">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="7f7b2-123">Default value is false.</span></span>

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

### <span data-ttu-id="7f7b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f7b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="7f7b2-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7f7b2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="7f7b2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f7b2-126">-ResourceId</span></span>
<span data-ttu-id="7f7b2-127">ИД ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7f7b2-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="7f7b2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f7b2-128">-Confirm</span></span>
<span data-ttu-id="7f7b2-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f7b2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f7b2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f7b2-130">-WhatIf</span></span>
<span data-ttu-id="7f7b2-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f7b2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f7b2-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7f7b2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f7b2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7b2-133">CommonParameters</span></span>
<span data-ttu-id="7f7b2-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f7b2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7b2-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f7b2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7b2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f7b2-136">INPUTS</span></span>

### <span data-ttu-id="7f7b2-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7f7b2-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="7f7b2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7f7b2-138">System.String</span></span>

## <span data-ttu-id="7f7b2-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f7b2-139">OUTPUTS</span></span>

### <span data-ttu-id="7f7b2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f7b2-140">System.Boolean</span></span>

## <span data-ttu-id="7f7b2-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f7b2-141">NOTES</span></span>

## <span data-ttu-id="7f7b2-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f7b2-142">RELATED LINKS</span></span>
