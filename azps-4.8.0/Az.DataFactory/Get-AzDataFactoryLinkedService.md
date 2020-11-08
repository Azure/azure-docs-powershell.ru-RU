---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5f59dfeeb024b4a81554a700bdcebc9d7f39e80a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242531"
---
# <span data-ttu-id="b56f7-101">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="b56f7-101">Get-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="b56f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b56f7-102">SYNOPSIS</span></span>
<span data-ttu-id="b56f7-103">Получение сведений о связанных службах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="b56f7-103">Gets information about linked services in Azure Data Factory.</span></span>

## <span data-ttu-id="b56f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b56f7-104">SYNTAX</span></span>

### <span data-ttu-id="b56f7-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b56f7-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b56f7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b56f7-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b56f7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b56f7-107">DESCRIPTION</span></span>
<span data-ttu-id="b56f7-108">Командлет **Get-AzDataFactoryLinkedService** получает сведения о связанных службах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="b56f7-108">The **Get-AzDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="b56f7-109">Если указать имя связанной службы, этот командлет получает сведения о связанной службе.</span><span class="sxs-lookup"><span data-stu-id="b56f7-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="b56f7-110">Если имя не задано, этот командлет получает сведения обо всех связанных службах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="b56f7-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="b56f7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b56f7-111">EXAMPLES</span></span>

### <span data-ttu-id="b56f7-112">Пример 1: получение сведений обо всех связанных службах</span><span class="sxs-lookup"><span data-stu-id="b56f7-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="b56f7-113">Эта команда получает сведения обо всех связанных службах в фабрике данных с именем WikiADF, а затем передает связанные службы командлету Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="b56f7-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b56f7-114">Этот командлет форматирует результаты.</span><span class="sxs-lookup"><span data-stu-id="b56f7-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="b56f7-115">Для получения дополнительных сведений введите `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="b56f7-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="b56f7-116">Пример 2: получение сведений о конкретной связанной службе</span><span class="sxs-lookup"><span data-stu-id="b56f7-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="b56f7-117">Эта команда получает сведения о связанной службе с именем HDILinkedService в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b56f7-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="b56f7-118">Пример 3: получение сведений о конкретной связанной службе путем указания параметра "фактическое значение"</span><span class="sxs-lookup"><span data-stu-id="b56f7-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="b56f7-119">Первая команда использует командлет Get-AzDataFactory для получения фабрики данных с именем ContosoFactory, а затем сохраняет ее в переменной $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="b56f7-119">The first command uses the Get-AzDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="b56f7-120">Вторая команда получает сведения о связанной службе для фабрики данных, хранящейся в $DataFactory, а затем передает эти данные командлету Format-Table с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="b56f7-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b56f7-121">**Format-Table** форматирует выходные данные в виде набора данных с указанными свойствами в качестве столбцов набора данных.</span><span class="sxs-lookup"><span data-stu-id="b56f7-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="b56f7-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b56f7-122">PARAMETERS</span></span>

### <span data-ttu-id="b56f7-123">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="b56f7-123">-DataFactory</span></span>
<span data-ttu-id="b56f7-124">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="b56f7-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b56f7-125">Этот командлет получает связанные службы, которые относятся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b56f7-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b56f7-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b56f7-126">-DataFactoryName</span></span>
<span data-ttu-id="b56f7-127">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="b56f7-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b56f7-128">Этот командлет получает связанные службы, которые относятся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b56f7-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b56f7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56f7-129">-DefaultProfile</span></span>
<span data-ttu-id="b56f7-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b56f7-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b56f7-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b56f7-131">-Name</span></span>
<span data-ttu-id="b56f7-132">Указывает имя связанной службы, сведения о которой требуется получить.</span><span class="sxs-lookup"><span data-stu-id="b56f7-132">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="b56f7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b56f7-133">-ResourceGroupName</span></span>
<span data-ttu-id="b56f7-134">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b56f7-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b56f7-135">Этот командлет получает связанные службы, которые относятся к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b56f7-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b56f7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56f7-136">CommonParameters</span></span>
<span data-ttu-id="b56f7-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b56f7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56f7-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b56f7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56f7-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b56f7-139">INPUTS</span></span>

### <span data-ttu-id="b56f7-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b56f7-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b56f7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b56f7-141">System.String</span></span>

## <span data-ttu-id="b56f7-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b56f7-142">OUTPUTS</span></span>

### <span data-ttu-id="b56f7-143">Microsoft. Azure. Commands. Factoring. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="b56f7-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="b56f7-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="b56f7-144">NOTES</span></span>
* <span data-ttu-id="b56f7-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="b56f7-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b56f7-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b56f7-146">RELATED LINKS</span></span>

[<span data-ttu-id="b56f7-147">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="b56f7-147">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)

[<span data-ttu-id="b56f7-148">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="b56f7-148">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


