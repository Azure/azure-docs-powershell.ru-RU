---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: bba4df58ed4046eeba562e3438119e1d5df40649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566274"
---
# <span data-ttu-id="94e57-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="94e57-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="94e57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94e57-102">SYNOPSIS</span></span>
<span data-ttu-id="94e57-103">Удаляет связанную службу из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="94e57-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94e57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94e57-104">SYNTAX</span></span>

### <span data-ttu-id="94e57-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94e57-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94e57-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="94e57-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e57-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="94e57-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94e57-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94e57-108">DESCRIPTION</span></span>
<span data-ttu-id="94e57-109">Командлет Remove-AzureRmDataFactoryV2LinkedService Удаляет связанную службу из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="94e57-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="94e57-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94e57-110">EXAMPLES</span></span>

### <span data-ttu-id="94e57-111">Пример 1: удаление связанной службы</span><span class="sxs-lookup"><span data-stu-id="94e57-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="94e57-112">Эта команда удаляет связанную службу с именем LinkedServiceTest из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="94e57-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="94e57-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="94e57-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="94e57-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94e57-114">PARAMETERS</span></span>

### <span data-ttu-id="94e57-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94e57-115">-Confirm</span></span>
<span data-ttu-id="94e57-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="94e57-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e57-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="94e57-117">-DataFactoryName</span></span>
<span data-ttu-id="94e57-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="94e57-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="94e57-119">Этот командлет удаляет связанную службу из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="94e57-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="94e57-120">-Force</span><span class="sxs-lookup"><span data-stu-id="94e57-120">-Force</span></span>
<span data-ttu-id="94e57-121">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="94e57-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="94e57-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94e57-122">-InputObject</span></span>
<span data-ttu-id="94e57-123">Указывает объект LinkedService, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="94e57-123">Specifies the LinkedService object to remove.</span></span>

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

### <span data-ttu-id="94e57-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="94e57-124">-Name</span></span>
<span data-ttu-id="94e57-125">Указывает имя связанной службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="94e57-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="94e57-126">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="94e57-126">Name of the linked service.</span></span>

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

### <span data-ttu-id="94e57-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94e57-127">-ResourceGroupName</span></span>
<span data-ttu-id="94e57-128">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="94e57-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="94e57-129">Этот командлет удаляет связанную службу из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="94e57-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


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

### <span data-ttu-id="94e57-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94e57-130">-ResourceId</span></span>
<span data-ttu-id="94e57-131">Идентификатор ресурса Azure связанной службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="94e57-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="94e57-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e57-132">-WhatIf</span></span>
<span data-ttu-id="94e57-133">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="94e57-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="94e57-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e57-134">-DefaultProfile</span></span>
<span data-ttu-id="94e57-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94e57-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94e57-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e57-136">CommonParameters</span></span>
<span data-ttu-id="94e57-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94e57-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e57-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94e57-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e57-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94e57-139">INPUTS</span></span>

### <span data-ttu-id="94e57-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="94e57-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="94e57-141">System. String</span><span class="sxs-lookup"><span data-stu-id="94e57-141">System.String</span></span>

## <span data-ttu-id="94e57-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94e57-142">OUTPUTS</span></span>

### <span data-ttu-id="94e57-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="94e57-143">System.Object</span></span>

## <span data-ttu-id="94e57-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="94e57-144">NOTES</span></span>
<span data-ttu-id="94e57-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="94e57-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="94e57-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94e57-146">RELATED LINKS</span></span>

[<span data-ttu-id="94e57-147">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="94e57-147">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="94e57-148">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="94e57-148">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

