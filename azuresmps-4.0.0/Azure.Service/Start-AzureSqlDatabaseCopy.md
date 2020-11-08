---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075845"
---
# <span data-ttu-id="3186c-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3186c-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="3186c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3186c-102">SYNOPSIS</span></span>
<span data-ttu-id="3186c-103">Запускает операцию копирования базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3186c-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="3186c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3186c-104">SYNTAX</span></span>

### <span data-ttu-id="3186c-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3186c-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3186c-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="3186c-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3186c-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3186c-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3186c-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="3186c-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3186c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3186c-109">DESCRIPTION</span></span>
<span data-ttu-id="3186c-110">Командлет **Start-AzureSqlDatabaseCopy** запускает операцию однократного копирования или непрерывную операцию копирования для конкретной базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3186c-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="3186c-111">Этот командлет не является транзакционным.</span><span class="sxs-lookup"><span data-stu-id="3186c-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="3186c-112">Исходная база данных — исходная база данных.</span><span class="sxs-lookup"><span data-stu-id="3186c-112">The original database is the source database.</span></span>
<span data-ttu-id="3186c-113">Копия — это дополнительная или целевая база данных.</span><span class="sxs-lookup"><span data-stu-id="3186c-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="3186c-114">Для непрерывной копии исходная и целевая базы данных не могут находиться на одном и том же сервере, а серверы, на которых размещаются исходная и целевая базы данных, должны входить в одну и ту же подписку.</span><span class="sxs-lookup"><span data-stu-id="3186c-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="3186c-115">Если параметр *ContinuousCopy* не указан, этот командлет создает единовременно одновременную копию исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="3186c-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="3186c-116">После получения ответа операцию можно продолжать.</span><span class="sxs-lookup"><span data-stu-id="3186c-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="3186c-117">Вы можете отслеживать операцию с помощью командлета Get-AzureSqlDatabaseCopy или Get-AzureSqlDatabaseOperation.</span><span class="sxs-lookup"><span data-stu-id="3186c-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="3186c-118">Если вы укажете *ContinuousCopy* , этот командлет создает непрерывную копию исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="3186c-118">If you specify *ContinuousCopy* , this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="3186c-119">При получении ответа операция выполняется.</span><span class="sxs-lookup"><span data-stu-id="3186c-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="3186c-120">Вы можете наблюдать за операцией с помощью **Get-AzureSqlDatabaseCopy** или **Get-AzureSqlDatabaseOperation**.</span><span class="sxs-lookup"><span data-stu-id="3186c-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="3186c-121">Вы можете создать непрерывную копию базы данных в Интернете или в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="3186c-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="3186c-122">Для настройки Active Geo-Replication для базы данных SQL Azure используется непрерывная оперативная копия https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .</span><span class="sxs-lookup"><span data-stu-id="3186c-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="3186c-123">Автономная непрерывная копия используется для настройки стандартных Geo-Replication для базы данных SQL Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .</span><span class="sxs-lookup"><span data-stu-id="3186c-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="3186c-124">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3186c-124">EXAMPLES</span></span>

### <span data-ttu-id="3186c-125">Пример 1: Планирование непрерывной копии базы данных</span><span class="sxs-lookup"><span data-stu-id="3186c-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="3186c-126">Эта команда планирует непрерывную копию базы данных с именем "заказы" на сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="3186c-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="3186c-127">Команда создает целевую базу данных на сервере с именем bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="3186c-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="3186c-128">Пример 2: создание однократного копирования на одном и том же сервере</span><span class="sxs-lookup"><span data-stu-id="3186c-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="3186c-129">Эта команда создает одновременную копию базы данных с именем "заказы" на сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="3186c-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="3186c-130">Команда создает копию с именем OrdersCopy на том же сервере.</span><span class="sxs-lookup"><span data-stu-id="3186c-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="3186c-131">Пример 3: Планирование непрерывной копии базы данных в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="3186c-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="3186c-132">Эта команда планирует непрерывную копию базы данных с именем "заказы" на сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="3186c-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="3186c-133">Эта команда создает автономную целевую базу данных на сервере с именем bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="3186c-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="3186c-134">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3186c-134">PARAMETERS</span></span>

