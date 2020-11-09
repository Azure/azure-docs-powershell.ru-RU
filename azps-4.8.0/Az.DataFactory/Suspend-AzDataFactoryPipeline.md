---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243671"
---
# <span data-ttu-id="a108b-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a108b-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="a108b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a108b-102">SYNOPSIS</span></span>
<span data-ttu-id="a108b-103">Приостанавливает конвейер в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a108b-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="a108b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a108b-104">SYNTAX</span></span>

### <span data-ttu-id="a108b-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a108b-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a108b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a108b-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a108b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a108b-107">DESCRIPTION</span></span>
<span data-ttu-id="a108b-108">Командлет **Suspend-AzDataFactoryPipeline** приостанавливает конвейер в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a108b-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="a108b-109">Вы можете возобновить конвейер с помощью командлета Resume-AzDataFactoryPipeline.</span><span class="sxs-lookup"><span data-stu-id="a108b-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="a108b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a108b-110">EXAMPLES</span></span>

### <span data-ttu-id="a108b-111">Пример 1: Приостановка конвейера</span><span class="sxs-lookup"><span data-stu-id="a108b-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="a108b-112">Эта команда приостанавливает конвейер с именем DPWikiSample в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a108b-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="a108b-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="a108b-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="a108b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a108b-114">PARAMETERS</span></span>

### <span data-ttu-id="a108b-115">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="a108b-115">-DataFactory</span></span>
<span data-ttu-id="a108b-116">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="a108b-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a108b-117">Этот командлет приостанавливает конвейер, принадлежащий к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a108b-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a108b-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a108b-118">-DataFactoryName</span></span>
<span data-ttu-id="a108b-119">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a108b-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a108b-120">Этот командлет приостанавливает конвейер, принадлежащий к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a108b-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a108b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a108b-121">-DefaultProfile</span></span>
<span data-ttu-id="a108b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a108b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a108b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a108b-123">-Name</span></span>
<span data-ttu-id="a108b-124">Указывает имя конвейера, который нужно приостановить.</span><span class="sxs-lookup"><span data-stu-id="a108b-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="a108b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a108b-125">-ResourceGroupName</span></span>
<span data-ttu-id="a108b-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a108b-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a108b-127">Этот командлет приостанавливает конвейер, принадлежащий к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a108b-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a108b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a108b-128">-Confirm</span></span>
<span data-ttu-id="a108b-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a108b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a108b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a108b-130">-WhatIf</span></span>
<span data-ttu-id="a108b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a108b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a108b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a108b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a108b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a108b-133">CommonParameters</span></span>
<span data-ttu-id="a108b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a108b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a108b-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a108b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a108b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a108b-136">INPUTS</span></span>

### <span data-ttu-id="a108b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a108b-137">System.String</span></span>

### <span data-ttu-id="a108b-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a108b-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="a108b-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a108b-139">OUTPUTS</span></span>

### <span data-ttu-id="a108b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a108b-140">System.Boolean</span></span>

## <span data-ttu-id="a108b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a108b-141">NOTES</span></span>
* <span data-ttu-id="a108b-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="a108b-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a108b-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a108b-143">RELATED LINKS</span></span>

[<span data-ttu-id="a108b-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a108b-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="a108b-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a108b-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="a108b-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a108b-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="a108b-147">Возобновить — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a108b-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="a108b-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a108b-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

