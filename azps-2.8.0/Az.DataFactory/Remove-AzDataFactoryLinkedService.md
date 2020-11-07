---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a0e8a131b0a66c3887ecea7054a2f13b75e7f598
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721475"
---
# <span data-ttu-id="4ea6a-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="4ea6a-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="4ea6a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ea6a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea6a-103">Удаляет связанную службу из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="4ea6a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ea6a-104">SYNTAX</span></span>

### <span data-ttu-id="4ea6a-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ea6a-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ea6a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4ea6a-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ea6a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ea6a-107">DESCRIPTION</span></span>
<span data-ttu-id="4ea6a-108">Командлет **Remove-AzDataFactoryLinkedService** Удаляет связанную службу из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="4ea6a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ea6a-109">EXAMPLES</span></span>

### <span data-ttu-id="4ea6a-110">Пример 1: удаление связанной службы</span><span class="sxs-lookup"><span data-stu-id="4ea6a-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="4ea6a-111">Эта команда удаляет связанную службу с именем LinkedServiceTest из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="4ea6a-112">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="4ea6a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ea6a-113">PARAMETERS</span></span>

### <span data-ttu-id="4ea6a-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-114">-DataFactory</span></span>
<span data-ttu-id="4ea6a-115">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="4ea6a-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4ea6a-116">Этот командлет удаляет связанную службу из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ea6a-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4ea6a-117">-DataFactoryName</span></span>
<span data-ttu-id="4ea6a-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4ea6a-119">Этот командлет удаляет связанную службу из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ea6a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea6a-120">-DefaultProfile</span></span>
<span data-ttu-id="4ea6a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4ea6a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ea6a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4ea6a-122">-Force</span></span>
<span data-ttu-id="4ea6a-123">Указывает на то, что этот командлет удаляет связанную службу без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="4ea6a-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ea6a-124">-Name</span></span>
<span data-ttu-id="4ea6a-125">Указывает имя связанной службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ea6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ea6a-127">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4ea6a-128">Этот командлет удаляет связанную службу из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ea6a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ea6a-129">-Confirm</span></span>
<span data-ttu-id="4ea6a-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ea6a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea6a-131">-WhatIf</span></span>
<span data-ttu-id="4ea6a-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ea6a-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ea6a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea6a-134">CommonParameters</span></span>
<span data-ttu-id="4ea6a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ea6a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea6a-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ea6a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea6a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ea6a-137">INPUTS</span></span>

### <span data-ttu-id="4ea6a-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4ea6a-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="4ea6a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4ea6a-139">System.String</span></span>

## <span data-ttu-id="4ea6a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ea6a-140">OUTPUTS</span></span>

### <span data-ttu-id="4ea6a-141">System. void</span><span class="sxs-lookup"><span data-stu-id="4ea6a-141">System.Void</span></span>

## <span data-ttu-id="4ea6a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ea6a-142">NOTES</span></span>
* <span data-ttu-id="4ea6a-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="4ea6a-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4ea6a-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ea6a-144">RELATED LINKS</span></span>

[<span data-ttu-id="4ea6a-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="4ea6a-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="4ea6a-146">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="4ea6a-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


