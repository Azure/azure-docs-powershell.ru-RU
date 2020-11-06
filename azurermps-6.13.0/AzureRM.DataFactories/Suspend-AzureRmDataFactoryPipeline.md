---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/suspend-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: ecbf1a97ebaa7f4d008b63f9b7d4c49c49a09956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568189"
---
# <span data-ttu-id="55bed-101">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="55bed-101">Suspend-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="55bed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55bed-102">SYNOPSIS</span></span>
<span data-ttu-id="55bed-103">Приостанавливает конвейер в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="55bed-103">Suspends a pipeline in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55bed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55bed-104">SYNTAX</span></span>

### <span data-ttu-id="55bed-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55bed-105">ByFactoryName (Default)</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55bed-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="55bed-106">ByFactoryObject</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55bed-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55bed-107">DESCRIPTION</span></span>
<span data-ttu-id="55bed-108">Командлет **Suspend-AzureRmDataFactoryPipeline** приостанавливает конвейер в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="55bed-108">The **Suspend-AzureRmDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="55bed-109">Вы можете возобновить конвейер с помощью командлета Resume-AzureRmDataFactoryPipeline.</span><span class="sxs-lookup"><span data-stu-id="55bed-109">You can resume the pipeline by using the Resume-AzureRmDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="55bed-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55bed-110">EXAMPLES</span></span>

### <span data-ttu-id="55bed-111">Пример 1: Приостановка конвейера</span><span class="sxs-lookup"><span data-stu-id="55bed-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="55bed-112">Эта команда приостанавливает конвейер с именем DPWikiSample в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="55bed-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="55bed-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="55bed-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="55bed-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55bed-114">PARAMETERS</span></span>

### <span data-ttu-id="55bed-115">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="55bed-115">-DataFactory</span></span>
<span data-ttu-id="55bed-116">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="55bed-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="55bed-117">Этот командлет приостанавливает конвейер, принадлежащий к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="55bed-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="55bed-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="55bed-118">-DataFactoryName</span></span>
<span data-ttu-id="55bed-119">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="55bed-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="55bed-120">Этот командлет приостанавливает конвейер, принадлежащий к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="55bed-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="55bed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55bed-121">-DefaultProfile</span></span>
<span data-ttu-id="55bed-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="55bed-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55bed-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55bed-123">-Name</span></span>
<span data-ttu-id="55bed-124">Указывает имя конвейера, который нужно приостановить.</span><span class="sxs-lookup"><span data-stu-id="55bed-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="55bed-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55bed-125">-ResourceGroupName</span></span>
<span data-ttu-id="55bed-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="55bed-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="55bed-127">Этот командлет приостанавливает конвейер, принадлежащий к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="55bed-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="55bed-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55bed-128">-Confirm</span></span>
<span data-ttu-id="55bed-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55bed-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55bed-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55bed-130">-WhatIf</span></span>
<span data-ttu-id="55bed-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55bed-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55bed-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55bed-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55bed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55bed-133">CommonParameters</span></span>
<span data-ttu-id="55bed-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55bed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55bed-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55bed-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55bed-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55bed-136">INPUTS</span></span>

### <span data-ttu-id="55bed-137">System. String</span><span class="sxs-lookup"><span data-stu-id="55bed-137">System.String</span></span>

### <span data-ttu-id="55bed-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="55bed-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="55bed-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55bed-139">OUTPUTS</span></span>

### <span data-ttu-id="55bed-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55bed-140">System.Boolean</span></span>

## <span data-ttu-id="55bed-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="55bed-141">NOTES</span></span>
* <span data-ttu-id="55bed-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="55bed-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="55bed-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55bed-143">RELATED LINKS</span></span>

[<span data-ttu-id="55bed-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="55bed-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="55bed-145">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="55bed-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="55bed-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="55bed-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="55bed-147">Возобновить — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="55bed-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="55bed-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="55bed-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


