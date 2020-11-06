---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: aede985cfac5b8ab25c4056eb44e54ea7c6b1c2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566525"
---
# <span data-ttu-id="d2a8f-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d2a8f-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="d2a8f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a8f-103">Удаляет конвейер из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2a8f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2a8f-104">SYNTAX</span></span>

### <span data-ttu-id="d2a8f-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2a8f-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2a8f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d2a8f-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2a8f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2a8f-107">DESCRIPTION</span></span>
<span data-ttu-id="d2a8f-108">Командлет **Remove-AzureRmDataFactoryPipeline** удаляет конвейер из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="d2a8f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2a8f-109">EXAMPLES</span></span>

### <span data-ttu-id="d2a8f-110">Пример 1: удаление конвейера</span><span class="sxs-lookup"><span data-stu-id="d2a8f-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="d2a8f-111">Этот командлет удаляет конвейер с именем DPWikisample из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="d2a8f-112">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="d2a8f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2a8f-113">PARAMETERS</span></span>

### <span data-ttu-id="d2a8f-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-114">-DataFactory</span></span>
<span data-ttu-id="d2a8f-115">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d2a8f-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d2a8f-116">Этот командлет удаляет конвейер из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2a8f-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d2a8f-117">-DataFactoryName</span></span>
<span data-ttu-id="d2a8f-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d2a8f-119">Этот командлет удаляет конвейер из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2a8f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a8f-120">-DefaultProfile</span></span>
<span data-ttu-id="d2a8f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d2a8f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2a8f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d2a8f-122">-Force</span></span>
<span data-ttu-id="d2a8f-123">Указывает на то, что этот командлет удаляет конвейер без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d2a8f-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2a8f-124">-Name</span></span>
<span data-ttu-id="d2a8f-125">Указывает имя конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="d2a8f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a8f-126">-ResourceGroupName</span></span>
<span data-ttu-id="d2a8f-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d2a8f-128">Этот командлет удаляет конвейер из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2a8f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2a8f-129">-Confirm</span></span>
<span data-ttu-id="d2a8f-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2a8f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2a8f-131">-WhatIf</span></span>
<span data-ttu-id="d2a8f-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2a8f-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2a8f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a8f-134">CommonParameters</span></span>
<span data-ttu-id="d2a8f-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2a8f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a8f-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a8f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a8f-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2a8f-137">INPUTS</span></span>

### <span data-ttu-id="d2a8f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d2a8f-138">System.String</span></span>

### <span data-ttu-id="d2a8f-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d2a8f-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="d2a8f-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2a8f-140">OUTPUTS</span></span>

### <span data-ttu-id="d2a8f-141">System. void</span><span class="sxs-lookup"><span data-stu-id="d2a8f-141">System.Void</span></span>

## <span data-ttu-id="d2a8f-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2a8f-142">NOTES</span></span>
* <span data-ttu-id="d2a8f-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="d2a8f-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d2a8f-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2a8f-144">RELATED LINKS</span></span>

[<span data-ttu-id="d2a8f-145">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d2a8f-145">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d2a8f-146">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d2a8f-146">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d2a8f-147">Возобновить — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d2a8f-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d2a8f-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d2a8f-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="d2a8f-149">Приостановить — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d2a8f-149">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


