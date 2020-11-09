---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: c396455804f6bb501fa6439fceffb0eb45875516
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243674"
---
# <span data-ttu-id="6074a-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6074a-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="6074a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6074a-102">SYNOPSIS</span></span>
<span data-ttu-id="6074a-103">Удаление фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6074a-103">Removes a data factory.</span></span>

## <span data-ttu-id="6074a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6074a-104">SYNTAX</span></span>

### <span data-ttu-id="6074a-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6074a-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6074a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6074a-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6074a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6074a-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6074a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6074a-108">DESCRIPTION</span></span>
<span data-ttu-id="6074a-109">Командлет Remove-AzDataFactoryV2 удаляет фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="6074a-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="6074a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6074a-110">EXAMPLES</span></span>

### <span data-ttu-id="6074a-111">Пример 1: удаление фабрики данных</span><span class="sxs-lookup"><span data-stu-id="6074a-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="6074a-112">Эта команда удаляет фабрику данных с именем WikiADF из группы ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="6074a-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="6074a-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="6074a-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="6074a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6074a-114">PARAMETERS</span></span>

### <span data-ttu-id="6074a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6074a-115">-DefaultProfile</span></span>
<span data-ttu-id="6074a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6074a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6074a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6074a-117">-Force</span></span>
<span data-ttu-id="6074a-118">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6074a-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6074a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6074a-119">-InputObject</span></span>
<span data-ttu-id="6074a-120">Указывает удаляемый объект факта.</span><span class="sxs-lookup"><span data-stu-id="6074a-120">Specifies the DataFactory object to remove.</span></span>

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

### <span data-ttu-id="6074a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6074a-121">-Name</span></span>
<span data-ttu-id="6074a-122">Указывает имя удаляемой фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6074a-122">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="6074a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6074a-123">-ResourceGroupName</span></span>
<span data-ttu-id="6074a-124">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6074a-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6074a-125">Этот командлет удаляет фабрику данных из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6074a-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6074a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6074a-126">-ResourceId</span></span>
<span data-ttu-id="6074a-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="6074a-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6074a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6074a-128">-Confirm</span></span>
<span data-ttu-id="6074a-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6074a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6074a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6074a-130">-WhatIf</span></span>
<span data-ttu-id="6074a-131">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="6074a-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6074a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6074a-132">CommonParameters</span></span>
<span data-ttu-id="6074a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6074a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6074a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6074a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6074a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6074a-135">INPUTS</span></span>

### <span data-ttu-id="6074a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6074a-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="6074a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6074a-137">System.String</span></span>

## <span data-ttu-id="6074a-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6074a-138">OUTPUTS</span></span>

### <span data-ttu-id="6074a-139">System. void</span><span class="sxs-lookup"><span data-stu-id="6074a-139">System.Void</span></span>

## <span data-ttu-id="6074a-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="6074a-140">NOTES</span></span>
<span data-ttu-id="6074a-141">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="6074a-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6074a-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6074a-142">RELATED LINKS</span></span>

[<span data-ttu-id="6074a-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6074a-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="6074a-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6074a-144">Set-AzDataFactoryV2</span></span>]()