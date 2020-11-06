---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8de6b2a0d86c9eb83a067f4982a5ef62d3a9adbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559875"
---
# <span data-ttu-id="f6822-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f6822-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f6822-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6822-102">SYNOPSIS</span></span>
<span data-ttu-id="f6822-103">Изменение учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f6822-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6822-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6822-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tags] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxDegreeOfParallelism <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6822-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6822-105">DESCRIPTION</span></span>
<span data-ttu-id="f6822-106">Командлет **Set-AzureRmDataLakeAnalyticsAccount** изменяет учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f6822-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f6822-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6822-107">EXAMPLES</span></span>

### <span data-ttu-id="f6822-108">Пример 1: изменение источника данных для учетной записи</span><span class="sxs-lookup"><span data-stu-id="f6822-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="f6822-109">Эта команда изменяет источник данных по умолчанию и свойство Tags для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f6822-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="f6822-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6822-110">PARAMETERS</span></span>

### <span data-ttu-id="f6822-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="f6822-111">-AllowAzureIpState</span></span>
<span data-ttu-id="f6822-112">При необходимости разрешите или запретите в Azure IP-адреса, которые поступают через брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="f6822-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="f6822-113">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="f6822-113">-FirewallState</span></span>
<span data-ttu-id="f6822-114">При необходимости включите или отключите существующие правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="f6822-114">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="f6822-115">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="f6822-115">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="f6822-116">Необязательный максимальный поддерживаемый уровень параллелизма для обновления учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f6822-116">The optional maximum supported degree of parallelism to update the account with.</span></span>

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

### <span data-ttu-id="f6822-117">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="f6822-117">-MaxJobCount</span></span>
<span data-ttu-id="f6822-118">Необязательные максимальные поддерживаемые задания, выполняемые под учетной записью, которые должны быть установлены в течение заданного времени.</span><span class="sxs-lookup"><span data-stu-id="f6822-118">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="f6822-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6822-119">-Name</span></span>
<span data-ttu-id="f6822-120">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f6822-120">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f6822-121">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="f6822-121">-QueryStoreRetention</span></span>
<span data-ttu-id="f6822-122">Необязательное количество дней, в течение которых хранятся метаданные задания для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f6822-122">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="f6822-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6822-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6822-124">Указывает имя группы ресурсов для учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f6822-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="f6822-125">-Теги</span><span class="sxs-lookup"><span data-stu-id="f6822-125">-Tags</span></span>
<span data-ttu-id="f6822-126">Указывает пары "ключ-значение", которые можно использовать для идентификации учетной записи Data Lake Analytics среди других ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f6822-126">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

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

### <span data-ttu-id="f6822-127">Уровень</span><span class="sxs-lookup"><span data-stu-id="f6822-127">-Tier</span></span>
<span data-ttu-id="f6822-128">Требуемый уровень обязательства для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f6822-128">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="f6822-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6822-129">-DefaultProfile</span></span>
<span data-ttu-id="f6822-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6822-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6822-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6822-131">CommonParameters</span></span>
<span data-ttu-id="f6822-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6822-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6822-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6822-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6822-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6822-134">INPUTS</span></span>

## <span data-ttu-id="f6822-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6822-135">OUTPUTS</span></span>

### <span data-ttu-id="f6822-136">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f6822-136">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="f6822-137">Обновленные сведения об учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f6822-137">The updated account details.</span></span>

## <span data-ttu-id="f6822-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6822-138">NOTES</span></span>

## <span data-ttu-id="f6822-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6822-139">RELATED LINKS</span></span>

[<span data-ttu-id="f6822-140">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f6822-140">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f6822-141">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f6822-141">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f6822-142">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f6822-142">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f6822-143">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f6822-143">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


