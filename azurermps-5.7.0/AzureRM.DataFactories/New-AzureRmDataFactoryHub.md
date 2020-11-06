---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
ms.openlocfilehash: 1891ab463b007b2e4a1502579f0d0e0a48779ca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566198"
---
# <span data-ttu-id="aa249-101">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="aa249-101">New-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="aa249-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa249-102">SYNOPSIS</span></span>
<span data-ttu-id="aa249-103">Создает центр для фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="aa249-103">Creates a hub for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa249-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa249-104">SYNTAX</span></span>

### <span data-ttu-id="aa249-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa249-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa249-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="aa249-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa249-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa249-107">DESCRIPTION</span></span>
<span data-ttu-id="aa249-108">Командлет **New-AzureRmDataFactoryHub** создает Hub для фабрики данных Azure в указанной группе ресурсов Azure и в указанной фабрике данных с указанным определением файла.</span><span class="sxs-lookup"><span data-stu-id="aa249-108">The **New-AzureRmDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="aa249-109">После того как вы создадите центр, вы можете использовать его для хранения и управления связанными службами в группе, а также добавлять конвейеры в этот центр.</span><span class="sxs-lookup"><span data-stu-id="aa249-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="aa249-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa249-110">EXAMPLES</span></span>

### <span data-ttu-id="aa249-111">Пример 1: создание концентратора</span><span class="sxs-lookup"><span data-stu-id="aa249-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="aa249-112">Эта команда создает концентратор с именем ContosoDataHub в группе ресурсов ADFResourceGroup и фабрика данных с именем ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="aa249-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="aa249-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa249-113">PARAMETERS</span></span>

### <span data-ttu-id="aa249-114">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="aa249-114">-DataFactory</span></span>
<span data-ttu-id="aa249-115">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="aa249-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="aa249-116">Этот командлет создает концентратор для фабрики данных, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="aa249-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa249-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="aa249-117">-DataFactoryName</span></span>
<span data-ttu-id="aa249-118">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="aa249-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="aa249-119">Этот командлет создает концентратор для фабрики данных, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="aa249-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa249-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa249-120">-DefaultProfile</span></span>
<span data-ttu-id="aa249-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aa249-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa249-122">-Файл</span><span class="sxs-lookup"><span data-stu-id="aa249-122">-File</span></span>
<span data-ttu-id="aa249-123">Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание концентратора.</span><span class="sxs-lookup"><span data-stu-id="aa249-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa249-124">-Force</span><span class="sxs-lookup"><span data-stu-id="aa249-124">-Force</span></span>
<span data-ttu-id="aa249-125">Указывает, что этот командлет заменяет существующий концентратор без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="aa249-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="aa249-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa249-126">-Name</span></span>
<span data-ttu-id="aa249-127">Указывает имя создаваемого концентратора.</span><span class="sxs-lookup"><span data-stu-id="aa249-127">Specifies the name of the hub to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa249-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa249-128">-ResourceGroupName</span></span>
<span data-ttu-id="aa249-129">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="aa249-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="aa249-130">Этот командлет создает концентратор, принадлежащий группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="aa249-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa249-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa249-131">-Confirm</span></span>
<span data-ttu-id="aa249-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa249-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa249-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa249-133">-WhatIf</span></span>
<span data-ttu-id="aa249-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa249-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa249-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa249-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa249-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa249-136">CommonParameters</span></span>
<span data-ttu-id="aa249-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa249-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa249-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa249-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa249-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa249-139">INPUTS</span></span>

### <span data-ttu-id="aa249-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="aa249-140">None</span></span>
<span data-ttu-id="aa249-141">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="aa249-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa249-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa249-142">OUTPUTS</span></span>

### <span data-ttu-id="aa249-143">Microsoft. Azure. Commands. Factoring. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="aa249-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="aa249-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa249-144">NOTES</span></span>
* <span data-ttu-id="aa249-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="aa249-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="aa249-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa249-146">RELATED LINKS</span></span>

[<span data-ttu-id="aa249-147">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="aa249-147">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="aa249-148">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="aa249-148">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)


