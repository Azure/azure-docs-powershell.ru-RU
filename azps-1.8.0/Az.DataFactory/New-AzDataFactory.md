---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 0ad9af6702af457dbdc1a934c8c9e9dd29fb1162
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900977"
---
# <span data-ttu-id="2277c-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="2277c-101">New-AzDataFactory</span></span>

## <span data-ttu-id="2277c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2277c-102">SYNOPSIS</span></span>
<span data-ttu-id="2277c-103">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="2277c-103">Creates a data factory.</span></span>

## <span data-ttu-id="2277c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2277c-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2277c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2277c-105">DESCRIPTION</span></span>
<span data-ttu-id="2277c-106">Командлет **New-AzDataFactory** создает фабрику данных с указанным именем группы ресурсов и расположением.</span><span class="sxs-lookup"><span data-stu-id="2277c-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="2277c-107">Для выполнения этих операций выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2277c-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="2277c-108">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="2277c-108">Create a data factory.</span></span> 
- <span data-ttu-id="2277c-109">Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="2277c-109">Create linked services.</span></span> 
- <span data-ttu-id="2277c-110">Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="2277c-110">Create datasets.</span></span> 
- <span data-ttu-id="2277c-111">Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="2277c-111">Create a pipeline.</span></span>

## <span data-ttu-id="2277c-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2277c-112">EXAMPLES</span></span>

### <span data-ttu-id="2277c-113">Пример 1: Создание фабрики данных</span><span class="sxs-lookup"><span data-stu-id="2277c-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="2277c-114">Эта команда создает фабрику данных с именем WikiADF в группе ресурсов с именем ADF в расположении WestUS.</span><span class="sxs-lookup"><span data-stu-id="2277c-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="2277c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2277c-115">PARAMETERS</span></span>

### <span data-ttu-id="2277c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2277c-116">-DefaultProfile</span></span>
<span data-ttu-id="2277c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2277c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2277c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2277c-118">-Force</span></span>
<span data-ttu-id="2277c-119">Указывает на то, что этот командлет заменяет существующую фабрику данных без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2277c-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="2277c-120">-Location</span><span class="sxs-lookup"><span data-stu-id="2277c-120">-Location</span></span>
<span data-ttu-id="2277c-121">Задает расположение для фабрики данных, например WestUS или EastUS.</span><span class="sxs-lookup"><span data-stu-id="2277c-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="2277c-122">В настоящее время поддерживается только WestUS.</span><span class="sxs-lookup"><span data-stu-id="2277c-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="2277c-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2277c-123">-Name</span></span>
<span data-ttu-id="2277c-124">Указывает имя фабрики данных, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="2277c-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="2277c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2277c-125">-ResourceGroupName</span></span>
<span data-ttu-id="2277c-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="2277c-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2277c-127">Этот командлет создает фабрику данных, принадлежащую группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2277c-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2277c-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="2277c-128">-Tag</span></span>
<span data-ttu-id="2277c-129">Теги фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="2277c-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="2277c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2277c-130">-Confirm</span></span>
<span data-ttu-id="2277c-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2277c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2277c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2277c-132">-WhatIf</span></span>
<span data-ttu-id="2277c-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2277c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2277c-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2277c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2277c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2277c-135">CommonParameters</span></span>
<span data-ttu-id="2277c-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2277c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2277c-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2277c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2277c-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2277c-138">INPUTS</span></span>

### <span data-ttu-id="2277c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2277c-139">System.String</span></span>

### <span data-ttu-id="2277c-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2277c-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2277c-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2277c-141">OUTPUTS</span></span>

### <span data-ttu-id="2277c-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2277c-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="2277c-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="2277c-143">NOTES</span></span>
* <span data-ttu-id="2277c-144">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="2277c-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2277c-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2277c-145">RELATED LINKS</span></span>

[<span data-ttu-id="2277c-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="2277c-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="2277c-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="2277c-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


