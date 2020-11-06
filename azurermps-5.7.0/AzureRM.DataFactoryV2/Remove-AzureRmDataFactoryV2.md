---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: 330bcf3622faa515a58ea8f1e087d1383b9f154a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557415"
---
# <span data-ttu-id="af541-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="af541-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="af541-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af541-102">SYNOPSIS</span></span>
<span data-ttu-id="af541-103">Удаление фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="af541-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af541-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af541-104">SYNTAX</span></span>

### <span data-ttu-id="af541-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af541-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af541-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="af541-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af541-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="af541-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af541-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af541-108">DESCRIPTION</span></span>
<span data-ttu-id="af541-109">Командлет Remove-AzureRmDataFactoryV2 удаляет фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="af541-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="af541-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af541-110">EXAMPLES</span></span>

### <span data-ttu-id="af541-111">Пример 1: удаление фабрики данных</span><span class="sxs-lookup"><span data-stu-id="af541-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="af541-112">Эта команда удаляет фабрику данных с именем WikiADF из группы ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="af541-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="af541-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="af541-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="af541-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af541-114">PARAMETERS</span></span>

### <span data-ttu-id="af541-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af541-115">-DefaultProfile</span></span>
<span data-ttu-id="af541-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af541-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af541-117">-Force</span><span class="sxs-lookup"><span data-stu-id="af541-117">-Force</span></span>
<span data-ttu-id="af541-118">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="af541-118">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af541-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af541-119">-InputObject</span></span>
<span data-ttu-id="af541-120">Указывает удаляемый объект факта.</span><span class="sxs-lookup"><span data-stu-id="af541-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af541-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af541-121">-Name</span></span>
<span data-ttu-id="af541-122">Указывает имя удаляемой фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="af541-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af541-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af541-123">-ResourceGroupName</span></span>
<span data-ttu-id="af541-124">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="af541-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="af541-125">Этот командлет удаляет фабрику данных из группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="af541-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af541-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af541-126">-ResourceId</span></span>
<span data-ttu-id="af541-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="af541-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af541-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af541-128">-Confirm</span></span>
<span data-ttu-id="af541-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="af541-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af541-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af541-130">-WhatIf</span></span>
<span data-ttu-id="af541-131">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="af541-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af541-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af541-132">CommonParameters</span></span>
<span data-ttu-id="af541-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af541-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af541-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af541-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af541-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af541-135">INPUTS</span></span>

### <span data-ttu-id="af541-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="af541-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="af541-137">System. String</span><span class="sxs-lookup"><span data-stu-id="af541-137">System.String</span></span>

## <span data-ttu-id="af541-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af541-138">OUTPUTS</span></span>

### <span data-ttu-id="af541-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="af541-139">System.Object</span></span>

## <span data-ttu-id="af541-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="af541-140">NOTES</span></span>
<span data-ttu-id="af541-141">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="af541-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="af541-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af541-142">RELATED LINKS</span></span>

[<span data-ttu-id="af541-143">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="af541-143">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="af541-144">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="af541-144">Set-AzureRmDataFactoryV2</span></span>]()
