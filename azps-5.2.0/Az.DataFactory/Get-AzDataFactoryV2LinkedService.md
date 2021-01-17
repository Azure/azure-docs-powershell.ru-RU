---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: ac3a45f9e150d65829a222e75e7072c6a2bdcd1e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393551"
---
# <span data-ttu-id="f5134-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f5134-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="f5134-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5134-102">SYNOPSIS</span></span>
<span data-ttu-id="f5134-103">Получает сведения о связанных службах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="f5134-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="f5134-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5134-104">SYNTAX</span></span>

### <span data-ttu-id="f5134-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5134-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5134-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f5134-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5134-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5134-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5134-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5134-108">DESCRIPTION</span></span>
<span data-ttu-id="f5134-109">Этот Get-AzDataFactoryV2LinkedService получает сведения о связанных службах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f5134-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="f5134-110">Если указать имя связанной службы, этот cmdlet получит сведения о связанной службе.</span><span class="sxs-lookup"><span data-stu-id="f5134-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="f5134-111">Если имя не указано, этот cmdlet получает сведения обо всех связанных службах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="f5134-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="f5134-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5134-112">EXAMPLES</span></span>

### <span data-ttu-id="f5134-113">Пример 1. Сведения обо всех связанных службах</span><span class="sxs-lookup"><span data-stu-id="f5134-113">Example 1: Get information about all linked services</span></span>
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

<span data-ttu-id="f5134-114">Эта команда получает сведения обо всех связанных службах в фабрике данных WikiADF, а затем передает связанные службы в командлет Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f5134-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f5134-115">Это Windows PowerShell форматирование результатов.</span><span class="sxs-lookup"><span data-stu-id="f5134-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="f5134-116">Для получения дополнительных сведений введите Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="f5134-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="f5134-117">Вы можете использовать один из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="f5134-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="f5134-118">Пример 2. Просмотр сведений о конкретной связанной службе</span><span class="sxs-lookup"><span data-stu-id="f5134-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="f5134-119">Эта команда получает сведения о связанной службе LinkedServiceCuratedWikiData в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f5134-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="f5134-120">Пример 3. Получите сведения об определенной связанной службе, указав параметр DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5134-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="f5134-121">Первая команда использует Get-AzDataFactoryV2 для получения фабрики данных ContosoFactory, а затем сохраняет его в переменной $DataFactory данных.</span><span class="sxs-lookup"><span data-stu-id="f5134-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="f5134-122">Вторая команда получает сведения о связанной службе для фабрики данных, $DataFactory, а затем передает ее в командлет Format-Table с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f5134-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f5134-123">Новый Format-Table форматирование выходных данных в виде наборов данных с указанными свойствами в качестве столбцов для наборов данных.</span><span class="sxs-lookup"><span data-stu-id="f5134-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="f5134-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5134-124">PARAMETERS</span></span>

### <span data-ttu-id="f5134-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5134-125">-DataFactory</span></span>
<span data-ttu-id="f5134-126">Указывает объект PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="f5134-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="f5134-127">Этот cmdlet получает связанные службы, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="f5134-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5134-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f5134-128">-DataFactoryName</span></span>
<span data-ttu-id="f5134-129">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f5134-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f5134-130">Этот cmdlet получает связанные службы, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="f5134-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5134-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5134-131">-DefaultProfile</span></span>
<span data-ttu-id="f5134-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5134-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5134-133">-Name</span><span class="sxs-lookup"><span data-stu-id="f5134-133">-Name</span></span>
<span data-ttu-id="f5134-134">Указывает имя связанной службы, сведения о которой нужно получить.</span><span class="sxs-lookup"><span data-stu-id="f5134-134">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="f5134-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5134-135">-ResourceGroupName</span></span>
<span data-ttu-id="f5134-136">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f5134-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f5134-137">Этот cmdlet получает связанные службы, которые относятся к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="f5134-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5134-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5134-138">-ResourceId</span></span>
<span data-ttu-id="f5134-139">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="f5134-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f5134-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5134-140">CommonParameters</span></span>
<span data-ttu-id="f5134-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5134-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5134-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5134-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5134-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5134-143">INPUTS</span></span>

### <span data-ttu-id="f5134-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f5134-144">System.String</span></span>

### <span data-ttu-id="f5134-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f5134-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f5134-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5134-146">OUTPUTS</span></span>

### <span data-ttu-id="f5134-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="f5134-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="f5134-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5134-148">NOTES</span></span>
<span data-ttu-id="f5134-149">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="f5134-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f5134-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5134-150">RELATED LINKS</span></span>

[<span data-ttu-id="f5134-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f5134-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="f5134-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="f5134-152">Remove-AzDataFactoryV2LinkedService</span></span>]()
