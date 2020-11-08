---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 42d9de3f23f1aca904aa0f42722217d0b9bf8a3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235620"
---
# <span data-ttu-id="8fccc-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="8fccc-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="8fccc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8fccc-102">SYNOPSIS</span></span>
<span data-ttu-id="8fccc-103">Создает поток данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="8fccc-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="8fccc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8fccc-104">SYNTAX</span></span>

### <span data-ttu-id="8fccc-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8fccc-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8fccc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8fccc-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fccc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fccc-107">DESCRIPTION</span></span>
<span data-ttu-id="8fccc-108">Командлет Set-AzDataFactoryV2DataFlow создает поток данных или обновляет существующий поток данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="8fccc-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="8fccc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8fccc-109">EXAMPLES</span></span>

### <span data-ttu-id="8fccc-110">Пример 1: создание потока данных</span><span class="sxs-lookup"><span data-stu-id="8fccc-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="8fccc-111">Эта команда создает поток данных с именем TaxiDemo1 в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8fccc-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="8fccc-112">В команде поток данных заосновывается на сведениях в TaxiDemo1.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="8fccc-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="8fccc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8fccc-113">PARAMETERS</span></span>

### <span data-ttu-id="8fccc-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8fccc-114">-DataFactoryName</span></span>
<span data-ttu-id="8fccc-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8fccc-115">The data factory name.</span></span>

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

### <span data-ttu-id="8fccc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fccc-116">-DefaultProfile</span></span>
<span data-ttu-id="8fccc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8fccc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fccc-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="8fccc-118">-DefinitionFile</span></span>
<span data-ttu-id="8fccc-119">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="8fccc-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fccc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8fccc-120">-Force</span></span>
<span data-ttu-id="8fccc-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="8fccc-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8fccc-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8fccc-122">-Name</span></span>
<span data-ttu-id="8fccc-123">Имя потока данных.</span><span class="sxs-lookup"><span data-stu-id="8fccc-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fccc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fccc-124">-ResourceGroupName</span></span>
<span data-ttu-id="8fccc-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8fccc-125">The resource group name.</span></span>

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

### <span data-ttu-id="8fccc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fccc-126">-ResourceId</span></span>
<span data-ttu-id="8fccc-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="8fccc-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8fccc-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fccc-128">-Confirm</span></span>
<span data-ttu-id="8fccc-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8fccc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fccc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fccc-130">-WhatIf</span></span>
<span data-ttu-id="8fccc-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8fccc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fccc-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8fccc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fccc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fccc-133">CommonParameters</span></span>
<span data-ttu-id="8fccc-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8fccc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fccc-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fccc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fccc-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8fccc-136">INPUTS</span></span>

### <span data-ttu-id="8fccc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8fccc-137">System.String</span></span>

## <span data-ttu-id="8fccc-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fccc-138">OUTPUTS</span></span>

### <span data-ttu-id="8fccc-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="8fccc-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="8fccc-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="8fccc-140">NOTES</span></span>
<span data-ttu-id="8fccc-141">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="8fccc-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8fccc-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8fccc-142">RELATED LINKS</span></span>

[<span data-ttu-id="8fccc-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="8fccc-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="8fccc-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="8fccc-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
