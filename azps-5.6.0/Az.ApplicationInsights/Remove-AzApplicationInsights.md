---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: 089561268233876976598f3cf74cd0a52fef8402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004851"
---
# <span data-ttu-id="0d450-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0d450-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="0d450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d450-102">SYNOPSIS</span></span>
<span data-ttu-id="0d450-103">Удаление ресурса статистики приложения</span><span class="sxs-lookup"><span data-stu-id="0d450-103">Remove an application insights resource</span></span>

## <span data-ttu-id="0d450-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0d450-104">SYNTAX</span></span>

### <span data-ttu-id="0d450-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d450-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d450-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d450-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d450-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d450-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d450-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d450-108">DESCRIPTION</span></span>
<span data-ttu-id="0d450-109">Удаление ресурса статистики приложения</span><span class="sxs-lookup"><span data-stu-id="0d450-109">Remove an application insights resource</span></span>

## <span data-ttu-id="0d450-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0d450-110">EXAMPLES</span></span>

### <span data-ttu-id="0d450-111">Пример 1. Удаление ресурса статистики приложения</span><span class="sxs-lookup"><span data-stu-id="0d450-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="0d450-112">Удаление ресурса аналитики приложения с именем "тест" в группе ресурсов "testgroup"</span><span class="sxs-lookup"><span data-stu-id="0d450-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="0d450-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d450-113">PARAMETERS</span></span>

### <span data-ttu-id="0d450-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0d450-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0d450-115">Компонент "Application Insights".</span><span class="sxs-lookup"><span data-stu-id="0d450-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="0d450-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d450-116">-DefaultProfile</span></span>
<span data-ttu-id="0d450-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d450-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d450-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0d450-118">-Name</span></span>
<span data-ttu-id="0d450-119">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="0d450-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="0d450-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d450-120">-PassThru</span></span>
<span data-ttu-id="0d450-121">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="0d450-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="0d450-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="0d450-122">This parameter is optional.</span></span> <span data-ttu-id="0d450-123">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="0d450-123">Default value is false.</span></span>

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

### <span data-ttu-id="0d450-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d450-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d450-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d450-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="0d450-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d450-126">-ResourceId</span></span>
<span data-ttu-id="0d450-127">ИД ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="0d450-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0d450-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d450-128">-Confirm</span></span>
<span data-ttu-id="0d450-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0d450-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d450-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d450-130">-WhatIf</span></span>
<span data-ttu-id="0d450-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d450-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d450-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0d450-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d450-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d450-133">CommonParameters</span></span>
<span data-ttu-id="0d450-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d450-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d450-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d450-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d450-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d450-136">INPUTS</span></span>

### <span data-ttu-id="0d450-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0d450-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="0d450-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0d450-138">System.String</span></span>

## <span data-ttu-id="0d450-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0d450-139">OUTPUTS</span></span>

### <span data-ttu-id="0d450-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0d450-140">System.Boolean</span></span>

## <span data-ttu-id="0d450-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0d450-141">NOTES</span></span>

## <span data-ttu-id="0d450-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d450-142">RELATED LINKS</span></span>
