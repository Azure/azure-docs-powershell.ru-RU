---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 7c35821cbaf75a616ab1b9b8bbc2db9fc2a96794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568795"
---
# <span data-ttu-id="2a005-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2a005-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="2a005-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a005-102">SYNOPSIS</span></span>
<span data-ttu-id="2a005-103">Создание учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2a005-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a005-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a005-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tags] <Hashtable>] [-MaxDegreeOfParallelism <Int32>]
 [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a005-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a005-105">DESCRIPTION</span></span>
<span data-ttu-id="2a005-106">Командлет **New-AzureRmDataLakeAnalyticsAccount** создает учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2a005-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="2a005-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a005-107">EXAMPLES</span></span>

### <span data-ttu-id="2a005-108">Пример 1: создание учетной записи для Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="2a005-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="2a005-109">Эта команда создает учетную запись Data Lake Analytics с именем ContosoAdlAccount, которая использует хранилище данных ContosoAdlStore, в группе ресурсов с именем ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="2a005-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="2a005-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a005-110">PARAMETERS</span></span>

### <span data-ttu-id="2a005-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2a005-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="2a005-112">Указывает имя учетной записи Data Lake Store, которую следует задать в качестве источника данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a005-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="2a005-113">-Location</span><span class="sxs-lookup"><span data-stu-id="2a005-113">-Location</span></span>
<span data-ttu-id="2a005-114">Указывает место, на котором нужно создать учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2a005-114">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="2a005-115">В настоящее время поддерживается только East США 2.</span><span class="sxs-lookup"><span data-stu-id="2a005-115">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="2a005-116">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="2a005-116">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="2a005-117">Необязательная максимальная поддерживаемая степень параллелизма для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2a005-117">The optional maximum supported degree of parallelism for this account.</span></span> <span data-ttu-id="2a005-118">Если ничего не указано, по умолчанию используется значение 30.</span><span class="sxs-lookup"><span data-stu-id="2a005-118">If none is specified, defaults to 30</span></span>

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

### <span data-ttu-id="2a005-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="2a005-119">-MaxJobCount</span></span>
<span data-ttu-id="2a005-120">Необязательные максимальные поддерживаемые задания, выполняемые под учетной записью.</span><span class="sxs-lookup"><span data-stu-id="2a005-120">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="2a005-121">Если ничего не указано, по умолчанию используется значение 3</span><span class="sxs-lookup"><span data-stu-id="2a005-121">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="2a005-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a005-122">-Name</span></span>
<span data-ttu-id="2a005-123">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2a005-123">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="2a005-124">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="2a005-124">-QueryStoreRetention</span></span>
<span data-ttu-id="2a005-125">Необязательное количество дней хранения метаданных задания.</span><span class="sxs-lookup"><span data-stu-id="2a005-125">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="2a005-126">Если ничего не указано, по умолчанию используется значение 30 дней.</span><span class="sxs-lookup"><span data-stu-id="2a005-126">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="2a005-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a005-127">-ResourceGroupName</span></span>
<span data-ttu-id="2a005-128">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="2a005-128">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="2a005-129">Чтобы создать группу ресурсов, используйте командлет New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2a005-129">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="2a005-130">-Теги</span><span class="sxs-lookup"><span data-stu-id="2a005-130">-Tags</span></span>
<span data-ttu-id="2a005-131">Указывает пары "ключ-значение", которые можно использовать для идентификации учетной записи Data Lake Analytics среди других ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="2a005-131">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

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

### <span data-ttu-id="2a005-132">Уровень</span><span class="sxs-lookup"><span data-stu-id="2a005-132">-Tier</span></span>
<span data-ttu-id="2a005-133">Требуемый уровень обязательства для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2a005-133">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="2a005-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a005-134">-DefaultProfile</span></span>
<span data-ttu-id="2a005-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a005-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a005-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a005-136">CommonParameters</span></span>
<span data-ttu-id="2a005-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a005-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a005-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a005-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a005-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a005-139">INPUTS</span></span>

## <span data-ttu-id="2a005-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a005-140">OUTPUTS</span></span>

### <span data-ttu-id="2a005-141">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2a005-141">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="2a005-142">Сведения о вновь созданной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2a005-142">The details of the newly created account.</span></span>

## <span data-ttu-id="2a005-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a005-143">NOTES</span></span>

## <span data-ttu-id="2a005-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a005-144">RELATED LINKS</span></span>

[<span data-ttu-id="2a005-145">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2a005-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="2a005-146">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2a005-146">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="2a005-147">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2a005-147">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="2a005-148">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2a005-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


