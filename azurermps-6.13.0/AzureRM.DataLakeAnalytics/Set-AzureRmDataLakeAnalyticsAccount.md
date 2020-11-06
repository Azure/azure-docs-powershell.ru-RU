---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 4bfbb25fa8b1e372175f741fd298384caa8050ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566510"
---
# <span data-ttu-id="a9024-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9024-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a9024-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9024-102">SYNOPSIS</span></span>
<span data-ttu-id="a9024-103">Изменение учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a9024-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9024-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9024-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9024-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9024-105">DESCRIPTION</span></span>
<span data-ttu-id="a9024-106">Командлет **Set-AzureRmDataLakeAnalyticsAccount** изменяет учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a9024-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a9024-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9024-107">EXAMPLES</span></span>

### <span data-ttu-id="a9024-108">Пример 1: изменение источника данных для учетной записи</span><span class="sxs-lookup"><span data-stu-id="a9024-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="a9024-109">Эта команда изменяет источник данных по умолчанию и свойство Tags для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a9024-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="a9024-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9024-110">PARAMETERS</span></span>

### <span data-ttu-id="a9024-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="a9024-111">-AllowAzureIpState</span></span>
<span data-ttu-id="a9024-112">При необходимости разрешите или запретите в Azure IP-адреса, которые поступают через брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="a9024-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="a9024-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9024-113">-DefaultProfile</span></span>
<span data-ttu-id="a9024-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a9024-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9024-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="a9024-115">-FirewallState</span></span>
<span data-ttu-id="a9024-116">При необходимости включите или отключите существующие правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a9024-116">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="a9024-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="a9024-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="a9024-118">Необязательная максимальная поддерживаемая единица измерения для обновления учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a9024-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="a9024-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="a9024-119">-MaxJobCount</span></span>
<span data-ttu-id="a9024-120">Необязательные максимальные поддерживаемые задания, выполняемые под учетной записью, которые должны быть установлены в течение заданного времени.</span><span class="sxs-lookup"><span data-stu-id="a9024-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="a9024-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a9024-121">-Name</span></span>
<span data-ttu-id="a9024-122">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a9024-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a9024-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="a9024-123">-QueryStoreRetention</span></span>
<span data-ttu-id="a9024-124">Необязательное количество дней, в течение которых хранятся метаданные задания для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a9024-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="a9024-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9024-125">-ResourceGroupName</span></span>
<span data-ttu-id="a9024-126">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a9024-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="a9024-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="a9024-127">-Tag</span></span>
<span data-ttu-id="a9024-128">Строковый словарь тегов, связанных с этой учетной записью, который должен заменить текущий набор тегов.</span><span class="sxs-lookup"><span data-stu-id="a9024-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

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

### <span data-ttu-id="a9024-129">Уровень</span><span class="sxs-lookup"><span data-stu-id="a9024-129">-Tier</span></span>
<span data-ttu-id="a9024-130">Требуемый уровень обязательства для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a9024-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="a9024-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9024-131">CommonParameters</span></span>
<span data-ttu-id="a9024-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9024-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9024-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9024-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9024-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9024-134">INPUTS</span></span>

### <span data-ttu-id="a9024-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a9024-135">System.String</span></span>

### <span data-ttu-id="a9024-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a9024-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a9024-137">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a9024-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a9024-138">System. Nullable "1 [[Microsoft. Azure. Management. Lake. Analytics. Models. TierType, Microsoft. Azure. Management. Lake. Analytics, Version = 3.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a9024-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a9024-139">System. Nullable "1 [[Microsoft. Azure. Management. Lake. Analytics. Models. FirewallState, Microsoft. Azure. Management. Lake. Analytics, Version = 3.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a9024-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a9024-140">System. Nullable "1 [[Microsoft. Azure. Management. Lake. Analytics. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. Lake. Analytics, Version = 3.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a9024-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a9024-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9024-141">OUTPUTS</span></span>

### <span data-ttu-id="a9024-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9024-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a9024-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9024-143">NOTES</span></span>

## <span data-ttu-id="a9024-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9024-144">RELATED LINKS</span></span>

[<span data-ttu-id="a9024-145">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9024-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a9024-146">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9024-146">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a9024-147">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9024-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a9024-148">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a9024-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


