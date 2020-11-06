---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 8a6553547bd75aeaaca8e96a85c9697d00ee65a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568925"
---
# <span data-ttu-id="ee167-101">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="ee167-101">Get-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="ee167-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee167-102">SYNOPSIS</span></span>
<span data-ttu-id="ee167-103">Получение сведений о связанных службах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ee167-103">Gets information about linked services in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee167-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee167-104">SYNTAX</span></span>

### <span data-ttu-id="ee167-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee167-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee167-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ee167-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee167-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee167-107">DESCRIPTION</span></span>
<span data-ttu-id="ee167-108">Командлет **Get-AzureRmDataFactoryLinkedService** получает сведения о связанных службах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ee167-108">The **Get-AzureRmDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="ee167-109">Если указать имя связанной службы, этот командлет получает сведения о связанной службе.</span><span class="sxs-lookup"><span data-stu-id="ee167-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="ee167-110">Если имя не задано, этот командлет получает сведения обо всех связанных службах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="ee167-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="ee167-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee167-111">EXAMPLES</span></span>

### <span data-ttu-id="ee167-112">Пример 1: получение сведений обо всех связанных службах</span><span class="sxs-lookup"><span data-stu-id="ee167-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="ee167-113">Эта команда получает сведения обо всех связанных службах в фабрике данных с именем WikiADF, а затем передает связанные службы командлету Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ee167-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ee167-114">Этот командлет форматирует результаты.</span><span class="sxs-lookup"><span data-stu-id="ee167-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="ee167-115">Для получения дополнительных сведений введите `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="ee167-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="ee167-116">Пример 2: получение сведений о конкретной связанной службе</span><span class="sxs-lookup"><span data-stu-id="ee167-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="ee167-117">Эта команда получает сведения о связанной службе с именем HDILinkedService в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ee167-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="ee167-118">Пример 3: получение сведений о конкретной связанной службе путем указания параметра "фактическое значение"</span><span class="sxs-lookup"><span data-stu-id="ee167-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzureRmDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="ee167-119">Первая команда использует командлет Get-AzureRmDataFactory для получения фабрики данных с именем ContosoFactory, а затем сохраняет ее в переменной $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="ee167-119">The first command uses the Get-AzureRmDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="ee167-120">Вторая команда получает сведения о связанной службе для фабрики данных, хранящейся в $DataFactory, а затем передает эти данные командлету Format-Table с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ee167-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ee167-121">**Format-Table** форматирует выходные данные в виде набора данных с указанными свойствами в качестве столбцов набора данных.</span><span class="sxs-lookup"><span data-stu-id="ee167-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="ee167-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee167-122">PARAMETERS</span></span>

### <span data-ttu-id="ee167-123">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="ee167-123">-DataFactory</span></span>
<span data-ttu-id="ee167-124">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="ee167-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ee167-125">Этот командлет получает связанные службы, которые относятся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ee167-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee167-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ee167-126">-DataFactoryName</span></span>
<span data-ttu-id="ee167-127">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ee167-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ee167-128">Этот командлет получает связанные службы, которые относятся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ee167-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee167-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee167-129">-DefaultProfile</span></span>
<span data-ttu-id="ee167-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ee167-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee167-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ee167-131">-Name</span></span>
<span data-ttu-id="ee167-132">Указывает имя связанной службы, сведения о которой требуется получить.</span><span class="sxs-lookup"><span data-stu-id="ee167-132">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="ee167-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee167-133">-ResourceGroupName</span></span>
<span data-ttu-id="ee167-134">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ee167-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ee167-135">Этот командлет получает связанные службы, которые относятся к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ee167-135">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee167-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee167-136">CommonParameters</span></span>
<span data-ttu-id="ee167-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee167-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee167-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee167-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee167-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee167-139">INPUTS</span></span>

### <span data-ttu-id="ee167-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ee167-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ee167-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ee167-141">System.String</span></span>

## <span data-ttu-id="ee167-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee167-142">OUTPUTS</span></span>

### <span data-ttu-id="ee167-143">Microsoft. Azure. Commands. Factoring. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="ee167-143">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="ee167-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee167-144">NOTES</span></span>
* <span data-ttu-id="ee167-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="ee167-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ee167-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee167-146">RELATED LINKS</span></span>

[<span data-ttu-id="ee167-147">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="ee167-147">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="ee167-148">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="ee167-148">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)


