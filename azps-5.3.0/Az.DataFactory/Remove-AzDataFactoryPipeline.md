---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 2bae0bd597cbd97a81efeaecb07e052457b88438
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508470"
---
# <span data-ttu-id="5cba1-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cba1-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="5cba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cba1-102">SYNOPSIS</span></span>
<span data-ttu-id="5cba1-103">Удаляет конвейер из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5cba1-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="5cba1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5cba1-104">SYNTAX</span></span>

### <span data-ttu-id="5cba1-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5cba1-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cba1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5cba1-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cba1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cba1-107">DESCRIPTION</span></span>
<span data-ttu-id="5cba1-108">Для удаления конвейера из фабрики данных Azure удаляется **cmdlet Remove-AzDataFactoryPipeline.**</span><span class="sxs-lookup"><span data-stu-id="5cba1-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="5cba1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5cba1-109">EXAMPLES</span></span>

### <span data-ttu-id="5cba1-110">Пример 1. Удаление конвейера</span><span class="sxs-lookup"><span data-stu-id="5cba1-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="5cba1-111">Этот cmdlet удаляет канал DPWikisample из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5cba1-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="5cba1-112">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="5cba1-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="5cba1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cba1-113">PARAMETERS</span></span>

### <span data-ttu-id="5cba1-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5cba1-114">-DataFactory</span></span>
<span data-ttu-id="5cba1-115">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="5cba1-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5cba1-116">Этот cmdlet удаляет канал из фабрики данных, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="5cba1-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cba1-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5cba1-117">-DataFactoryName</span></span>
<span data-ttu-id="5cba1-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="5cba1-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5cba1-119">Этот cmdlet удаляет канал из фабрики данных, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="5cba1-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cba1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cba1-120">-DefaultProfile</span></span>
<span data-ttu-id="5cba1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5cba1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cba1-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5cba1-122">-Force</span></span>
<span data-ttu-id="5cba1-123">Указывает на то, что этот cmdlet удаляет канал без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5cba1-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="5cba1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5cba1-124">-Name</span></span>
<span data-ttu-id="5cba1-125">Указывает имя конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="5cba1-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="5cba1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cba1-126">-ResourceGroupName</span></span>
<span data-ttu-id="5cba1-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5cba1-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5cba1-128">Этот cmdlet удаляет канал из группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="5cba1-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cba1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cba1-129">-Confirm</span></span>
<span data-ttu-id="5cba1-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cba1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cba1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cba1-131">-WhatIf</span></span>
<span data-ttu-id="5cba1-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cba1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cba1-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5cba1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cba1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cba1-134">CommonParameters</span></span>
<span data-ttu-id="5cba1-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cba1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cba1-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cba1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cba1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cba1-137">INPUTS</span></span>

### <span data-ttu-id="5cba1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5cba1-138">System.String</span></span>

### <span data-ttu-id="5cba1-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5cba1-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="5cba1-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5cba1-140">OUTPUTS</span></span>

### <span data-ttu-id="5cba1-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="5cba1-141">System.Void</span></span>

## <span data-ttu-id="5cba1-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5cba1-142">NOTES</span></span>
* <span data-ttu-id="5cba1-143">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="5cba1-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5cba1-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cba1-144">RELATED LINKS</span></span>

[<span data-ttu-id="5cba1-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cba1-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="5cba1-146">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cba1-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="5cba1-147">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cba1-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="5cba1-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="5cba1-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="5cba1-149">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5cba1-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


