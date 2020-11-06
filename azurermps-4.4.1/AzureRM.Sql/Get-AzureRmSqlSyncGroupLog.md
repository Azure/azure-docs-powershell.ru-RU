---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
ms.openlocfilehash: 924e00578383e103d1451e311d027edd02752496
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559460"
---
# <span data-ttu-id="dc4f2-101">Get-AzureRmSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="dc4f2-101">Get-AzureRmSqlSyncGroupLog</span></span>

## <span data-ttu-id="dc4f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="dc4f2-103">Возвращает журналы группы синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc4f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc4f2-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc4f2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc4f2-105">DESCRIPTION</span></span>
<span data-ttu-id="dc4f2-106">Командлет **Get-AzureRmSqlSyncGroupLog** возвращает журналы группы синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-106">The **Get-AzureRmSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="dc4f2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc4f2-107">EXAMPLES</span></span>

### <span data-ttu-id="dc4f2-108">Пример 1: получение журналов группы синхронизации Azure SQL</span><span class="sxs-lookup"><span data-stu-id="dc4f2-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="dc4f2-109">Эта команда получает журналы группы синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="dc4f2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc4f2-110">PARAMETERS</span></span>

### <span data-ttu-id="dc4f2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc4f2-111">-DatabaseName</span></span>
<span data-ttu-id="dc4f2-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="dc4f2-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dc4f2-113">-EndTime</span></span>
<span data-ttu-id="dc4f2-114">Время завершения журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-114">The end time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4f2-115">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="dc4f2-115">-LogLevel</span></span>
<span data-ttu-id="dc4f2-116">Тип журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-116">The type of the logs to query.</span></span>
<span data-ttu-id="dc4f2-117">Допустимые значения: "ошибка", "предупреждение", "успех" и "все".</span><span class="sxs-lookup"><span data-stu-id="dc4f2-117">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4f2-118">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="dc4f2-118">-SyncGroupName</span></span>
<span data-ttu-id="dc4f2-119">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-119">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc4f2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc4f2-120">-ResourceGroupName</span></span>
<span data-ttu-id="dc4f2-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="dc4f2-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="dc4f2-122">-ServerName</span></span>
<span data-ttu-id="dc4f2-123">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="dc4f2-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dc4f2-124">-StartTime</span></span>
<span data-ttu-id="dc4f2-125">Время запуска журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-125">The start time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc4f2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc4f2-126">-DefaultProfile</span></span>
<span data-ttu-id="dc4f2-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc4f2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc4f2-128">CommonParameters</span></span>
<span data-ttu-id="dc4f2-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc4f2-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc4f2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc4f2-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc4f2-131">INPUTS</span></span>

## <span data-ttu-id="dc4f2-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc4f2-132">OUTPUTS</span></span>

### <span data-ttu-id="dc4f2-133">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="dc4f2-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="dc4f2-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc4f2-134">NOTES</span></span>

## <span data-ttu-id="dc4f2-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc4f2-135">RELATED LINKS</span></span>

