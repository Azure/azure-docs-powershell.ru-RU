---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 05f2de37ebeb477d45f96c415759ead3080a9e60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563844"
---
# <span data-ttu-id="1293e-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1293e-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="1293e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1293e-102">SYNOPSIS</span></span>
<span data-ttu-id="1293e-103">Изменяет конфигурацию группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1293e-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1293e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1293e-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1293e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1293e-105">DESCRIPTION</span></span>
<span data-ttu-id="1293e-106">Эта команда изменяет конфигурацию группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1293e-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>

<span data-ttu-id="1293e-107">Для выполнения команды следует использовать основной сервер группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="1293e-107">The Failover Group's primary server should be used to execute the command.</span></span>

<span data-ttu-id="1293e-108">Для управления набором баз данных в группе используйте команды "Add-AzureRmSqlDatabaseToFailoverGroup" и "Remove-AzureRmSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="1293e-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>

<span data-ttu-id="1293e-109">Во время предварительного просмотра компонента "группы отработки отказа" для параметра "-GracePeriodWithDataLossHours" поддерживаются только значения, превышающие или равные 1 часу.</span><span class="sxs-lookup"><span data-stu-id="1293e-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="1293e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1293e-110">EXAMPLES</span></span>

### <span data-ttu-id="1293e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1293e-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="1293e-112">Задает для политики отработки отказа отказоустойчивой группы значение "Авто".</span><span class="sxs-lookup"><span data-stu-id="1293e-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="1293e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1293e-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="1293e-114">Задает для политики отработки отказа отказоустойчивой группы значение "вручную" по конвейеру в группе отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="1293e-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="1293e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1293e-115">PARAMETERS</span></span>

### <span data-ttu-id="1293e-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="1293e-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="1293e-117">Следует ли запускать автоматический переход с конечной точки только для чтения на сервере-получателе.</span><span class="sxs-lookup"><span data-stu-id="1293e-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="1293e-118">Эта функция пока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1293e-118">This feature is not yet supported.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1293e-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="1293e-119">-FailoverGroupName</span></span>
<span data-ttu-id="1293e-120">Имя группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1293e-120">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="1293e-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="1293e-121">-FailoverPolicy</span></span>
<span data-ttu-id="1293e-122">Политика перемещения при сбое для группы Azure SQL Database failover.</span><span class="sxs-lookup"><span data-stu-id="1293e-122">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1293e-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="1293e-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="1293e-124">Интервал перед автоматическим переходом на другой ресурс инициируется при возникновении сбоя на сервере основного сервера, и отработка отказа не может быть завершена без потери данных.</span><span class="sxs-lookup"><span data-stu-id="1293e-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1293e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1293e-125">-ResourceGroupName</span></span>
<span data-ttu-id="1293e-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1293e-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="1293e-127">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1293e-127">-ServerName</span></span>
<span data-ttu-id="1293e-128">Имя основного сервера базы данных Azure SQL для группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="1293e-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="1293e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1293e-129">-DefaultProfile</span></span>
<span data-ttu-id="1293e-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1293e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1293e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1293e-131">CommonParameters</span></span>
<span data-ttu-id="1293e-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1293e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1293e-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1293e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1293e-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1293e-134">INPUTS</span></span>

### <span data-ttu-id="1293e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1293e-135">System.String</span></span>

## <span data-ttu-id="1293e-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1293e-136">OUTPUTS</span></span>

### <span data-ttu-id="1293e-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="1293e-137">System.Object</span></span>

## <span data-ttu-id="1293e-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="1293e-138">NOTES</span></span>

## <span data-ttu-id="1293e-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1293e-139">RELATED LINKS</span></span>

[<span data-ttu-id="1293e-140">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1293e-140">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1293e-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1293e-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1293e-142">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1293e-142">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="1293e-143">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1293e-143">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="1293e-144">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1293e-144">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1293e-145">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1293e-145">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1293e-146">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="1293e-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