### <span data-ttu-id="3186c-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="3186c-135">-ContinuousCopy</span></span>
<span data-ttu-id="3186c-136">Указывает на то, что копия базы данных будет непрерывной копией (базой данных реплики).</span><span class="sxs-lookup"><span data-stu-id="3186c-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="3186c-137">Непрерывное копирование не поддерживается на одном и том же сервере.</span><span class="sxs-lookup"><span data-stu-id="3186c-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="3186c-138">Если этот параметр не указан, выполняется одновременная копия.</span><span class="sxs-lookup"><span data-stu-id="3186c-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="3186c-139">Для одновременных копий базы данных источников и партнеров должны находиться на одном и том же сервере.</span><span class="sxs-lookup"><span data-stu-id="3186c-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-140">-База данных</span><span class="sxs-lookup"><span data-stu-id="3186c-140">-Database</span></span>
<span data-ttu-id="3186c-141">Указывает объект, представляющий исходную базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="3186c-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="3186c-142">Этот параметр принимает входные данные конвейера.</span><span class="sxs-lookup"><span data-stu-id="3186c-142">This parameter accepts pipeline input.</span></span>

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3186c-143">-DatabaseName</span></span>
<span data-ttu-id="3186c-144">Указывает имя исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="3186c-144">Specifies the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-145">-Force</span><span class="sxs-lookup"><span data-stu-id="3186c-145">-Force</span></span>
<span data-ttu-id="3186c-146">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3186c-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3186c-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="3186c-147">-OfflineSecondary</span></span>
<span data-ttu-id="3186c-148">Указывает на то, что непрерывное копирование является пассивным, а не активной копией.</span><span class="sxs-lookup"><span data-stu-id="3186c-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="3186c-149">Если исходная база данных является базой данных стандартного выпуска, этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3186c-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="3186c-150">Если указан этот параметр, необходимо также указать *ContinuousCopy* .</span><span class="sxs-lookup"><span data-stu-id="3186c-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="3186c-151">-PartnerDatabase</span></span>
<span data-ttu-id="3186c-152">Указывает имя целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="3186c-152">Specifies name of the target database.</span></span>
<span data-ttu-id="3186c-153">Если указан параметр *ContinuousCopy* , значение для *PartnerDatabase* должно совпадать с именем исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="3186c-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="3186c-154">Если вы не указали *ContinuousCopy* , необходимо указать имя целевой базы данных, которое может отличаться от имени базы данных-источника.</span><span class="sxs-lookup"><span data-stu-id="3186c-154">If you do not specify *ContinuousCopy* , you must specify a name for the target database, which can be different from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="3186c-155">-PartnerServer</span></span>
<span data-ttu-id="3186c-156">Указывает имя сервера, на котором размещена целевая база данных.</span><span class="sxs-lookup"><span data-stu-id="3186c-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="3186c-157">Этот сервер должен находиться в той же подписке Azure, что и сервер исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="3186c-157">This server must be in the same Azure subscription as the source database server.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-158">-Profile</span><span class="sxs-lookup"><span data-stu-id="3186c-158">-Profile</span></span>
<span data-ttu-id="3186c-159">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3186c-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3186c-160">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3186c-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-161">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3186c-161">-ServerName</span></span>
<span data-ttu-id="3186c-162">Указывает имя сервера, на котором находится исходная база данных.</span><span class="sxs-lookup"><span data-stu-id="3186c-162">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3186c-163">-Confirm</span></span>
<span data-ttu-id="3186c-164">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3186c-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3186c-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3186c-165">-WhatIf</span></span>
<span data-ttu-id="3186c-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3186c-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3186c-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3186c-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3186c-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3186c-168">CommonParameters</span></span>
<span data-ttu-id="3186c-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3186c-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3186c-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3186c-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3186c-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3186c-171">INPUTS</span></span>

### <span data-ttu-id="3186c-172">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="3186c-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="3186c-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3186c-173">OUTPUTS</span></span>

### <span data-ttu-id="3186c-174">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3186c-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="3186c-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="3186c-175">NOTES</span></span>
* <span data-ttu-id="3186c-176">Проверка подлинности: для этого командлета требуется проверка подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="3186c-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="3186c-177">Пример использования проверки подлинности на основе сертификатов для настройки текущей подписки можно найти в разделе New-AzureSqlDatabaseServerContext командлет.</span><span class="sxs-lookup"><span data-stu-id="3186c-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="3186c-178">Наблюдение: Проверка состояния одного или нескольких связей непрерывной копии, которые активны на сервере, с помощью командлета **Get-AzureSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="3186c-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="3186c-179">Чтобы проверить состояние операций как в исходном, так и на целевом объекте отношения непрерывной копии, используйте командлет **Get-AzureSqlDatabaseOperation** .</span><span class="sxs-lookup"><span data-stu-id="3186c-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="3186c-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3186c-180">RELATED LINKS</span></span>

[<span data-ttu-id="3186c-181">База данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="3186c-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="3186c-182">Операции для баз данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="3186c-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="3186c-183">Начать копирование базы данных</span><span class="sxs-lookup"><span data-stu-id="3186c-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[<span data-ttu-id="3186c-184">Командлеты базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="3186c-184">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="3186c-185">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3186c-185">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="3186c-186">Остановить-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3186c-186">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


