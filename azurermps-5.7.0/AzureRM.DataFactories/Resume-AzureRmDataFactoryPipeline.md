---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/resume-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 5cf769a02b6a02f0fba9b26df48554d80a406140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559124"
---
# <span data-ttu-id="d3c1d-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d3c1d-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="d3c1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c1d-103">Возобновляет приостановленный конвейер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3c1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3c1d-104">SYNTAX</span></span>

### <span data-ttu-id="d3c1d-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3c1d-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3c1d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d3c1d-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3c1d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3c1d-107">DESCRIPTION</span></span>
<span data-ttu-id="d3c1d-108">Командлет **Resume-AzureRmDataFactoryPipeline** возобновляет приостановленный конвейер в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="d3c1d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3c1d-109">EXAMPLES</span></span>

### <span data-ttu-id="d3c1d-110">Пример 1: возобновление процесса продаж</span><span class="sxs-lookup"><span data-stu-id="d3c1d-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="d3c1d-111">Эта команда возобновляет конвейер с именем DPWikisample в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="d3c1d-112">Приостановка конвейера с помощью командлета **Suspend-AzureRmDataFactoryPipeline** .</span><span class="sxs-lookup"><span data-stu-id="d3c1d-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="d3c1d-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="d3c1d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3c1d-114">PARAMETERS</span></span>

### <span data-ttu-id="d3c1d-115">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-115">-DataFactory</span></span>
<span data-ttu-id="d3c1d-116">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d3c1d-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d3c1d-117">Этот командлет возобновляет конвейер, принадлежащий к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c1d-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d3c1d-118">-DataFactoryName</span></span>
<span data-ttu-id="d3c1d-119">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d3c1d-120">Этот командлет возобновляет конвейер, принадлежащий к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c1d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c1d-121">-DefaultProfile</span></span>
<span data-ttu-id="d3c1d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d3c1d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c1d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3c1d-123">-Name</span></span>
<span data-ttu-id="d3c1d-124">Указывает имя конвейера для возобновления.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-124">Specifies the name of the pipeline to resume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c1d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3c1d-125">-ResourceGroupName</span></span>
<span data-ttu-id="d3c1d-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d3c1d-127">Этот командлет возобновляет конвейер, принадлежащий группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c1d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3c1d-128">-Confirm</span></span>
<span data-ttu-id="d3c1d-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c1d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3c1d-130">-WhatIf</span></span>
<span data-ttu-id="d3c1d-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3c1d-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c1d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c1d-133">CommonParameters</span></span>
<span data-ttu-id="d3c1d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c1d-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c1d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c1d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3c1d-136">INPUTS</span></span>

### <span data-ttu-id="d3c1d-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="d3c1d-137">None</span></span>
<span data-ttu-id="d3c1d-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d3c1d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d3c1d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3c1d-139">OUTPUTS</span></span>

### <span data-ttu-id="d3c1d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3c1d-140">System.Boolean</span></span>

## <span data-ttu-id="d3c1d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3c1d-141">NOTES</span></span>
* <span data-ttu-id="d3c1d-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="d3c1d-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d3c1d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3c1d-143">RELATED LINKS</span></span>

[<span data-ttu-id="d3c1d-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d3c1d-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d3c1d-145">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d3c1d-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d3c1d-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d3c1d-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d3c1d-147">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d3c1d-147">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="d3c1d-148">Приостановить — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d3c1d-148">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


