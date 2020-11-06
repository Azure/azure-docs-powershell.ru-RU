---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: 9d7d3e3ae06d46b1ea3cb3b1e4e8db1944dc87e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566284"
---
# <span data-ttu-id="3d3a5-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3d3a5-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="3d3a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d3a5-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3a5-103">Удаление фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d3a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d3a5-104">SYNTAX</span></span>

### <span data-ttu-id="3d3a5-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d3a5-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d3a5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3d3a5-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d3a5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3d3a5-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d3a5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d3a5-108">DESCRIPTION</span></span>
<span data-ttu-id="3d3a5-109">Командлет Remove-AzureRmDataFactoryV2 удаляет фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="3d3a5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d3a5-110">EXAMPLES</span></span>

### <span data-ttu-id="3d3a5-111">Пример 1: удаление фабрики данных</span><span class="sxs-lookup"><span data-stu-id="3d3a5-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="3d3a5-112">Эта команда удаляет фабрику данных с именем WikiADF из группы ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="3d3a5-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="3d3a5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d3a5-114">PARAMETERS</span></span>

### <span data-ttu-id="3d3a5-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d3a5-115">-Confirm</span></span>
<span data-ttu-id="3d3a5-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d3a5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d3a5-117">-InputObject</span></span>
<span data-ttu-id="3d3a5-118">Указывает удаляемый объект факта.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-118">Specifies the DataFactory object to remove.</span></span>

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

### <span data-ttu-id="3d3a5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3d3a5-119">-Force</span></span>
<span data-ttu-id="3d3a5-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3d3a5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d3a5-121">-Name</span></span>
<span data-ttu-id="3d3a5-122">Указывает имя удаляемой фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-122">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="3d3a5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d3a5-123">-ResourceGroupName</span></span>
<span data-ttu-id="3d3a5-124">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3d3a5-125">Этот командлет удаляет фабрику данных из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3d3a5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d3a5-126">-ResourceId</span></span>
<span data-ttu-id="3d3a5-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3d3a5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d3a5-128">-WhatIf</span></span>
<span data-ttu-id="3d3a5-129">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3d3a5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3a5-130">-DefaultProfile</span></span>
<span data-ttu-id="3d3a5-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d3a5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3a5-132">CommonParameters</span></span>
<span data-ttu-id="3d3a5-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d3a5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3a5-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d3a5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3a5-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d3a5-135">INPUTS</span></span>

### <span data-ttu-id="3d3a5-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3d3a5-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="3d3a5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3d3a5-137">System.String</span></span>

## <span data-ttu-id="3d3a5-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d3a5-138">OUTPUTS</span></span>

### <span data-ttu-id="3d3a5-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="3d3a5-139">System.Object</span></span>

## <span data-ttu-id="3d3a5-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d3a5-140">NOTES</span></span>
<span data-ttu-id="3d3a5-141">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="3d3a5-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3d3a5-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d3a5-142">RELATED LINKS</span></span>

[<span data-ttu-id="3d3a5-143">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3d3a5-143">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="3d3a5-144">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3d3a5-144">Set-AzureRmDataFactoryV2</span></span>]()
