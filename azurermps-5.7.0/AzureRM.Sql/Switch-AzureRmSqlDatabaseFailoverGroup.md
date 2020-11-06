---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/switch-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: b11478e02baa515fdbd3f3625392616245f2b935
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567373"
---
# <span data-ttu-id="b729e-101">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b729e-101">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="b729e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b729e-102">SYNOPSIS</span></span>
<span data-ttu-id="b729e-103">Выполняет отработку отказа группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b729e-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b729e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b729e-104">SYNTAX</span></span>

```
Switch-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b729e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b729e-105">DESCRIPTION</span></span>
<span data-ttu-id="b729e-106">Эта команда меняет местами роли серверов в группе отработки отказа и переключает все базы данных-получатели на основную роль.</span><span class="sxs-lookup"><span data-stu-id="b729e-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="b729e-107">Все новые сеансы TDS автоматически перенаправляются на дополнительный сервер после обновления кэша DNS-клиента.</span><span class="sxs-lookup"><span data-stu-id="b729e-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="b729e-108">После возвращения исходного основного сервера в сети все ранее базы данных-источники будут переключаться на эту роль.</span><span class="sxs-lookup"><span data-stu-id="b729e-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>

<span data-ttu-id="b729e-109">Для выполнения этой команды необходимо использовать сервер-получатель группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="b729e-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="b729e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b729e-110">EXAMPLES</span></span>

### <span data-ttu-id="b729e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b729e-111">Example 1</span></span>
```
C:\> Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzureRmSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="b729e-112">Выпустить операцию отработки отказа, которая позволяет по конвейеру потерять данные в группе отказоустойчивости.</span><span class="sxs-lookup"><span data-stu-id="b729e-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="b729e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b729e-113">Example 2</span></span>
```
C:\> Switch-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="b729e-114">Выдайте наиболее фиксированную операцию отработки отказа, которая будет выполнена успешно без потери данных или отката.</span><span class="sxs-lookup"><span data-stu-id="b729e-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="b729e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b729e-115">PARAMETERS</span></span>

### <span data-ttu-id="b729e-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="b729e-116">-AllowDataLoss</span></span>
<span data-ttu-id="b729e-117">Завершение отработки отказа, даже если это может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="b729e-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="b729e-118">Это позволит продолжить отработку отказа, даже если база данных-источник недоступна.</span><span class="sxs-lookup"><span data-stu-id="b729e-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b729e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b729e-119">-AsJob</span></span>
<span data-ttu-id="b729e-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b729e-120">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b729e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b729e-121">-DefaultProfile</span></span>
<span data-ttu-id="b729e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b729e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b729e-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="b729e-123">-FailoverGroupName</span></span>
<span data-ttu-id="b729e-124">Имя группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b729e-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="b729e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b729e-125">-ResourceGroupName</span></span>
<span data-ttu-id="b729e-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b729e-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="b729e-127">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b729e-127">-ServerName</span></span>
<span data-ttu-id="b729e-128">Имя дополнительного сервера базы данных SQL Azure для группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="b729e-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="b729e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b729e-129">-Confirm</span></span>
<span data-ttu-id="b729e-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b729e-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b729e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b729e-131">-WhatIf</span></span>
<span data-ttu-id="b729e-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b729e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b729e-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b729e-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b729e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b729e-134">CommonParameters</span></span>
<span data-ttu-id="b729e-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b729e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b729e-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b729e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b729e-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b729e-137">INPUTS</span></span>

### <span data-ttu-id="b729e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b729e-138">System.String</span></span>

## <span data-ttu-id="b729e-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b729e-139">OUTPUTS</span></span>

### <span data-ttu-id="b729e-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="b729e-140">System.Object</span></span>

## <span data-ttu-id="b729e-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="b729e-141">NOTES</span></span>

## <span data-ttu-id="b729e-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b729e-142">RELATED LINKS</span></span>

[<span data-ttu-id="b729e-143">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b729e-143">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b729e-144">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b729e-144">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b729e-145">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b729e-145">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b729e-146">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b729e-146">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="b729e-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b729e-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="b729e-148">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b729e-148">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b729e-149">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="b729e-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
