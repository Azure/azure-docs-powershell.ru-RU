---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 2a762bb115132f97dd31cf14f9f13d7c6cf5ef70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065008"
---
# <span data-ttu-id="10b71-101">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="10b71-101">Set-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="10b71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10b71-102">SYNOPSIS</span></span>
<span data-ttu-id="10b71-103">Изменение учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="10b71-103">Modifies a Data Lake Analytics account.</span></span>

## <span data-ttu-id="10b71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10b71-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10b71-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10b71-105">DESCRIPTION</span></span>
<span data-ttu-id="10b71-106">Командлет **Set-AzDataLakeAnalyticsAccount** изменяет учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="10b71-106">The **Set-AzDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="10b71-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10b71-107">EXAMPLES</span></span>

### <span data-ttu-id="10b71-108">Пример 1: изменение источника данных для учетной записи</span><span class="sxs-lookup"><span data-stu-id="10b71-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="10b71-109">Эта команда изменяет источник данных по умолчанию и свойство Tags для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="10b71-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="10b71-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10b71-110">PARAMETERS</span></span>

### <span data-ttu-id="10b71-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="10b71-111">-AllowAzureIpState</span></span>
<span data-ttu-id="10b71-112">При необходимости разрешите или запретите в Azure IP-адреса, которые поступают через брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="10b71-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10b71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b71-113">-DefaultProfile</span></span>
<span data-ttu-id="10b71-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="10b71-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10b71-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="10b71-115">-FirewallState</span></span>
<span data-ttu-id="10b71-116">При необходимости включите или отключите существующие правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="10b71-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10b71-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="10b71-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="10b71-118">Необязательная максимальная поддерживаемая единица измерения для обновления учетной записи.</span><span class="sxs-lookup"><span data-stu-id="10b71-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="10b71-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="10b71-119">-MaxJobCount</span></span>
<span data-ttu-id="10b71-120">Необязательные максимальные поддерживаемые задания, выполняемые под учетной записью, которые должны быть установлены в течение заданного времени.</span><span class="sxs-lookup"><span data-stu-id="10b71-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="10b71-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="10b71-121">-Name</span></span>
<span data-ttu-id="10b71-122">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="10b71-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="10b71-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="10b71-123">-QueryStoreRetention</span></span>
<span data-ttu-id="10b71-124">Необязательное количество дней, в течение которых хранятся метаданные задания для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="10b71-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="10b71-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10b71-125">-ResourceGroupName</span></span>
<span data-ttu-id="10b71-126">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="10b71-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10b71-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="10b71-127">-Tag</span></span>
<span data-ttu-id="10b71-128">Строковый словарь тегов, связанных с этой учетной записью, который должен заменить текущий набор тегов.</span><span class="sxs-lookup"><span data-stu-id="10b71-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10b71-129">Уровень</span><span class="sxs-lookup"><span data-stu-id="10b71-129">-Tier</span></span>
<span data-ttu-id="10b71-130">Требуемый уровень обязательства для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="10b71-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="10b71-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b71-131">CommonParameters</span></span>
<span data-ttu-id="10b71-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10b71-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b71-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b71-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b71-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10b71-134">INPUTS</span></span>

### <span data-ttu-id="10b71-135">System. String</span><span class="sxs-lookup"><span data-stu-id="10b71-135">System.String</span></span>

### <span data-ttu-id="10b71-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="10b71-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="10b71-137">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="10b71-137">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="10b71-138">System. Nullable "1 [[Microsoft. Azure. Management. Lake. Analytics. Models. TierType, Microsoft. Azure. Management. Lake. Analytics, Version = 3.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="10b71-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="10b71-139">System. Nullable "1 [[Microsoft. Azure. Management. Lake. Analytics. Models. FirewallState, Microsoft. Azure. Management. Lake. Analytics, Version = 3.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="10b71-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="10b71-140">System. Nullable "1 [[Microsoft. Azure. Management. Lake. Analytics. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. Lake. Analytics, Version = 3.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="10b71-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="10b71-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10b71-141">OUTPUTS</span></span>

### <span data-ttu-id="10b71-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="10b71-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="10b71-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="10b71-143">NOTES</span></span>

## <span data-ttu-id="10b71-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10b71-144">RELATED LINKS</span></span>

[<span data-ttu-id="10b71-145">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="10b71-145">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="10b71-146">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="10b71-146">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="10b71-147">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="10b71-147">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="10b71-148">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="10b71-148">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


