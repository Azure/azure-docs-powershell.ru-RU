---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 5792aeb937f82d3d80c0a6a7aea11e1ad0497970
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222641"
---
# <span data-ttu-id="277a0-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="277a0-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="277a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="277a0-102">SYNOPSIS</span></span>
<span data-ttu-id="277a0-103">Создает сопоставление набора данных для подписки на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="277a0-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="277a0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="277a0-104">SYNTAX</span></span>

### <span data-ttu-id="277a0-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="277a0-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="277a0-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="277a0-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="277a0-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="277a0-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="277a0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="277a0-108">DESCRIPTION</span></span>
<span data-ttu-id="277a0-109">Командалет **New-AzDataShareDataSetMapping** создает сопоставление набора данных между исходными наборами данных и учетной записью хранения в подписке на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="277a0-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="277a0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="277a0-110">EXAMPLES</span></span>

### <span data-ttu-id="277a0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="277a0-111">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccoutName "WikiAdsAccount" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsDataSetMapping" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName        : AdsContainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : AdsStorage
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/AdsShareSubscription/dataSetMappings/AdsDataSetMapping
Name                 : AdsDataSetMapping
Type                 : Microsoft.DataShare/DataSetMappings
```

<span data-ttu-id="277a0-112">Эта команда создает сопоставление набора данных AdsDataSetMapping с учетной записью хранения AdsStorage для обмена подпиской AdsShareSubscription в учетной записи викиAdsAccount для обмена данными.</span><span class="sxs-lookup"><span data-stu-id="277a0-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="277a0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="277a0-113">PARAMETERS</span></span>

### <span data-ttu-id="277a0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="277a0-114">-AccountName</span></span>
<span data-ttu-id="277a0-115">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="277a0-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277a0-116">-Container</span><span class="sxs-lookup"><span data-stu-id="277a0-116">-Container</span></span>
<span data-ttu-id="277a0-117">Имя контейнера учетной записи хранения Azure</span><span class="sxs-lookup"><span data-stu-id="277a0-117">Azure storage account container name</span></span>

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

### <span data-ttu-id="277a0-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="277a0-118">-DataSetId</span></span>
<span data-ttu-id="277a0-119">Consumer data set id</span><span class="sxs-lookup"><span data-stu-id="277a0-119">Consumer data set id</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277a0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277a0-120">-DefaultProfile</span></span>
<span data-ttu-id="277a0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="277a0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="277a0-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="277a0-122">-FilePath</span></span>
<span data-ttu-id="277a0-123">Путь к файлу хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="277a0-123">Azure storage file path</span></span>

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

### <span data-ttu-id="277a0-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="277a0-124">-FileSystem</span></span>
<span data-ttu-id="277a0-125">Имя файловой системы Azure ADLS gen2</span><span class="sxs-lookup"><span data-stu-id="277a0-125">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="277a0-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="277a0-126">-FolderPath</span></span>
<span data-ttu-id="277a0-127">Путь к папке хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="277a0-127">Azure storage folder path</span></span>

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

### <span data-ttu-id="277a0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="277a0-128">-Name</span></span>
<span data-ttu-id="277a0-129">Имя сопоставления набора данных Azure</span><span class="sxs-lookup"><span data-stu-id="277a0-129">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277a0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="277a0-130">-ResourceGroupName</span></span>
<span data-ttu-id="277a0-131">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="277a0-131">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277a0-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="277a0-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="277a0-133">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="277a0-133">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="277a0-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="277a0-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="277a0-135">Azure Storage Account ResourceId</span><span class="sxs-lookup"><span data-stu-id="277a0-135">Azure Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="277a0-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="277a0-136">-Confirm</span></span>
<span data-ttu-id="277a0-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="277a0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="277a0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="277a0-138">-WhatIf</span></span>
<span data-ttu-id="277a0-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="277a0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="277a0-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="277a0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="277a0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277a0-141">CommonParameters</span></span>
<span data-ttu-id="277a0-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="277a0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277a0-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="277a0-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277a0-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="277a0-144">INPUTS</span></span>

### <span data-ttu-id="277a0-145">System.String</span><span class="sxs-lookup"><span data-stu-id="277a0-145">System.String</span></span>

## <span data-ttu-id="277a0-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="277a0-146">OUTPUTS</span></span>

### <span data-ttu-id="277a0-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="277a0-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="277a0-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="277a0-148">NOTES</span></span>

## <span data-ttu-id="277a0-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="277a0-149">RELATED LINKS</span></span>
