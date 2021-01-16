---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406588"
---
# <span data-ttu-id="637ef-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="637ef-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="637ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="637ef-102">SYNOPSIS</span></span>
<span data-ttu-id="637ef-103">Создает учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="637ef-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="637ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="637ef-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="637ef-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="637ef-105">DESCRIPTION</span></span>
<span data-ttu-id="637ef-106">Для создания учетной записи Azure Data Lake Analytics будет создаваться **cmdlet New-AzDataLakeAnalyticsAccount.**</span><span class="sxs-lookup"><span data-stu-id="637ef-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="637ef-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="637ef-107">EXAMPLES</span></span>

### <span data-ttu-id="637ef-108">Пример 1. Создание учетной записи Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="637ef-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="637ef-109">Эта команда создает учетную запись ContosoAdlAccount с хранилищем данных ContosoAdlStore в группе ресурсов ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="637ef-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="637ef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="637ef-110">PARAMETERS</span></span>

### <span data-ttu-id="637ef-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="637ef-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="637ef-112">Указывает имя учетной записи Магазина данных, которая будет задана в качестве источника данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="637ef-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="637ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="637ef-113">-DefaultProfile</span></span>
<span data-ttu-id="637ef-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="637ef-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="637ef-115">-Location</span><span class="sxs-lookup"><span data-stu-id="637ef-115">-Location</span></span>
<span data-ttu-id="637ef-116">Определяет расположение, в котором нужно создать учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="637ef-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="637ef-117">В настоящее время поддерживается только восток США 2.</span><span class="sxs-lookup"><span data-stu-id="637ef-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="637ef-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="637ef-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="637ef-119">Максимальные поддерживаемые аналитические единицы для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="637ef-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="637ef-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="637ef-120">-MaxJobCount</span></span>
<span data-ttu-id="637ef-121">Необязательное максимальное число поддерживаемых заданий, которые одновременно работают в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="637ef-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="637ef-122">Если значение не указано, по умолчанию установлено значение 3</span><span class="sxs-lookup"><span data-stu-id="637ef-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="637ef-123">-Name</span><span class="sxs-lookup"><span data-stu-id="637ef-123">-Name</span></span>
<span data-ttu-id="637ef-124">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="637ef-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="637ef-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="637ef-125">-QueryStoreRetention</span></span>
<span data-ttu-id="637ef-126">При желании можно хранить метаданные задания в течение дополнительного количества дней.</span><span class="sxs-lookup"><span data-stu-id="637ef-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="637ef-127">Если значение не задано, по умолчанию установлено значение 30 дней.</span><span class="sxs-lookup"><span data-stu-id="637ef-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="637ef-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="637ef-128">-ResourceGroupName</span></span>
<span data-ttu-id="637ef-129">Имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="637ef-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="637ef-130">Чтобы создать группу ресурсов, воспользуйтесь New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="637ef-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="637ef-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="637ef-131">-Tag</span></span>
<span data-ttu-id="637ef-132">Строковый строковый словарь тегов, связанный с этой учетной записью</span><span class="sxs-lookup"><span data-stu-id="637ef-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="637ef-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="637ef-133">-Tier</span></span>
<span data-ttu-id="637ef-134">Нужный уровень обязательств для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="637ef-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="637ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="637ef-135">CommonParameters</span></span>
<span data-ttu-id="637ef-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="637ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="637ef-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="637ef-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="637ef-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="637ef-138">INPUTS</span></span>

### <span data-ttu-id="637ef-139">System.String</span><span class="sxs-lookup"><span data-stu-id="637ef-139">System.String</span></span>

### <span data-ttu-id="637ef-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="637ef-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="637ef-141">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="637ef-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="637ef-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Analytics.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="637ef-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="637ef-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="637ef-143">OUTPUTS</span></span>

### <span data-ttu-id="637ef-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="637ef-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="637ef-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="637ef-145">NOTES</span></span>

## <span data-ttu-id="637ef-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="637ef-146">RELATED LINKS</span></span>

[<span data-ttu-id="637ef-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="637ef-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="637ef-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="637ef-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="637ef-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="637ef-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="637ef-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="637ef-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)

