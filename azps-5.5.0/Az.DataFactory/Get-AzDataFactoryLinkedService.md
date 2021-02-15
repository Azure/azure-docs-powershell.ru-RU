---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5f59dfeeb024b4a81554a700bdcebc9d7f39e80a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230660"
---
# <span data-ttu-id="8f773-101">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8f773-101">Get-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="8f773-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f773-102">SYNOPSIS</span></span>
<span data-ttu-id="8f773-103">Получает сведения о связанных службах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="8f773-103">Gets information about linked services in Azure Data Factory.</span></span>

## <span data-ttu-id="8f773-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8f773-104">SYNTAX</span></span>

### <span data-ttu-id="8f773-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f773-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f773-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8f773-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f773-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f773-107">DESCRIPTION</span></span>
<span data-ttu-id="8f773-108">Чтобы получить сведения о связанных службах в фабрике данных Azure, можно получить сведения о **cmdlet Get-AzDataFactoryLinkedService.**</span><span class="sxs-lookup"><span data-stu-id="8f773-108">The **Get-AzDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="8f773-109">Если указать имя связанной службы, этот cmdlet получит сведения о связанной службе.</span><span class="sxs-lookup"><span data-stu-id="8f773-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="8f773-110">Если имя не указано, этот cmdlet получает сведения обо всех связанных службах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="8f773-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="8f773-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8f773-111">EXAMPLES</span></span>

### <span data-ttu-id="8f773-112">Пример 1. Сведения обо всех связанных службах</span><span class="sxs-lookup"><span data-stu-id="8f773-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="8f773-113">Эта команда получает сведения обо всех связанных службах в фабрике данных WikiADF, а затем передает связанные службы в командлет Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="8f773-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8f773-114">Этот cmdlet formats the results (Форматирование результатов).</span><span class="sxs-lookup"><span data-stu-id="8f773-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="8f773-115">Для получения дополнительных сведений введите `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="8f773-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="8f773-116">Пример 2. Просмотр сведений о конкретной связанной службе</span><span class="sxs-lookup"><span data-stu-id="8f773-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="8f773-117">Эта команда получает сведения о связанной службе HDILinkedService в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8f773-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="8f773-118">Пример 3. Получите сведения об определенной связанной службе, указав параметр DataFactory</span><span class="sxs-lookup"><span data-stu-id="8f773-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="8f773-119">Первая команда использует Get-AzDataFactory для получения фабрики данных ContosoFactory, а затем сохраняет его в переменной $DataFactory данных.</span><span class="sxs-lookup"><span data-stu-id="8f773-119">The first command uses the Get-AzDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="8f773-120">Вторая команда получает сведения о связанной службе для фабрики данных, $DataFactory, а затем передает ее в командлет Format-Table с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="8f773-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8f773-121">**Format-Table** форматирование вывода в виде наборов данных с указанными свойствами в качестве столбцов для наборов данных.</span><span class="sxs-lookup"><span data-stu-id="8f773-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="8f773-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f773-122">PARAMETERS</span></span>

### <span data-ttu-id="8f773-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8f773-123">-DataFactory</span></span>
<span data-ttu-id="8f773-124">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="8f773-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8f773-125">Этот cmdlet получает связанные службы, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8f773-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8f773-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8f773-126">-DataFactoryName</span></span>
<span data-ttu-id="8f773-127">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8f773-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8f773-128">Этот cmdlet получает связанные службы, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8f773-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8f773-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f773-129">-DefaultProfile</span></span>
<span data-ttu-id="8f773-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8f773-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f773-131">-Name</span><span class="sxs-lookup"><span data-stu-id="8f773-131">-Name</span></span>
<span data-ttu-id="8f773-132">Указывает имя связанной службы, сведения о которой нужно получить.</span><span class="sxs-lookup"><span data-stu-id="8f773-132">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f773-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f773-133">-ResourceGroupName</span></span>
<span data-ttu-id="8f773-134">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="8f773-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8f773-135">Этот cmdlet получает связанные службы, которые относятся к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8f773-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8f773-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f773-136">CommonParameters</span></span>
<span data-ttu-id="8f773-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f773-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f773-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f773-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f773-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f773-139">INPUTS</span></span>

### <span data-ttu-id="8f773-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8f773-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="8f773-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8f773-141">System.String</span></span>

## <span data-ttu-id="8f773-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f773-142">OUTPUTS</span></span>

### <span data-ttu-id="8f773-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="8f773-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="8f773-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8f773-144">NOTES</span></span>
* <span data-ttu-id="8f773-145">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="8f773-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8f773-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f773-146">RELATED LINKS</span></span>

[<span data-ttu-id="8f773-147">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8f773-147">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)

[<span data-ttu-id="8f773-148">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8f773-148">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


