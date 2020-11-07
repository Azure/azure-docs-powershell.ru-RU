---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: f84973c29d83e8c7c01c3505d17166275a833460
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721461"
---
# <span data-ttu-id="b7749-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b7749-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="b7749-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7749-102">SYNOPSIS</span></span>
<span data-ttu-id="b7749-103">Удаляет связанную службу из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="b7749-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="b7749-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7749-104">SYNTAX</span></span>

### <span data-ttu-id="b7749-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7749-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7749-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b7749-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7749-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7749-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7749-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7749-108">DESCRIPTION</span></span>
<span data-ttu-id="b7749-109">Командлет Remove-AzDataFactoryV2LinkedService Удаляет связанную службу из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="b7749-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="b7749-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7749-110">EXAMPLES</span></span>

### <span data-ttu-id="b7749-111">Пример 1: удаление связанной службы</span><span class="sxs-lookup"><span data-stu-id="b7749-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="b7749-112">Эта команда удаляет связанную службу с именем LinkedServiceTest из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b7749-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="b7749-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="b7749-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="b7749-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7749-114">PARAMETERS</span></span>

### <span data-ttu-id="b7749-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b7749-115">-DataFactoryName</span></span>
<span data-ttu-id="b7749-116">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="b7749-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b7749-117">Этот командлет удаляет связанную службу из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b7749-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b7749-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7749-118">-DefaultProfile</span></span>
<span data-ttu-id="b7749-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7749-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7749-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b7749-120">-Force</span></span>
<span data-ttu-id="b7749-121">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b7749-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b7749-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7749-122">-InputObject</span></span>
<span data-ttu-id="b7749-123">Указывает объект LinkedService, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b7749-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7749-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7749-124">-Name</span></span>
<span data-ttu-id="b7749-125">Указывает имя связанной службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b7749-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="b7749-126">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="b7749-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7749-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7749-127">-ResourceGroupName</span></span>
<span data-ttu-id="b7749-128">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b7749-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b7749-129">Этот командлет удаляет связанную службу из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b7749-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b7749-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7749-130">-ResourceId</span></span>
<span data-ttu-id="b7749-131">Идентификатор ресурса Azure связанной службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b7749-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="b7749-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7749-132">-Confirm</span></span>
<span data-ttu-id="b7749-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b7749-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7749-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7749-134">-WhatIf</span></span>
<span data-ttu-id="b7749-135">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="b7749-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b7749-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7749-136">CommonParameters</span></span>
<span data-ttu-id="b7749-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7749-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7749-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7749-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7749-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7749-139">INPUTS</span></span>

### <span data-ttu-id="b7749-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="b7749-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="b7749-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b7749-141">System.String</span></span>

## <span data-ttu-id="b7749-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7749-142">OUTPUTS</span></span>

### <span data-ttu-id="b7749-143">System. void</span><span class="sxs-lookup"><span data-stu-id="b7749-143">System.Void</span></span>

## <span data-ttu-id="b7749-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7749-144">NOTES</span></span>
<span data-ttu-id="b7749-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="b7749-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b7749-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7749-146">RELATED LINKS</span></span>

[<span data-ttu-id="b7749-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b7749-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="b7749-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="b7749-148">Set-AzDataFactoryV2LinkedService</span></span>]()

