---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 91e1bb556f2464f535e64a870b5491fceb9eac4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971267"
---
# <span data-ttu-id="36ff7-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="36ff7-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="36ff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="36ff7-103">Создает центр для фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="36ff7-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="36ff7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36ff7-104">SYNTAX</span></span>

### <span data-ttu-id="36ff7-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36ff7-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36ff7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="36ff7-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ff7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36ff7-107">DESCRIPTION</span></span>
<span data-ttu-id="36ff7-108">С помощью **cmdlet New-AzDataFactoryHub** в указанной группе ресурсов Azure и в фабрике данных Azure создается центр для фабрики данных Azure с указанным определением файла.</span><span class="sxs-lookup"><span data-stu-id="36ff7-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="36ff7-109">После создания концентратора вы можете использовать его для хранения связанных служб в группе и управления ими, а также добавлять в него конвейеры.</span><span class="sxs-lookup"><span data-stu-id="36ff7-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="36ff7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36ff7-110">EXAMPLES</span></span>

### <span data-ttu-id="36ff7-111">Пример 1. Создание концентратора</span><span class="sxs-lookup"><span data-stu-id="36ff7-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="36ff7-112">Эта команда создает концентратор ContosoDataHub в группе ресурсов ADFResourceGroup и фабрике данных ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="36ff7-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="36ff7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36ff7-113">PARAMETERS</span></span>

### <span data-ttu-id="36ff7-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="36ff7-114">-DataFactory</span></span>
<span data-ttu-id="36ff7-115">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="36ff7-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="36ff7-116">Этот cmdlet создает концентратор для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="36ff7-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ff7-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="36ff7-117">-DataFactoryName</span></span>
<span data-ttu-id="36ff7-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="36ff7-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="36ff7-119">Этот cmdlet создает концентратор для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="36ff7-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="36ff7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ff7-120">-DefaultProfile</span></span>
<span data-ttu-id="36ff7-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="36ff7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36ff7-122">-File</span><span class="sxs-lookup"><span data-stu-id="36ff7-122">-File</span></span>
<span data-ttu-id="36ff7-123">Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание концентратора.</span><span class="sxs-lookup"><span data-stu-id="36ff7-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ff7-124">-Force</span><span class="sxs-lookup"><span data-stu-id="36ff7-124">-Force</span></span>
<span data-ttu-id="36ff7-125">Указывает на то, что этот cmdlet заменяет существующий концентратор без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="36ff7-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="36ff7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="36ff7-126">-Name</span></span>
<span data-ttu-id="36ff7-127">Указывает имя концентратора, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="36ff7-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="36ff7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ff7-128">-ResourceGroupName</span></span>
<span data-ttu-id="36ff7-129">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="36ff7-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="36ff7-130">Этот cmdlet создает центр, принадлежащий группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="36ff7-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="36ff7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36ff7-131">-Confirm</span></span>
<span data-ttu-id="36ff7-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="36ff7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ff7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ff7-133">-WhatIf</span></span>
<span data-ttu-id="36ff7-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36ff7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36ff7-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="36ff7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ff7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ff7-136">CommonParameters</span></span>
<span data-ttu-id="36ff7-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36ff7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ff7-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ff7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ff7-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36ff7-139">INPUTS</span></span>

### <span data-ttu-id="36ff7-140">System.String</span><span class="sxs-lookup"><span data-stu-id="36ff7-140">System.String</span></span>

### <span data-ttu-id="36ff7-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="36ff7-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="36ff7-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36ff7-142">OUTPUTS</span></span>

### <span data-ttu-id="36ff7-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="36ff7-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="36ff7-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36ff7-144">NOTES</span></span>
* <span data-ttu-id="36ff7-145">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="36ff7-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="36ff7-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36ff7-146">RELATED LINKS</span></span>

[<span data-ttu-id="36ff7-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="36ff7-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="36ff7-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="36ff7-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


