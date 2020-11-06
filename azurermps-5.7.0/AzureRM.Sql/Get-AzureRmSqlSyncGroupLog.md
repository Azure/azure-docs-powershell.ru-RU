---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroupLog.md
ms.openlocfilehash: f8a939dbaac0dadb52aff28b208f7fb69ef836df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566892"
---
# <span data-ttu-id="de55d-101">Get-AzureRmSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="de55d-101">Get-AzureRmSqlSyncGroupLog</span></span>

## <span data-ttu-id="de55d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de55d-102">SYNOPSIS</span></span>
<span data-ttu-id="de55d-103">Возвращает журналы группы синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="de55d-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de55d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de55d-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de55d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de55d-105">DESCRIPTION</span></span>
<span data-ttu-id="de55d-106">Командлет **Get-AzureRmSqlSyncGroupLog** возвращает журналы группы синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="de55d-106">The **Get-AzureRmSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="de55d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de55d-107">EXAMPLES</span></span>

### <span data-ttu-id="de55d-108">Пример 1: получение журналов группы синхронизации Azure SQL</span><span class="sxs-lookup"><span data-stu-id="de55d-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="de55d-109">Эта команда получает журналы группы синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="de55d-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="de55d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de55d-110">PARAMETERS</span></span>

### <span data-ttu-id="de55d-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="de55d-111">-DatabaseName</span></span>
<span data-ttu-id="de55d-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="de55d-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="de55d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de55d-113">-DefaultProfile</span></span>
<span data-ttu-id="de55d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="de55d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de55d-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="de55d-115">-EndTime</span></span>
<span data-ttu-id="de55d-116">Время завершения журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="de55d-116">The end time of the logs to query.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de55d-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="de55d-117">-LogLevel</span></span>
<span data-ttu-id="de55d-118">Тип журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="de55d-118">The type of the logs to query.</span></span>
<span data-ttu-id="de55d-119">Допустимые значения: "ошибка", "предупреждение", "успех" и "все".</span><span class="sxs-lookup"><span data-stu-id="de55d-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de55d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de55d-120">-ResourceGroupName</span></span>
<span data-ttu-id="de55d-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de55d-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="de55d-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="de55d-122">-ServerName</span></span>
<span data-ttu-id="de55d-123">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="de55d-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="de55d-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="de55d-124">-StartTime</span></span>
<span data-ttu-id="de55d-125">Время запуска журналов для запроса.</span><span class="sxs-lookup"><span data-stu-id="de55d-125">The start time of the logs to query.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de55d-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="de55d-126">-SyncGroupName</span></span>
<span data-ttu-id="de55d-127">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="de55d-127">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de55d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de55d-128">CommonParameters</span></span>
<span data-ttu-id="de55d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de55d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de55d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de55d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de55d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de55d-131">INPUTS</span></span>

### <span data-ttu-id="de55d-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="de55d-132">None</span></span>
<span data-ttu-id="de55d-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="de55d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de55d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de55d-134">OUTPUTS</span></span>

### <span data-ttu-id="de55d-135">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncGroupLogModel</span><span class="sxs-lookup"><span data-stu-id="de55d-135">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="de55d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="de55d-136">NOTES</span></span>

## <span data-ttu-id="de55d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de55d-137">RELATED LINKS</span></span>
