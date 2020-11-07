---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: a11588c5c8ce4e2a04b3ead13281ab64163bc5ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732310"
---
# <span data-ttu-id="f82c5-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f82c5-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="f82c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f82c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f82c5-103">Удаляет связанную службу из фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f82c5-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f82c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f82c5-104">SYNTAX</span></span>

### <span data-ttu-id="f82c5-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f82c5-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f82c5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f82c5-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f82c5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f82c5-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f82c5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f82c5-108">DESCRIPTION</span></span>
<span data-ttu-id="f82c5-109">Командлет Remove-AzureRmDataFactoryV2LinkedService Удаляет связанную службу из фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f82c5-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="f82c5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f82c5-110">EXAMPLES</span></span>

### <span data-ttu-id="f82c5-111">Пример 1: удаление связанной службы</span><span class="sxs-lookup"><span data-stu-id="f82c5-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="f82c5-112">Эта команда удаляет связанную службу с именем LinkedServiceTest из фабрики данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f82c5-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="f82c5-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="f82c5-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="f82c5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f82c5-114">PARAMETERS</span></span>

### <span data-ttu-id="f82c5-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f82c5-115">-DataFactoryName</span></span>
<span data-ttu-id="f82c5-116">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f82c5-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f82c5-117">Этот командлет удаляет связанную службу из фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f82c5-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f82c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f82c5-118">-DefaultProfile</span></span>
<span data-ttu-id="f82c5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f82c5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f82c5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f82c5-120">-Force</span></span>
<span data-ttu-id="f82c5-121">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f82c5-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f82c5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f82c5-122">-InputObject</span></span>
<span data-ttu-id="f82c5-123">Указывает объект LinkedService, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f82c5-123">Specifies the LinkedService object to remove.</span></span>

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

### <span data-ttu-id="f82c5-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f82c5-124">-Name</span></span>
<span data-ttu-id="f82c5-125">Указывает имя связанной службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f82c5-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="f82c5-126">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="f82c5-126">Name of the linked service.</span></span>

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

### <span data-ttu-id="f82c5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f82c5-127">-ResourceGroupName</span></span>
<span data-ttu-id="f82c5-128">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f82c5-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f82c5-129">Этот командлет удаляет связанную службу из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f82c5-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f82c5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f82c5-130">-ResourceId</span></span>
<span data-ttu-id="f82c5-131">Идентификатор ресурса Azure связанной службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f82c5-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="f82c5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f82c5-132">-Confirm</span></span>
<span data-ttu-id="f82c5-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f82c5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f82c5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f82c5-134">-WhatIf</span></span>
<span data-ttu-id="f82c5-135">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="f82c5-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f82c5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f82c5-136">CommonParameters</span></span>
<span data-ttu-id="f82c5-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f82c5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f82c5-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f82c5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f82c5-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f82c5-139">INPUTS</span></span>

### <span data-ttu-id="f82c5-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="f82c5-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="f82c5-141">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f82c5-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f82c5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f82c5-142">System.String</span></span>

## <span data-ttu-id="f82c5-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f82c5-143">OUTPUTS</span></span>

### <span data-ttu-id="f82c5-144">System. void</span><span class="sxs-lookup"><span data-stu-id="f82c5-144">System.Void</span></span>

## <span data-ttu-id="f82c5-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f82c5-145">NOTES</span></span>
<span data-ttu-id="f82c5-146">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="f82c5-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f82c5-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f82c5-147">RELATED LINKS</span></span>

[<span data-ttu-id="f82c5-148">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f82c5-148">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="f82c5-149">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f82c5-149">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

