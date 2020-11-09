---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: b1d39c3d60d043485cc4ec4dc0c4ba986a97e800
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313820"
---
# <span data-ttu-id="6d218-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="6d218-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="6d218-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d218-102">SYNOPSIS</span></span>
<span data-ttu-id="6d218-103">Удаляет конвейер из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6d218-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="6d218-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d218-104">SYNTAX</span></span>

### <span data-ttu-id="6d218-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6d218-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d218-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6d218-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d218-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6d218-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d218-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d218-108">DESCRIPTION</span></span>
<span data-ttu-id="6d218-109">Командлет Remove-AzDataFactoryV2Pipeline удаляет конвейер из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="6d218-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="6d218-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d218-110">EXAMPLES</span></span>

### <span data-ttu-id="6d218-111">Пример 1: удаление конвейера</span><span class="sxs-lookup"><span data-stu-id="6d218-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="6d218-112">Этот командлет удаляет конвейер с именем DPWikisample из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="6d218-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="6d218-113">Команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="6d218-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="6d218-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d218-114">PARAMETERS</span></span>

### <span data-ttu-id="6d218-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6d218-115">-DataFactoryName</span></span>
<span data-ttu-id="6d218-116">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6d218-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6d218-117">Этот командлет удаляет конвейер из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6d218-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6d218-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d218-118">-DefaultProfile</span></span>
<span data-ttu-id="6d218-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d218-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d218-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6d218-120">-Force</span></span>
<span data-ttu-id="6d218-121">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6d218-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6d218-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d218-122">-InputObject</span></span>
<span data-ttu-id="6d218-123">Указывает объект конвейера.</span><span class="sxs-lookup"><span data-stu-id="6d218-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="6d218-124">Этот командлет удаляет конвейер, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6d218-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d218-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d218-125">-Name</span></span>
<span data-ttu-id="6d218-126">Указывает имя конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6d218-126">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d218-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d218-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d218-128">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6d218-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6d218-129">Этот командлет удаляет конвейер из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6d218-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6d218-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d218-130">-ResourceId</span></span>
<span data-ttu-id="6d218-131">Идентификатор ресурса Azure для конвейера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6d218-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d218-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d218-132">-Confirm</span></span>
<span data-ttu-id="6d218-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d218-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d218-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d218-134">-WhatIf</span></span>
<span data-ttu-id="6d218-135">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="6d218-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6d218-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d218-136">CommonParameters</span></span>
<span data-ttu-id="6d218-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d218-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d218-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d218-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d218-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d218-139">INPUTS</span></span>

### <span data-ttu-id="6d218-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="6d218-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="6d218-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6d218-141">System.String</span></span>

## <span data-ttu-id="6d218-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d218-142">OUTPUTS</span></span>

### <span data-ttu-id="6d218-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d218-143">System.Boolean</span></span>

## <span data-ttu-id="6d218-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d218-144">NOTES</span></span>
<span data-ttu-id="6d218-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="6d218-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6d218-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d218-146">RELATED LINKS</span></span>

[<span data-ttu-id="6d218-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="6d218-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="6d218-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="6d218-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="6d218-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="6d218-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

