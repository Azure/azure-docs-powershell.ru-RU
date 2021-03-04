---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 95f99f629fd32333e06c6194fcaf51837224f4a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956088"
---
# <span data-ttu-id="d1ee3-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="d1ee3-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="d1ee3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ee3-103">Удаление ключа API для анализа приложения</span><span class="sxs-lookup"><span data-stu-id="d1ee3-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="d1ee3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d1ee3-104">SYNTAX</span></span>

### <span data-ttu-id="d1ee3-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d1ee3-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1ee3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1ee3-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1ee3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1ee3-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1ee3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1ee3-108">DESCRIPTION</span></span>
<span data-ttu-id="d1ee3-109">Удаление ключа API для анализа приложения</span><span class="sxs-lookup"><span data-stu-id="d1ee3-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="d1ee3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d1ee3-110">EXAMPLES</span></span>

### <span data-ttu-id="d1ee3-111">Пример 1. Удаление ключа API статистики приложения</span><span class="sxs-lookup"><span data-stu-id="d1ee3-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="d1ee3-112">Удалите ключ API конкретного приложения с ид "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" для "test" в группе ресурсов "testGroup".</span><span class="sxs-lookup"><span data-stu-id="d1ee3-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="d1ee3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1ee3-113">PARAMETERS</span></span>

### <span data-ttu-id="d1ee3-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="d1ee3-114">-ApiKeyId</span></span>
<span data-ttu-id="d1ee3-115">ИД ключа API application Insights.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-115">Application Insights API Key ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ee3-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d1ee3-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="d1ee3-117">Компонент "Application Insights".</span><span class="sxs-lookup"><span data-stu-id="d1ee3-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="d1ee3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ee3-118">-DefaultProfile</span></span>
<span data-ttu-id="d1ee3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1ee3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d1ee3-120">-Name</span></span>
<span data-ttu-id="d1ee3-121">Имя компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="d1ee3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1ee3-122">-PassThru</span></span>
<span data-ttu-id="d1ee3-123">Если этот задан, будет указано "Истина" в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="d1ee3-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-124">This parameter is optional.</span></span> <span data-ttu-id="d1ee3-125">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-125">Default value is false.</span></span>

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

### <span data-ttu-id="d1ee3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1ee3-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1ee3-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="d1ee3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1ee3-128">-ResourceId</span></span>
<span data-ttu-id="d1ee3-129">ИД ресурса компонента Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="d1ee3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1ee3-130">-Confirm</span></span>
<span data-ttu-id="d1ee3-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1ee3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1ee3-132">-WhatIf</span></span>
<span data-ttu-id="d1ee3-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1ee3-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1ee3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ee3-135">CommonParameters</span></span>
<span data-ttu-id="d1ee3-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ee3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ee3-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1ee3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ee3-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1ee3-138">INPUTS</span></span>

### <span data-ttu-id="d1ee3-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d1ee3-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="d1ee3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d1ee3-140">System.String</span></span>

## <span data-ttu-id="d1ee3-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d1ee3-141">OUTPUTS</span></span>

### <span data-ttu-id="d1ee3-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1ee3-142">System.Boolean</span></span>

## <span data-ttu-id="d1ee3-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d1ee3-143">NOTES</span></span>

## <span data-ttu-id="d1ee3-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1ee3-144">RELATED LINKS</span></span>
