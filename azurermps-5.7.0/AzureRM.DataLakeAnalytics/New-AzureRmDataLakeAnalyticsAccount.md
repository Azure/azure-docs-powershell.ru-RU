---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 36bf1bbfeb0c44189f5eeeaa0988d0314980e48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561855"
---
# <span data-ttu-id="641d6-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="641d6-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="641d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="641d6-102">SYNOPSIS</span></span>
<span data-ttu-id="641d6-103">Создание учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="641d6-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="641d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="641d6-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="641d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="641d6-105">DESCRIPTION</span></span>
<span data-ttu-id="641d6-106">Командлет **New-AzureRmDataLakeAnalyticsAccount** создает учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="641d6-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="641d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="641d6-107">EXAMPLES</span></span>

### <span data-ttu-id="641d6-108">Пример 1: создание учетной записи для Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="641d6-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="641d6-109">Эта команда создает учетную запись Data Lake Analytics с именем ContosoAdlAccount, которая использует хранилище данных ContosoAdlStore, в группе ресурсов с именем ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="641d6-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="641d6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="641d6-110">PARAMETERS</span></span>

### <span data-ttu-id="641d6-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="641d6-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="641d6-112">Указывает имя учетной записи Data Lake Store, которую следует задать в качестве источника данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="641d6-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="641d6-113">-DefaultProfile</span></span>
<span data-ttu-id="641d6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="641d6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="641d6-115">-Location</span><span class="sxs-lookup"><span data-stu-id="641d6-115">-Location</span></span>
<span data-ttu-id="641d6-116">Указывает место, на котором нужно создать учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="641d6-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="641d6-117">В настоящее время поддерживается только East США 2.</span><span class="sxs-lookup"><span data-stu-id="641d6-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641d6-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="641d6-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="641d6-119">Необязательная максимальная поддерживаемая единица измерения для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="641d6-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641d6-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="641d6-120">-MaxJobCount</span></span>
<span data-ttu-id="641d6-121">Необязательные максимальные поддерживаемые задания, выполняемые под учетной записью.</span><span class="sxs-lookup"><span data-stu-id="641d6-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="641d6-122">Если ничего не указано, по умолчанию используется значение 3</span><span class="sxs-lookup"><span data-stu-id="641d6-122">If none is specified, defaults to 3</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641d6-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="641d6-123">-Name</span></span>
<span data-ttu-id="641d6-124">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="641d6-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641d6-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="641d6-125">-QueryStoreRetention</span></span>
<span data-ttu-id="641d6-126">Необязательное количество дней хранения метаданных задания.</span><span class="sxs-lookup"><span data-stu-id="641d6-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="641d6-127">Если ничего не указано, по умолчанию используется значение 30 дней.</span><span class="sxs-lookup"><span data-stu-id="641d6-127">If none specified, the default is 30 days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641d6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="641d6-128">-ResourceGroupName</span></span>
<span data-ttu-id="641d6-129">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="641d6-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="641d6-130">Чтобы создать группу ресурсов, используйте командлет New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="641d6-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641d6-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="641d6-131">-Tag</span></span>
<span data-ttu-id="641d6-132">Строка, словарь строк тегов, связанный с этой учетной записью</span><span class="sxs-lookup"><span data-stu-id="641d6-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641d6-133">Уровень</span><span class="sxs-lookup"><span data-stu-id="641d6-133">-Tier</span></span>
<span data-ttu-id="641d6-134">Требуемый уровень обязательства для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="641d6-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="641d6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="641d6-135">CommonParameters</span></span>
<span data-ttu-id="641d6-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="641d6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="641d6-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="641d6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="641d6-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="641d6-138">INPUTS</span></span>

### <span data-ttu-id="641d6-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="641d6-139">None</span></span>
<span data-ttu-id="641d6-140">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="641d6-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="641d6-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="641d6-141">OUTPUTS</span></span>

### <span data-ttu-id="641d6-142">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="641d6-142">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="641d6-143">Сведения о вновь созданной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="641d6-143">The details of the newly created account.</span></span>

## <span data-ttu-id="641d6-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="641d6-144">NOTES</span></span>

## <span data-ttu-id="641d6-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="641d6-145">RELATED LINKS</span></span>

[<span data-ttu-id="641d6-146">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="641d6-146">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="641d6-147">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="641d6-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="641d6-148">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="641d6-148">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="641d6-149">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="641d6-149">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


