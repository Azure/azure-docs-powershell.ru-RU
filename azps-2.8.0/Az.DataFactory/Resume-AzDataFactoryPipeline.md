---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/resume-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
ms.openlocfilehash: 221fb414464c062a2f1798223bfe68a09543d7c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721454"
---
# <span data-ttu-id="ad8fa-101">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ad8fa-101">Resume-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="ad8fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad8fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ad8fa-103">Возобновляет приостановленный конвейер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-103">Resumes a suspended pipeline in Data Factory.</span></span>

## <span data-ttu-id="ad8fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad8fa-104">SYNTAX</span></span>

### <span data-ttu-id="ad8fa-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad8fa-105">ByFactoryName (Default)</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad8fa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ad8fa-106">ByFactoryObject</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad8fa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad8fa-107">DESCRIPTION</span></span>
<span data-ttu-id="ad8fa-108">Командлет **Resume-AzDataFactoryPipeline** возобновляет приостановленный конвейер в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-108">The **Resume-AzDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="ad8fa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad8fa-109">EXAMPLES</span></span>

### <span data-ttu-id="ad8fa-110">Пример 1: возобновление процесса продаж</span><span class="sxs-lookup"><span data-stu-id="ad8fa-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="ad8fa-111">Эта команда возобновляет конвейер с именем DPWikisample в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="ad8fa-112">Приостановка конвейера с помощью командлета **Suspend-AzDataFactoryPipeline** .</span><span class="sxs-lookup"><span data-stu-id="ad8fa-112">Use the **Suspend-AzDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="ad8fa-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="ad8fa-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad8fa-114">PARAMETERS</span></span>

### <span data-ttu-id="ad8fa-115">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-115">-DataFactory</span></span>
<span data-ttu-id="ad8fa-116">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="ad8fa-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ad8fa-117">Этот командлет возобновляет конвейер, принадлежащий к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad8fa-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ad8fa-118">-DataFactoryName</span></span>
<span data-ttu-id="ad8fa-119">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ad8fa-120">Этот командлет возобновляет конвейер, принадлежащий к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad8fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad8fa-121">-DefaultProfile</span></span>
<span data-ttu-id="ad8fa-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ad8fa-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad8fa-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad8fa-123">-Name</span></span>
<span data-ttu-id="ad8fa-124">Указывает имя конвейера для возобновления.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-124">Specifies the name of the pipeline to resume.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad8fa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad8fa-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad8fa-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ad8fa-127">Этот командлет возобновляет конвейер, принадлежащий группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad8fa-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad8fa-128">-Confirm</span></span>
<span data-ttu-id="ad8fa-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad8fa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad8fa-130">-WhatIf</span></span>
<span data-ttu-id="ad8fa-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad8fa-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad8fa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad8fa-133">CommonParameters</span></span>
<span data-ttu-id="ad8fa-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad8fa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad8fa-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad8fa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad8fa-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad8fa-136">INPUTS</span></span>

### <span data-ttu-id="ad8fa-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ad8fa-137">System.String</span></span>

### <span data-ttu-id="ad8fa-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ad8fa-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ad8fa-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad8fa-139">OUTPUTS</span></span>

### <span data-ttu-id="ad8fa-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad8fa-140">System.Boolean</span></span>

## <span data-ttu-id="ad8fa-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad8fa-141">NOTES</span></span>
* <span data-ttu-id="ad8fa-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="ad8fa-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ad8fa-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad8fa-143">RELATED LINKS</span></span>

[<span data-ttu-id="ad8fa-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ad8fa-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="ad8fa-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ad8fa-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="ad8fa-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ad8fa-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="ad8fa-147">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="ad8fa-147">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="ad8fa-148">Приостановить — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="ad8fa-148">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


