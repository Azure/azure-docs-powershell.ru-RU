---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: c396455804f6bb501fa6439fceffb0eb45875516
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215068"
---
# <span data-ttu-id="1830e-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1830e-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="1830e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1830e-102">SYNOPSIS</span></span>
<span data-ttu-id="1830e-103">Удаляет фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="1830e-103">Removes a data factory.</span></span>

## <span data-ttu-id="1830e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1830e-104">SYNTAX</span></span>

### <span data-ttu-id="1830e-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1830e-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1830e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1830e-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1830e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1830e-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1830e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1830e-108">DESCRIPTION</span></span>
<span data-ttu-id="1830e-109">Этот Remove-AzDataFactoryV2 удаляет фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="1830e-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="1830e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1830e-110">EXAMPLES</span></span>

### <span data-ttu-id="1830e-111">Пример 1. Удаление фабрики данных</span><span class="sxs-lookup"><span data-stu-id="1830e-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="1830e-112">Эта команда удаляет фабрику данных с именем WikiADF из группы ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="1830e-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="1830e-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="1830e-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="1830e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1830e-114">PARAMETERS</span></span>

### <span data-ttu-id="1830e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1830e-115">-DefaultProfile</span></span>
<span data-ttu-id="1830e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1830e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1830e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1830e-117">-Force</span></span>
<span data-ttu-id="1830e-118">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1830e-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1830e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1830e-119">-InputObject</span></span>
<span data-ttu-id="1830e-120">Определяет удаляемый объект DataFactory.</span><span class="sxs-lookup"><span data-stu-id="1830e-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1830e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1830e-121">-Name</span></span>
<span data-ttu-id="1830e-122">Название фабрики данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1830e-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1830e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1830e-123">-ResourceGroupName</span></span>
<span data-ttu-id="1830e-124">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="1830e-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1830e-125">Этот cmdlet удаляет фабрику данных из группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1830e-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1830e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1830e-126">-ResourceId</span></span>
<span data-ttu-id="1830e-127">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="1830e-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1830e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1830e-128">-Confirm</span></span>
<span data-ttu-id="1830e-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1830e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1830e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1830e-130">-WhatIf</span></span>
<span data-ttu-id="1830e-131">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1830e-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1830e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1830e-132">CommonParameters</span></span>
<span data-ttu-id="1830e-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1830e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1830e-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1830e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1830e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1830e-135">INPUTS</span></span>

### <span data-ttu-id="1830e-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1830e-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="1830e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1830e-137">System.String</span></span>

## <span data-ttu-id="1830e-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1830e-138">OUTPUTS</span></span>

### <span data-ttu-id="1830e-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="1830e-139">System.Void</span></span>

## <span data-ttu-id="1830e-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1830e-140">NOTES</span></span>
<span data-ttu-id="1830e-141">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="1830e-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1830e-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1830e-142">RELATED LINKS</span></span>

[<span data-ttu-id="1830e-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1830e-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="1830e-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1830e-144">Set-AzDataFactoryV2</span></span>]()
