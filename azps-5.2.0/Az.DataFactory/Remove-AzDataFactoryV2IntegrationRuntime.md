---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329338"
---
# <span data-ttu-id="95506-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="95506-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="95506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95506-102">SYNOPSIS</span></span>
<span data-ttu-id="95506-103">Удаляет время интеграции со временем запуска.</span><span class="sxs-lookup"><span data-stu-id="95506-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="95506-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95506-104">SYNTAX</span></span>

### <span data-ttu-id="95506-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95506-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95506-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="95506-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95506-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="95506-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95506-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95506-108">DESCRIPTION</span></span>
<span data-ttu-id="95506-109">Этот Remove-AzDataFactoryV2IntegrationRuntime удаляет время интеграции.</span><span class="sxs-lookup"><span data-stu-id="95506-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="95506-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95506-110">EXAMPLES</span></span>

### <span data-ttu-id="95506-111">Пример 1. Удаление времени запуска интеграции</span><span class="sxs-lookup"><span data-stu-id="95506-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="95506-112">Эта команда удаляет время интеграции с именем test-reserved-ir из фабрики данных test-df.</span><span class="sxs-lookup"><span data-stu-id="95506-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="95506-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="95506-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="95506-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95506-114">PARAMETERS</span></span>

### <span data-ttu-id="95506-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="95506-115">-DataFactoryName</span></span>
<span data-ttu-id="95506-116">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="95506-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95506-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95506-117">-DefaultProfile</span></span>
<span data-ttu-id="95506-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95506-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95506-119">-Force</span><span class="sxs-lookup"><span data-stu-id="95506-119">-Force</span></span>
<span data-ttu-id="95506-120">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="95506-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="95506-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95506-121">-InputObject</span></span>
<span data-ttu-id="95506-122">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="95506-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95506-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="95506-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="95506-124">Название связанной фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="95506-124">The linked data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95506-125">-Name</span><span class="sxs-lookup"><span data-stu-id="95506-125">-Name</span></span>
<span data-ttu-id="95506-126">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="95506-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95506-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95506-127">-ResourceGroupName</span></span>
<span data-ttu-id="95506-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95506-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95506-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95506-129">-ResourceId</span></span>
<span data-ttu-id="95506-130">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="95506-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95506-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95506-131">-Confirm</span></span>
<span data-ttu-id="95506-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95506-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95506-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95506-133">-WhatIf</span></span>
<span data-ttu-id="95506-134">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95506-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="95506-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95506-135">CommonParameters</span></span>
<span data-ttu-id="95506-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95506-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95506-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95506-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95506-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95506-138">INPUTS</span></span>

### <span data-ttu-id="95506-139">System.String</span><span class="sxs-lookup"><span data-stu-id="95506-139">System.String</span></span>

### <span data-ttu-id="95506-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="95506-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="95506-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95506-141">OUTPUTS</span></span>

### <span data-ttu-id="95506-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="95506-142">System.Void</span></span>

## <span data-ttu-id="95506-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95506-143">NOTES</span></span>
<span data-ttu-id="95506-144">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="95506-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="95506-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95506-145">RELATED LINKS</span></span>

[<span data-ttu-id="95506-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="95506-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="95506-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="95506-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

