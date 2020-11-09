---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313580"
---
# <span data-ttu-id="dc6c7-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="dc6c7-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="dc6c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc6c7-102">SYNOPSIS</span></span>
<span data-ttu-id="dc6c7-103">Создание учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="dc6c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc6c7-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc6c7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc6c7-105">DESCRIPTION</span></span>
<span data-ttu-id="dc6c7-106">Командлет **New-AzDataLakeAnalyticsAccount** создает учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="dc6c7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc6c7-107">EXAMPLES</span></span>

### <span data-ttu-id="dc6c7-108">Пример 1: создание учетной записи для Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="dc6c7-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="dc6c7-109">Эта команда создает учетную запись Data Lake Analytics с именем ContosoAdlAccount, которая использует хранилище данных ContosoAdlStore, в группе ресурсов с именем ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="dc6c7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc6c7-110">PARAMETERS</span></span>

### <span data-ttu-id="dc6c7-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dc6c7-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="dc6c7-112">Указывает имя учетной записи Data Lake Store, которую следует задать в качестве источника данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc6c7-113">-DefaultProfile</span></span>
<span data-ttu-id="dc6c7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dc6c7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc6c7-115">-Location</span><span class="sxs-lookup"><span data-stu-id="dc6c7-115">-Location</span></span>
<span data-ttu-id="dc6c7-116">Указывает место, на котором нужно создать учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="dc6c7-117">В настоящее время поддерживается только East США 2.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="dc6c7-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="dc6c7-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="dc6c7-119">Необязательная максимальная поддерживаемая единица измерения для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6c7-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="dc6c7-120">-MaxJobCount</span></span>
<span data-ttu-id="dc6c7-121">Необязательные максимальные поддерживаемые задания, выполняемые под учетной записью.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="dc6c7-122">Если ничего не указано, по умолчанию используется значение 3</span><span class="sxs-lookup"><span data-stu-id="dc6c7-122">If none is specified, defaults to 3</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6c7-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc6c7-123">-Name</span></span>
<span data-ttu-id="dc6c7-124">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6c7-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="dc6c7-125">-QueryStoreRetention</span></span>
<span data-ttu-id="dc6c7-126">Необязательное количество дней хранения метаданных задания.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="dc6c7-127">Если ничего не указано, по умолчанию используется значение 30 дней.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-127">If none specified, the default is 30 days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6c7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc6c7-128">-ResourceGroupName</span></span>
<span data-ttu-id="dc6c7-129">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="dc6c7-130">Чтобы создать группу ресурсов, используйте командлет New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6c7-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="dc6c7-131">-Tag</span></span>
<span data-ttu-id="dc6c7-132">Строка, словарь строк тегов, связанный с этой учетной записью</span><span class="sxs-lookup"><span data-stu-id="dc6c7-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6c7-133">Уровень</span><span class="sxs-lookup"><span data-stu-id="dc6c7-133">-Tier</span></span>
<span data-ttu-id="dc6c7-134">Требуемый уровень обязательства для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6c7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc6c7-135">CommonParameters</span></span>
<span data-ttu-id="dc6c7-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc6c7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc6c7-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc6c7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc6c7-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc6c7-138">INPUTS</span></span>

### <span data-ttu-id="dc6c7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dc6c7-139">System.String</span></span>

### <span data-ttu-id="dc6c7-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dc6c7-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dc6c7-141">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dc6c7-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dc6c7-142">System. Nullable "1 [[Microsoft. Azure. Management. Lake. Analytics. Models. TierType, Microsoft. Azure. Management. Lake. Analytics, Version = 3.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dc6c7-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="dc6c7-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc6c7-143">OUTPUTS</span></span>

### <span data-ttu-id="dc6c7-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="dc6c7-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="dc6c7-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc6c7-145">NOTES</span></span>

## <span data-ttu-id="dc6c7-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc6c7-146">RELATED LINKS</span></span>

[<span data-ttu-id="dc6c7-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="dc6c7-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="dc6c7-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="dc6c7-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="dc6c7-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="dc6c7-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="dc6c7-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="dc6c7-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)

