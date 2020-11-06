---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 1636dd6b101a7639c84b0cd7c2659eac23a10b11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568205"
---
# <span data-ttu-id="8d833-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="8d833-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="8d833-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d833-102">SYNOPSIS</span></span>
<span data-ttu-id="8d833-103">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8d833-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d833-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d833-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d833-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d833-105">DESCRIPTION</span></span>
<span data-ttu-id="8d833-106">Командлет **New-AzureRmDataFactory** создает фабрику данных с указанным именем группы ресурсов и расположением.</span><span class="sxs-lookup"><span data-stu-id="8d833-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="8d833-107">Для выполнения этих операций выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="8d833-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="8d833-108">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8d833-108">Create a data factory.</span></span> 
- <span data-ttu-id="8d833-109">Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="8d833-109">Create linked services.</span></span> 
- <span data-ttu-id="8d833-110">Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="8d833-110">Create datasets.</span></span> 
- <span data-ttu-id="8d833-111">Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="8d833-111">Create a pipeline.</span></span>

## <span data-ttu-id="8d833-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d833-112">EXAMPLES</span></span>

### <span data-ttu-id="8d833-113">Пример 1: Создание фабрики данных</span><span class="sxs-lookup"><span data-stu-id="8d833-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="8d833-114">Эта команда создает фабрику данных с именем WikiADF в группе ресурсов с именем ADF в расположении WestUS.</span><span class="sxs-lookup"><span data-stu-id="8d833-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="8d833-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d833-115">PARAMETERS</span></span>

### <span data-ttu-id="8d833-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d833-116">-DefaultProfile</span></span>
<span data-ttu-id="8d833-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8d833-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d833-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8d833-118">-Force</span></span>
<span data-ttu-id="8d833-119">Указывает на то, что этот командлет заменяет существующую фабрику данных без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8d833-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8d833-120">-Location</span><span class="sxs-lookup"><span data-stu-id="8d833-120">-Location</span></span>
<span data-ttu-id="8d833-121">Задает расположение для фабрики данных, например WestUS или EastUS.</span><span class="sxs-lookup"><span data-stu-id="8d833-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="8d833-122">В настоящее время поддерживается только WestUS.</span><span class="sxs-lookup"><span data-stu-id="8d833-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="8d833-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8d833-123">-Name</span></span>
<span data-ttu-id="8d833-124">Указывает имя фабрики данных, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="8d833-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="8d833-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d833-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d833-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="8d833-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8d833-127">Этот командлет создает фабрику данных, принадлежащую группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="8d833-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d833-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="8d833-128">-Tag</span></span>
<span data-ttu-id="8d833-129">Теги фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8d833-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="8d833-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d833-130">-Confirm</span></span>
<span data-ttu-id="8d833-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8d833-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d833-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d833-132">-WhatIf</span></span>
<span data-ttu-id="8d833-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8d833-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d833-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8d833-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d833-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d833-135">CommonParameters</span></span>
<span data-ttu-id="8d833-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d833-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d833-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d833-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d833-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d833-138">INPUTS</span></span>

### <span data-ttu-id="8d833-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8d833-139">System.String</span></span>

### <span data-ttu-id="8d833-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8d833-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8d833-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d833-141">OUTPUTS</span></span>

### <span data-ttu-id="8d833-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8d833-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="8d833-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d833-143">NOTES</span></span>
* <span data-ttu-id="8d833-144">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="8d833-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8d833-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d833-145">RELATED LINKS</span></span>

[<span data-ttu-id="8d833-146">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="8d833-146">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="8d833-147">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="8d833-147">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


