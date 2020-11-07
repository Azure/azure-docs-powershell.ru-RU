---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: dc6315c16072a736c0db10df6615efb1696b78f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731151"
---
# <span data-ttu-id="6343e-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="6343e-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="6343e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6343e-102">SYNOPSIS</span></span>
<span data-ttu-id="6343e-103">Получение сведений о связанных службах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="6343e-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="6343e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6343e-104">SYNTAX</span></span>

### <span data-ttu-id="6343e-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6343e-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6343e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6343e-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6343e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6343e-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6343e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6343e-108">DESCRIPTION</span></span>
<span data-ttu-id="6343e-109">Командлет Get-AzDataFactoryV2LinkedService получает сведения о связанных службах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="6343e-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="6343e-110">Если указать имя связанной службы, этот командлет получает сведения о связанной службе.</span><span class="sxs-lookup"><span data-stu-id="6343e-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="6343e-111">Если имя не задано, этот командлет получает сведения обо всех связанных службах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="6343e-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="6343e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6343e-112">EXAMPLES</span></span>

### <span data-ttu-id="6343e-113">Пример 1: получение сведений обо всех связанных службах</span><span class="sxs-lookup"><span data-stu-id="6343e-113">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="6343e-114">Эта команда получает сведения обо всех связанных службах в фабрике данных с именем WikiADF, а затем передает связанные службы командлету Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="6343e-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6343e-115">Этот командлет Windows PowerShell форматирует результаты.</span><span class="sxs-lookup"><span data-stu-id="6343e-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="6343e-116">Чтобы получить дополнительные сведения, введите Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="6343e-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="6343e-117">Вы можете использовать один из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="6343e-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="6343e-118">Пример 2: получение сведений о конкретной связанной службе</span><span class="sxs-lookup"><span data-stu-id="6343e-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="6343e-119">Эта команда получает сведения о связанной службе с именем LinkedServiceCuratedWikiData в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="6343e-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="6343e-120">Пример 3: получение сведений о конкретной связанной службе путем указания параметра "фактическое значение"</span><span class="sxs-lookup"><span data-stu-id="6343e-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="6343e-121">Первая команда использует командлет Get-AzDataFactoryV2 для получения фабрики данных с именем ContosoFactory, а затем сохраняет ее в переменной $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="6343e-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="6343e-122">Вторая команда получает сведения о связанной службе для фабрики данных, хранящейся в $DataFactory, а затем передает эти данные командлету Format-Table с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="6343e-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6343e-123">Командлет Format-Table форматирует выходные данные в виде набора данных с указанными свойствами в качестве столбцов набора данных.</span><span class="sxs-lookup"><span data-stu-id="6343e-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="6343e-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6343e-124">PARAMETERS</span></span>

### <span data-ttu-id="6343e-125">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="6343e-125">-DataFactory</span></span>
<span data-ttu-id="6343e-126">Указывает объект PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="6343e-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="6343e-127">Этот командлет получает связанные службы, которые относятся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6343e-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6343e-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6343e-128">-DataFactoryName</span></span>
<span data-ttu-id="6343e-129">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6343e-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6343e-130">Этот командлет получает связанные службы, которые относятся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6343e-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6343e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6343e-131">-DefaultProfile</span></span>
<span data-ttu-id="6343e-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6343e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6343e-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6343e-133">-Name</span></span>
<span data-ttu-id="6343e-134">Указывает имя связанной службы, сведения о которой требуется получить.</span><span class="sxs-lookup"><span data-stu-id="6343e-134">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6343e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6343e-135">-ResourceGroupName</span></span>
<span data-ttu-id="6343e-136">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6343e-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6343e-137">Этот командлет получает связанные службы, которые относятся к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6343e-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6343e-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6343e-138">-ResourceId</span></span>
<span data-ttu-id="6343e-139">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="6343e-139">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6343e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6343e-140">CommonParameters</span></span>
<span data-ttu-id="6343e-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6343e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6343e-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6343e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6343e-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6343e-143">INPUTS</span></span>

### <span data-ttu-id="6343e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6343e-144">System.String</span></span>

### <span data-ttu-id="6343e-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6343e-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="6343e-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6343e-146">OUTPUTS</span></span>

### <span data-ttu-id="6343e-147">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="6343e-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="6343e-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="6343e-148">NOTES</span></span>
<span data-ttu-id="6343e-149">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="6343e-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6343e-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6343e-150">RELATED LINKS</span></span>

[<span data-ttu-id="6343e-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="6343e-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="6343e-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="6343e-152">Remove-AzDataFactoryV2LinkedService</span></span>]()
