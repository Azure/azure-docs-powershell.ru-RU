---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413070"
---
# <span data-ttu-id="630ec-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="630ec-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="630ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="630ec-102">SYNOPSIS</span></span>
<span data-ttu-id="630ec-103">Начинает операцию копирования базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="630ec-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="630ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="630ec-104">SYNTAX</span></span>

### <span data-ttu-id="630ec-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="630ec-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="630ec-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="630ec-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="630ec-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="630ec-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="630ec-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="630ec-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="630ec-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="630ec-109">DESCRIPTION</span></span>
<span data-ttu-id="630ec-110">Для запуска однобайтового копирования или непрерывной копии определенной базы данных Azure SQL запускается проектный SQL **AzureSqlDataCopy.**</span><span class="sxs-lookup"><span data-stu-id="630ec-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="630ec-111">Этот cmdlet не является транзакцией.</span><span class="sxs-lookup"><span data-stu-id="630ec-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="630ec-112">Исходная база данных является исходной.</span><span class="sxs-lookup"><span data-stu-id="630ec-112">The original database is the source database.</span></span>
<span data-ttu-id="630ec-113">Копия является вторичной или целевой базой данных.</span><span class="sxs-lookup"><span data-stu-id="630ec-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="630ec-114">При непрерывной копии исходные и целевые базы данных не могут находиться на одном сервере, а серверы, на основе которой они находятся, должны быть частью одной подписки.</span><span class="sxs-lookup"><span data-stu-id="630ec-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="630ec-115">Если параметр *ContinuousCopy* не задан, этот cmdlet создает разовую копию базы данных.</span><span class="sxs-lookup"><span data-stu-id="630ec-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="630ec-116">После того как ответ будет получен, операция по-прежнему может быть в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="630ec-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="630ec-117">Вы можете отслеживать операцию с помощью Get-AzureSqlDatabaseCopy или Get-AzureSqlDatabaseOperation.</span><span class="sxs-lookup"><span data-stu-id="630ec-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="630ec-118">Если задать *Режим ContinuousCopy,* этот cmdlet создаст рывную копию базы данных.</span><span class="sxs-lookup"><span data-stu-id="630ec-118">If you specify *ContinuousCopy*, this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="630ec-119">После того как ответ будет получен, операция будет в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="630ec-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="630ec-120">Вы можете отслеживать операцию с помощью **Get-AzureSqlDatabaseCopy** или **Get-AzureSqlDatabaseOperation.**</span><span class="sxs-lookup"><span data-stu-id="630ec-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="630ec-121">Вы можете создать непрерывную копию в виде интерактивной или автономной базы данных.</span><span class="sxs-lookup"><span data-stu-id="630ec-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="630ec-122">Веб-лентоемая копия используется для настройки active Geo-Replication для базы данных Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ SQL.</span><span class="sxs-lookup"><span data-stu-id="630ec-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="630ec-123">Для настройки стандартной Geo-Replication для базы данных Azure SQL используется SQL копировать. https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/</span><span class="sxs-lookup"><span data-stu-id="630ec-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="630ec-124">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="630ec-124">EXAMPLES</span></span>

### <span data-ttu-id="630ec-125">Пример 1. Запланируйте непрерывную копию базы данных</span><span class="sxs-lookup"><span data-stu-id="630ec-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="630ec-126">Эта команда запланирует непрерывную копию базы данных "Заказы" на сервере lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="630ec-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="630ec-127">Команда создает целевую базу данных на сервере с именем bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="630ec-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="630ec-128">Пример 2. Создание одно экземпляра на одном сервере</span><span class="sxs-lookup"><span data-stu-id="630ec-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="630ec-129">Эта команда создает разовую копию базы данных "Заказы" на сервере с именем lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="630ec-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="630ec-130">Команда создает копию с именем OrdersCopy на том же сервере.</span><span class="sxs-lookup"><span data-stu-id="630ec-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="630ec-131">Пример 3. Запланируйте непрерывную копию автономной базы данных</span><span class="sxs-lookup"><span data-stu-id="630ec-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="630ec-132">Эта команда запланирует непрерывную копию базы данных "Заказы" на сервере lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="630ec-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="630ec-133">Эта команда создает целевую базу данных автономного режима на сервере bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="630ec-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="630ec-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="630ec-134">PARAMETERS</span></span>

### <span data-ttu-id="630ec-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="630ec-135">-ContinuousCopy</span></span>
<span data-ttu-id="630ec-136">Означает, что копия базы данных будет непрерывной (копией).</span><span class="sxs-lookup"><span data-stu-id="630ec-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="630ec-137">Непрерывная копия не поддерживается на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="630ec-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="630ec-138">Если этот параметр не задан, выполняется разовая копия.</span><span class="sxs-lookup"><span data-stu-id="630ec-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="630ec-139">Для разной копии исходные и партнерские базы данных должны быть на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="630ec-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

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

