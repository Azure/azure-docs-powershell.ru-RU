---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: c13fdf46dff4ba0b62a8009bad7c4790507b2561
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975011"
---
# <span data-ttu-id="5bf3c-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="5bf3c-101">New-AzDataFactory</span></span>

## <span data-ttu-id="5bf3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bf3c-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf3c-103">Создает фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-103">Creates a data factory.</span></span>

## <span data-ttu-id="5bf3c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5bf3c-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bf3c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bf3c-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf3c-106">С **помощью cmdlet New-AzDataFactory** создается фабрика данных с указанным именем и расположением группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="5bf3c-107">Выполните эти действия в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="5bf3c-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="5bf3c-108">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-108">Create a data factory.</span></span> 
- <span data-ttu-id="5bf3c-109">Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-109">Create linked services.</span></span> 
- <span data-ttu-id="5bf3c-110">Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-110">Create datasets.</span></span> 
- <span data-ttu-id="5bf3c-111">Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-111">Create a pipeline.</span></span>

## <span data-ttu-id="5bf3c-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5bf3c-112">EXAMPLES</span></span>

### <span data-ttu-id="5bf3c-113">Пример 1. Создание фабрики данных</span><span class="sxs-lookup"><span data-stu-id="5bf3c-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="5bf3c-114">Эта команда создает фабрику данных с именем WikiADF в группе ресурсов ADF в расположении WestUS.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="5bf3c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bf3c-115">PARAMETERS</span></span>

### <span data-ttu-id="5bf3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf3c-116">-DefaultProfile</span></span>
<span data-ttu-id="5bf3c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5bf3c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bf3c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5bf3c-118">-Force</span></span>
<span data-ttu-id="5bf3c-119">Указывает на то, что этот cmdlet заменяет существующую фабрику данных, не запросив подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="5bf3c-120">-Location</span><span class="sxs-lookup"><span data-stu-id="5bf3c-120">-Location</span></span>
<span data-ttu-id="5bf3c-121">Определяет расположение фабрики данных, например WestUS или EastUS.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="5bf3c-122">В настоящее время поддерживается только westUS.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-122">Only WestUS is currently supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf3c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5bf3c-123">-Name</span></span>
<span data-ttu-id="5bf3c-124">Название фабрики данных, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-124">Specifies the name of the data factory to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf3c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf3c-125">-ResourceGroupName</span></span>
<span data-ttu-id="5bf3c-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5bf3c-127">Этот cmdlet создает фабрику данных, которая принадлежит к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf3c-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="5bf3c-128">-Tag</span></span>
<span data-ttu-id="5bf3c-129">Теги фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-129">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf3c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bf3c-130">-Confirm</span></span>
<span data-ttu-id="5bf3c-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf3c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf3c-132">-WhatIf</span></span>
<span data-ttu-id="5bf3c-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf3c-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf3c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf3c-135">CommonParameters</span></span>
<span data-ttu-id="5bf3c-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf3c-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bf3c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf3c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bf3c-138">INPUTS</span></span>

### <span data-ttu-id="5bf3c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5bf3c-139">System.String</span></span>

### <span data-ttu-id="5bf3c-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5bf3c-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5bf3c-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5bf3c-141">OUTPUTS</span></span>

### <span data-ttu-id="5bf3c-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5bf3c-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="5bf3c-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5bf3c-143">NOTES</span></span>
* <span data-ttu-id="5bf3c-144">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="5bf3c-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5bf3c-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bf3c-145">RELATED LINKS</span></span>

[<span data-ttu-id="5bf3c-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="5bf3c-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="5bf3c-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="5bf3c-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


