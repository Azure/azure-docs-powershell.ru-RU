---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 5dbf797ffabdf42b1d30d9d709ba6bb3153d8696
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420644"
---
# <span data-ttu-id="3201d-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="3201d-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="3201d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3201d-102">SYNOPSIS</span></span>
<span data-ttu-id="3201d-103">Добавляет наборы данных в обойму данных Azure.</span><span class="sxs-lookup"><span data-stu-id="3201d-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="3201d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3201d-104">SYNTAX</span></span>

### <span data-ttu-id="3201d-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3201d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3201d-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="3201d-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3201d-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="3201d-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3201d-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="3201d-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3201d-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3201d-109">DESCRIPTION</span></span>
<span data-ttu-id="3201d-110">С **его учетной** записью можно добавлять наборы данных в azure Share Data Share.</span><span class="sxs-lookup"><span data-stu-id="3201d-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="3201d-111">Вы можете добавлять наборы данных типа BLOB, ADLS Gen2 и ADLS Gen1.</span><span class="sxs-lookup"><span data-stu-id="3201d-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="3201d-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3201d-112">EXAMPLES</span></span>

### <span data-ttu-id="3201d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3201d-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="3201d-114">Эта команда добавляет набор данных AdsDataSet типа BLOB-контейнера для обмена данными Azure AdsShare.</span><span class="sxs-lookup"><span data-stu-id="3201d-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="3201d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3201d-115">PARAMETERS</span></span>

### <span data-ttu-id="3201d-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3201d-116">-AccountName</span></span>
<span data-ttu-id="3201d-117">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="3201d-117">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="3201d-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="3201d-119">Путь к папке ADLS -1 хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="3201d-119">Azure storage ADLS gen1 folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-120">-Container</span><span class="sxs-lookup"><span data-stu-id="3201d-120">-Container</span></span>
<span data-ttu-id="3201d-121">Имя контейнера учетной записи хранения Azure</span><span class="sxs-lookup"><span data-stu-id="3201d-121">Azure storage account container name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3201d-122">-DefaultProfile</span></span>
<span data-ttu-id="3201d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3201d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3201d-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="3201d-124">-FileName</span></span>
<span data-ttu-id="3201d-125">Имя файла ADLS-файла ADLS хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="3201d-125">Azure storage ADLS gen1 file name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="3201d-126">-FilePath</span></span>
<span data-ttu-id="3201d-127">Путь к файлу хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="3201d-127">Azure storage file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="3201d-128">-FileSystem</span></span>
<span data-ttu-id="3201d-129">Имя файловой системы Azure ADLS gen2</span><span class="sxs-lookup"><span data-stu-id="3201d-129">Azure ADLS gen2 file system name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="3201d-130">-FolderPath</span></span>
<span data-ttu-id="3201d-131">Путь к папке хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="3201d-131">Azure storage folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="3201d-132">-Name</span></span>
<span data-ttu-id="3201d-133">Имя набора данных Azure</span><span class="sxs-lookup"><span data-stu-id="3201d-133">Azure data set name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3201d-134">-ResourceGroupName</span></span>
<span data-ttu-id="3201d-135">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="3201d-135">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3201d-136">-ShareName</span></span>
<span data-ttu-id="3201d-137">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="3201d-137">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3201d-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="3201d-139">ResourceId учетной записи хранения Azure</span><span class="sxs-lookup"><span data-stu-id="3201d-139">Azure storage account resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3201d-140">-Confirm</span></span>
<span data-ttu-id="3201d-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3201d-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3201d-142">-WhatIf</span></span>
<span data-ttu-id="3201d-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3201d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3201d-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3201d-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3201d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3201d-145">CommonParameters</span></span>
<span data-ttu-id="3201d-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3201d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3201d-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3201d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3201d-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3201d-148">INPUTS</span></span>

### <span data-ttu-id="3201d-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3201d-149">System.String</span></span>

## <span data-ttu-id="3201d-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3201d-150">OUTPUTS</span></span>

### <span data-ttu-id="3201d-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="3201d-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="3201d-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3201d-152">NOTES</span></span>

## <span data-ttu-id="3201d-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3201d-153">RELATED LINKS</span></span>
