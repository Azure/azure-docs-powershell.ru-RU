---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: bce1969ed951f196b1ff2c6d5bcc359ee68bc3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568605"
---
# <span data-ttu-id="0aca6-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0aca6-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="0aca6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0aca6-102">SYNOPSIS</span></span>
<span data-ttu-id="0aca6-103">Получение сведений о конвейерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="0aca6-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aca6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0aca6-104">SYNTAX</span></span>

### <span data-ttu-id="0aca6-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0aca6-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0aca6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0aca6-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0aca6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0aca6-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Pipeline -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0aca6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0aca6-108">DESCRIPTION</span></span>
<span data-ttu-id="0aca6-109">Командлет Get-AzureRmDataFactoryV2Pipeline получает сведения о конвейерах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="0aca6-109">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="0aca6-110">Если вы задаете имя конвейера, этот командлет получает сведения об этом конвейере.</span><span class="sxs-lookup"><span data-stu-id="0aca6-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="0aca6-111">Если имя не задано, этот командлет получает сведения обо всех конвейерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="0aca6-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="0aca6-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0aca6-112">EXAMPLES</span></span>

### <span data-ttu-id="0aca6-113">Пример 1: получение сведений обо всех каналах</span><span class="sxs-lookup"><span data-stu-id="0aca6-113">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="0aca6-114">Эта команда получает сведения обо всех конвейерах в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0aca6-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="0aca6-115">Вы можете использовать один из приведенных ниже примеров команд.</span><span class="sxs-lookup"><span data-stu-id="0aca6-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="0aca6-116">Во втором используется объект фактов в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="0aca6-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="0aca6-117">Пример 2: получение сведений о конкретном конвейере</span><span class="sxs-lookup"><span data-stu-id="0aca6-117">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="0aca6-118">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0aca6-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="0aca6-119">Команда передает эти данные командлету Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0aca6-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0aca6-120">Этот командлет Windows PowerShell форматирует результаты.</span><span class="sxs-lookup"><span data-stu-id="0aca6-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="0aca6-121">Чтобы получить дополнительные сведения, введите Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="0aca6-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="0aca6-122">Пример 3: получение свойств определенного конвейера</span><span class="sxs-lookup"><span data-stu-id="0aca6-122">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}
```

<span data-ttu-id="0aca6-123">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF, а затем использует стандартную нотацию для просмотра свойства Activitys, связанного с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="0aca6-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="0aca6-124">Пример 6: получение сведений о входных данных для первого действия</span><span class="sxs-lookup"><span data-stu-id="0aca6-124">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="0aca6-125">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF, а затем использует стандартную нотацию для просмотра свойства Activitys, связанного с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="0aca6-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="0aca6-126">Команда отображает свойство Inputs первого элемента массива "действия" с помощью командлета Format-List.</span><span class="sxs-lookup"><span data-stu-id="0aca6-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="0aca6-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0aca6-127">PARAMETERS</span></span>

### <span data-ttu-id="0aca6-128">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="0aca6-128">-DataFactory</span></span>
<span data-ttu-id="0aca6-129">Указывает объект PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="0aca6-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="0aca6-130">Этот командлет получает конвейеры, которые принадлежат к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0aca6-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0aca6-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0aca6-131">-DataFactoryName</span></span>
<span data-ttu-id="0aca6-132">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0aca6-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0aca6-133">Этот командлет получает конвейеры, которые принадлежат к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0aca6-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0aca6-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aca6-134">-DefaultProfile</span></span>
<span data-ttu-id="0aca6-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0aca6-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aca6-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0aca6-136">-Name</span></span>
<span data-ttu-id="0aca6-137">Указывает имя конвейера, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="0aca6-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aca6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aca6-138">-ResourceGroupName</span></span>
<span data-ttu-id="0aca6-139">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="0aca6-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0aca6-140">Этот командлет получает конвейеры, принадлежащие к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0aca6-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0aca6-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0aca6-141">-ResourceId</span></span>
<span data-ttu-id="0aca6-142">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="0aca6-142">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aca6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aca6-143">CommonParameters</span></span>
<span data-ttu-id="0aca6-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0aca6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aca6-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aca6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aca6-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0aca6-146">INPUTS</span></span>

### <span data-ttu-id="0aca6-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0aca6-147">System.String</span></span>
<span data-ttu-id="0aca6-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0aca6-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0aca6-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0aca6-149">OUTPUTS</span></span>

### <span data-ttu-id="0aca6-150">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0aca6-150">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0aca6-151">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="0aca6-151">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="0aca6-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="0aca6-152">NOTES</span></span>
<span data-ttu-id="0aca6-153">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="0aca6-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0aca6-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0aca6-154">RELATED LINKS</span></span>

[<span data-ttu-id="0aca6-155">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0aca6-155">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0aca6-156">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0aca6-156">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0aca6-157">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0aca6-157">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
