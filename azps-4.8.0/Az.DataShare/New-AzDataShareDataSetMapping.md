---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 5792aeb937f82d3d80c0a6a7aea11e1ad0497970
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079675"
---
# <span data-ttu-id="116b4-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="116b4-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="116b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="116b4-102">SYNOPSIS</span></span>
<span data-ttu-id="116b4-103">Создание сопоставления наборов данных для общего доступа к подписке.</span><span class="sxs-lookup"><span data-stu-id="116b4-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="116b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="116b4-104">SYNTAX</span></span>

### <span data-ttu-id="116b4-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="116b4-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="116b4-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="116b4-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="116b4-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="116b4-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="116b4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="116b4-108">DESCRIPTION</span></span>
<span data-ttu-id="116b4-109">Командлет **New-AzDataShareDataSetMapping** создает сопоставление набора данных между исходными наборами данных и учетной записью хранения приемников в подписке "общий доступ".</span><span class="sxs-lookup"><span data-stu-id="116b4-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="116b4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="116b4-110">EXAMPLES</span></span>

### <span data-ttu-id="116b4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="116b4-111">Example 1</span></span>
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

<span data-ttu-id="116b4-112">Эта команда создает сопоставление AdsDataSetMapping с учетной записью хранения AdsStorage для предоставления общего доступа к подписке, AdsShareSubscription в учетной записи общего доступа к данным WikiAdsAccount.</span><span class="sxs-lookup"><span data-stu-id="116b4-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="116b4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="116b4-113">PARAMETERS</span></span>

### <span data-ttu-id="116b4-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="116b4-114">-AccountName</span></span>
<span data-ttu-id="116b4-115">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="116b4-115">Azure data share account name</span></span>

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

### <span data-ttu-id="116b4-116">-Container</span><span class="sxs-lookup"><span data-stu-id="116b4-116">-Container</span></span>
<span data-ttu-id="116b4-117">Имя контейнера учетной записи службы хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="116b4-117">Azure storage account container name</span></span>

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

### <span data-ttu-id="116b4-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="116b4-118">-DataSetId</span></span>
<span data-ttu-id="116b4-119">Идентификатор множества данных потребителей</span><span class="sxs-lookup"><span data-stu-id="116b4-119">Consumer data set id</span></span>

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

### <span data-ttu-id="116b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116b4-120">-DefaultProfile</span></span>
<span data-ttu-id="116b4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="116b4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="116b4-122">-FilePath</span><span class="sxs-lookup"><span data-stu-id="116b4-122">-FilePath</span></span>
<span data-ttu-id="116b4-123">Путь к файлу хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="116b4-123">Azure storage file path</span></span>

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

### <span data-ttu-id="116b4-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="116b4-124">-FileSystem</span></span>
<span data-ttu-id="116b4-125">Имя файловой системы для Azure ADLS Gen2</span><span class="sxs-lookup"><span data-stu-id="116b4-125">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="116b4-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="116b4-126">-FolderPath</span></span>
<span data-ttu-id="116b4-127">Путь к папке хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="116b4-127">Azure storage folder path</span></span>

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

### <span data-ttu-id="116b4-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="116b4-128">-Name</span></span>
<span data-ttu-id="116b4-129">Имя сопоставления для наборов данных Azure</span><span class="sxs-lookup"><span data-stu-id="116b4-129">Azure data set mapping name</span></span>

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

### <span data-ttu-id="116b4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="116b4-130">-ResourceGroupName</span></span>
<span data-ttu-id="116b4-131">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="116b4-131">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="116b4-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="116b4-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="116b4-133">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="116b4-133">Azure data share subscription name</span></span>

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

### <span data-ttu-id="116b4-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="116b4-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="116b4-135">ResourceId для учетной записи хранения Azure</span><span class="sxs-lookup"><span data-stu-id="116b4-135">Azure Storage Account ResourceId</span></span>

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

### <span data-ttu-id="116b4-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="116b4-136">-Confirm</span></span>
<span data-ttu-id="116b4-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="116b4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="116b4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="116b4-138">-WhatIf</span></span>
<span data-ttu-id="116b4-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="116b4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="116b4-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="116b4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="116b4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116b4-141">CommonParameters</span></span>
<span data-ttu-id="116b4-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="116b4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116b4-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="116b4-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116b4-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="116b4-144">INPUTS</span></span>

### <span data-ttu-id="116b4-145">System. String</span><span class="sxs-lookup"><span data-stu-id="116b4-145">System.String</span></span>

## <span data-ttu-id="116b4-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="116b4-146">OUTPUTS</span></span>

### <span data-ttu-id="116b4-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="116b4-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="116b4-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="116b4-148">NOTES</span></span>

## <span data-ttu-id="116b4-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="116b4-149">RELATED LINKS</span></span>
