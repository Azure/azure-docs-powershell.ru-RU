---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 1155b7c0b294ac3bc5c2106b473ce1cf55a9ac82
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324523"
---
# <span data-ttu-id="b779a-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="b779a-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="b779a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b779a-102">SYNOPSIS</span></span>
<span data-ttu-id="b779a-103">Создает центр для фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="b779a-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="b779a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b779a-104">SYNTAX</span></span>

### <span data-ttu-id="b779a-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b779a-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b779a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b779a-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b779a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b779a-107">DESCRIPTION</span></span>
<span data-ttu-id="b779a-108">С помощью **cmdlet New-AzDataFactoryHub** в указанной группе ресурсов Azure и в фабрике данных Azure создается центр для фабрики данных Azure с указанным определением файла.</span><span class="sxs-lookup"><span data-stu-id="b779a-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="b779a-109">После создания концентратора вы можете использовать его для хранения связанных служб в группе и управления ими, а также добавлять в него конвейеры.</span><span class="sxs-lookup"><span data-stu-id="b779a-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="b779a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b779a-110">EXAMPLES</span></span>

### <span data-ttu-id="b779a-111">Пример 1. Создание концентратора</span><span class="sxs-lookup"><span data-stu-id="b779a-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="b779a-112">Эта команда создает концентратор ContosoDataHub в группе ресурсов ADFResourceGroup и фабрике данных ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="b779a-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="b779a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b779a-113">PARAMETERS</span></span>

### <span data-ttu-id="b779a-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b779a-114">-DataFactory</span></span>
<span data-ttu-id="b779a-115">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="b779a-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b779a-116">Этот cmdlet создает концентратор для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="b779a-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b779a-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b779a-117">-DataFactoryName</span></span>
<span data-ttu-id="b779a-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="b779a-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b779a-119">Этот cmdlet создает концентратор для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="b779a-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b779a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b779a-120">-DefaultProfile</span></span>
<span data-ttu-id="b779a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b779a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b779a-122">-File</span><span class="sxs-lookup"><span data-stu-id="b779a-122">-File</span></span>
<span data-ttu-id="b779a-123">Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание концентратора.</span><span class="sxs-lookup"><span data-stu-id="b779a-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

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

### <span data-ttu-id="b779a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b779a-124">-Force</span></span>
<span data-ttu-id="b779a-125">Указывает на то, что этот cmdlet заменяет существующий концентратор без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b779a-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b779a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b779a-126">-Name</span></span>
<span data-ttu-id="b779a-127">Указывает имя концентратора, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="b779a-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="b779a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b779a-128">-ResourceGroupName</span></span>
<span data-ttu-id="b779a-129">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b779a-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b779a-130">Этот cmdlet создает концентратор, который принадлежит к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="b779a-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b779a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b779a-131">-Confirm</span></span>
<span data-ttu-id="b779a-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b779a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b779a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b779a-133">-WhatIf</span></span>
<span data-ttu-id="b779a-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b779a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b779a-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b779a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b779a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b779a-136">CommonParameters</span></span>
<span data-ttu-id="b779a-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b779a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b779a-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b779a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b779a-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b779a-139">INPUTS</span></span>

### <span data-ttu-id="b779a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b779a-140">System.String</span></span>

### <span data-ttu-id="b779a-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b779a-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="b779a-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b779a-142">OUTPUTS</span></span>

### <span data-ttu-id="b779a-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="b779a-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="b779a-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b779a-144">NOTES</span></span>
* <span data-ttu-id="b779a-145">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="b779a-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b779a-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b779a-146">RELATED LINKS</span></span>

[<span data-ttu-id="b779a-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="b779a-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="b779a-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="b779a-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