### <span data-ttu-id="630ec-140">-Database</span><span class="sxs-lookup"><span data-stu-id="630ec-140">-Database</span></span>
<span data-ttu-id="630ec-141">Определяет объект, который представляет исходный источник базы SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="630ec-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="630ec-142">Этот параметр принимает входные данные конвейера.</span><span class="sxs-lookup"><span data-stu-id="630ec-142">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="630ec-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="630ec-143">-DatabaseName</span></span>
<span data-ttu-id="630ec-144">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="630ec-144">Specifies the name of the source database.</span></span>

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

### <span data-ttu-id="630ec-145">-Force</span><span class="sxs-lookup"><span data-stu-id="630ec-145">-Force</span></span>
<span data-ttu-id="630ec-146">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="630ec-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="630ec-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="630ec-147">-OfflineSecondary</span></span>
<span data-ttu-id="630ec-148">Указывает, что непрерывной копией является пассивная, а не активная копия.</span><span class="sxs-lookup"><span data-stu-id="630ec-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="630ec-149">Если базой данных является standard edition, этот параметр является required.</span><span class="sxs-lookup"><span data-stu-id="630ec-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="630ec-150">Если этот параметр задан, необходимо также у *указывается ContinuousCopy.*</span><span class="sxs-lookup"><span data-stu-id="630ec-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

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

### <span data-ttu-id="630ec-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="630ec-151">-PartnerDatabase</span></span>
<span data-ttu-id="630ec-152">Указывает имя целевой базы данных.</span><span class="sxs-lookup"><span data-stu-id="630ec-152">Specifies name of the target database.</span></span>
<span data-ttu-id="630ec-153">Если для *параметра ContinuousCopy задан параметр ContinuousCopy,* значение *partnerDatabase* должно совпадать с именем базы данных.</span><span class="sxs-lookup"><span data-stu-id="630ec-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="630ec-154">Если не указать *ContinuousCopy,* необходимо указать имя целевой базы данных, которое может быть другим.</span><span class="sxs-lookup"><span data-stu-id="630ec-154">If you do not specify *ContinuousCopy*, you must specify a name for the target database, which can be different from the source database name.</span></span>

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

### <span data-ttu-id="630ec-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="630ec-155">-PartnerServer</span></span>
<span data-ttu-id="630ec-156">Имя сервера, на котором размещена целевая база данных.</span><span class="sxs-lookup"><span data-stu-id="630ec-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="630ec-157">Этот сервер должен быть в той же подписке Azure, что и исходный сервер базы данных.</span><span class="sxs-lookup"><span data-stu-id="630ec-157">This server must be in the same Azure subscription as the source database server.</span></span>

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

### <span data-ttu-id="630ec-158">-Profile</span><span class="sxs-lookup"><span data-stu-id="630ec-158">-Profile</span></span>
<span data-ttu-id="630ec-159">Определяет профиль Azure, для которого читается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="630ec-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="630ec-160">Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="630ec-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="630ec-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="630ec-161">-ServerName</span></span>
<span data-ttu-id="630ec-162">Указывает имя сервера, на котором находится базовая база данных.</span><span class="sxs-lookup"><span data-stu-id="630ec-162">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="630ec-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="630ec-163">-Confirm</span></span>
<span data-ttu-id="630ec-164">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="630ec-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="630ec-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="630ec-165">-WhatIf</span></span>
<span data-ttu-id="630ec-166">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="630ec-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="630ec-167">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="630ec-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="630ec-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="630ec-168">CommonParameters</span></span>
<span data-ttu-id="630ec-169">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="630ec-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="630ec-170">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="630ec-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="630ec-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="630ec-171">INPUTS</span></span>

### <span data-ttu-id="630ec-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="630ec-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="630ec-173">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="630ec-173">OUTPUTS</span></span>

### <span data-ttu-id="630ec-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="630ec-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="630ec-175">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="630ec-175">NOTES</span></span>
* <span data-ttu-id="630ec-176">Проверка подлинности: этот cmdlet требует проверки подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="630ec-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="630ec-177">Пример использования проверки подлинности на основе сертификата для проверки текущей подписки см. в New-AzureSqlDatabaseServerContext.</span><span class="sxs-lookup"><span data-stu-id="630ec-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="630ec-178">Мониторинг. Чтобы проверить состояние активных на сервере связей непрерывной копии, используйте для этого cmdlet **Get-AzureSqlDataBaseCopy.**</span><span class="sxs-lookup"><span data-stu-id="630ec-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="630ec-179">Чтобы проверить состояние операций как в источнике, так и в целевом объекте непрерывной копии, воспользуйтесь cmdlet **Get-AzureSqlDatabaseOperation.**</span><span class="sxs-lookup"><span data-stu-id="630ec-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="630ec-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="630ec-180">RELATED LINKS</span></span>

[<span data-ttu-id="630ec-181">База SQL Azure</span><span class="sxs-lookup"><span data-stu-id="630ec-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="630ec-182">Операции для баз данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="630ec-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="630ec-183">Запуск копирования базы данных</span><span class="sxs-lookup"><span data-stu-id="630ec-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[<span data-ttu-id="630ec-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="630ec-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="630ec-185">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="630ec-185">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


