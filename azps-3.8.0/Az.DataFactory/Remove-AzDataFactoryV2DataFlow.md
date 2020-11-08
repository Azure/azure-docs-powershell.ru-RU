---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 8b5b9e8cfd1909b0d91627a2c0600620f264da78
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064940"
---
# <span data-ttu-id="e5d98-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="e5d98-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="e5d98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5d98-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d98-103">Удаляет поток данных из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e5d98-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="e5d98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5d98-104">SYNTAX</span></span>

### <span data-ttu-id="e5d98-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5d98-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5d98-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5d98-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5d98-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5d98-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5d98-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5d98-108">DESCRIPTION</span></span>
<span data-ttu-id="e5d98-109">Командлет Remove-AzDataFactoryV2DataFlow удаляет поток данных из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d98-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="e5d98-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5d98-110">EXAMPLES</span></span>

### <span data-ttu-id="e5d98-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5d98-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="e5d98-112">Эта команда удаляет поток данных с именем dataflow5 из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e5d98-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="e5d98-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5d98-113">PARAMETERS</span></span>

### <span data-ttu-id="e5d98-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e5d98-114">-DataFactoryName</span></span>
<span data-ttu-id="e5d98-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e5d98-115">The data factory name.</span></span>

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

### <span data-ttu-id="e5d98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d98-116">-DefaultProfile</span></span>
<span data-ttu-id="e5d98-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d98-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5d98-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e5d98-118">-Force</span></span>
<span data-ttu-id="e5d98-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e5d98-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e5d98-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5d98-120">-InputObject</span></span>
<span data-ttu-id="e5d98-121">Объект потока данных.</span><span class="sxs-lookup"><span data-stu-id="e5d98-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d98-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5d98-122">-Name</span></span>
<span data-ttu-id="e5d98-123">Имя потока данных.</span><span class="sxs-lookup"><span data-stu-id="e5d98-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d98-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5d98-124">-ResourceGroupName</span></span>
<span data-ttu-id="e5d98-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5d98-125">The resource group name.</span></span>

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

### <span data-ttu-id="e5d98-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5d98-126">-ResourceId</span></span>
<span data-ttu-id="e5d98-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d98-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e5d98-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5d98-128">-PassThru</span></span>
<span data-ttu-id="e5d98-129">Если задано значение true, операция Case запишется успешно.</span><span class="sxs-lookup"><span data-stu-id="e5d98-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="e5d98-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e5d98-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="e5d98-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5d98-131">-Confirm</span></span>
<span data-ttu-id="e5d98-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5d98-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5d98-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5d98-133">-WhatIf</span></span>
<span data-ttu-id="e5d98-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5d98-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5d98-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5d98-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5d98-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d98-136">CommonParameters</span></span>
<span data-ttu-id="e5d98-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5d98-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d98-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5d98-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d98-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5d98-139">INPUTS</span></span>

### <span data-ttu-id="e5d98-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="e5d98-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="e5d98-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e5d98-141">System.String</span></span>

## <span data-ttu-id="e5d98-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5d98-142">OUTPUTS</span></span>

### <span data-ttu-id="e5d98-143">System. void</span><span class="sxs-lookup"><span data-stu-id="e5d98-143">System.Void</span></span>

### <span data-ttu-id="e5d98-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5d98-144">System.Boolean</span></span>

## <span data-ttu-id="e5d98-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5d98-145">NOTES</span></span>
<span data-ttu-id="e5d98-146">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="e5d98-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e5d98-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5d98-147">RELATED LINKS</span></span>

[<span data-ttu-id="e5d98-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="e5d98-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="e5d98-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="e5d98-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

