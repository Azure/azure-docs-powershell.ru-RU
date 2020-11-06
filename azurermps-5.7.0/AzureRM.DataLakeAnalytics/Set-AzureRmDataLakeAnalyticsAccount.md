---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8ca5efc7e5cee80fdf7ce34a13ce23ac733c0154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563596"
---
# <span data-ttu-id="034b6-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="034b6-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="034b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="034b6-102">SYNOPSIS</span></span>
<span data-ttu-id="034b6-103">Изменение учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="034b6-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="034b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="034b6-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="034b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="034b6-105">DESCRIPTION</span></span>
<span data-ttu-id="034b6-106">Командлет **Set-AzureRmDataLakeAnalyticsAccount** изменяет учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="034b6-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="034b6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="034b6-107">EXAMPLES</span></span>

### <span data-ttu-id="034b6-108">Пример 1: изменение источника данных для учетной записи</span><span class="sxs-lookup"><span data-stu-id="034b6-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="034b6-109">Эта команда изменяет источник данных по умолчанию и свойство Tags для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="034b6-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="034b6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="034b6-110">PARAMETERS</span></span>

### <span data-ttu-id="034b6-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="034b6-111">-AllowAzureIpState</span></span>
<span data-ttu-id="034b6-112">При необходимости разрешите или запретите в Azure IP-адреса, которые поступают через брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="034b6-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="034b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034b6-113">-DefaultProfile</span></span>
<span data-ttu-id="034b6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="034b6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="034b6-115">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="034b6-115">-FirewallState</span></span>
<span data-ttu-id="034b6-116">При необходимости включите или отключите существующие правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="034b6-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="034b6-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="034b6-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="034b6-118">Необязательная максимальная поддерживаемая единица измерения для обновления учетной записи.</span><span class="sxs-lookup"><span data-stu-id="034b6-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="034b6-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="034b6-119">-MaxJobCount</span></span>
<span data-ttu-id="034b6-120">Необязательные максимальные поддерживаемые задания, выполняемые под учетной записью, которые должны быть установлены в течение заданного времени.</span><span class="sxs-lookup"><span data-stu-id="034b6-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="034b6-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="034b6-121">-Name</span></span>
<span data-ttu-id="034b6-122">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="034b6-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="034b6-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="034b6-123">-QueryStoreRetention</span></span>
<span data-ttu-id="034b6-124">Необязательное количество дней, в течение которых хранятся метаданные задания для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="034b6-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="034b6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="034b6-125">-ResourceGroupName</span></span>
<span data-ttu-id="034b6-126">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="034b6-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="034b6-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="034b6-127">-Tag</span></span>
<span data-ttu-id="034b6-128">Строковый словарь тегов, связанных с этой учетной записью, который должен заменить текущий набор тегов.</span><span class="sxs-lookup"><span data-stu-id="034b6-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="034b6-129">Уровень</span><span class="sxs-lookup"><span data-stu-id="034b6-129">-Tier</span></span>
<span data-ttu-id="034b6-130">Требуемый уровень обязательства для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="034b6-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="034b6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034b6-131">CommonParameters</span></span>
<span data-ttu-id="034b6-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="034b6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034b6-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="034b6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034b6-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="034b6-134">INPUTS</span></span>

### <span data-ttu-id="034b6-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="034b6-135">None</span></span>
<span data-ttu-id="034b6-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="034b6-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="034b6-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="034b6-137">OUTPUTS</span></span>

### <span data-ttu-id="034b6-138">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="034b6-138">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="034b6-139">Обновленные сведения об учетной записи.</span><span class="sxs-lookup"><span data-stu-id="034b6-139">The updated account details.</span></span>

## <span data-ttu-id="034b6-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="034b6-140">NOTES</span></span>

## <span data-ttu-id="034b6-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="034b6-141">RELATED LINKS</span></span>

[<span data-ttu-id="034b6-142">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="034b6-142">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="034b6-143">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="034b6-143">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="034b6-144">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="034b6-144">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="034b6-145">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="034b6-145">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


