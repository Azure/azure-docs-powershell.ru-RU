---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: 074261adf9c2f5501ca12753971fac08783ab36f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078659"
---
# <span data-ttu-id="db91a-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="db91a-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="db91a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db91a-102">SYNOPSIS</span></span>
<span data-ttu-id="db91a-103">Импортирует BACPAC-файл и создает на сервере новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="db91a-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="db91a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db91a-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db91a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db91a-105">DESCRIPTION</span></span>
<span data-ttu-id="db91a-106">Командлет **New-AzSqlDatabaseImport** импортирует файл BACPAC из учетной записи хранения Azure в новую базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="db91a-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="db91a-107">Чтобы получить сведения о состоянии этого запроса, может быть отправлен запрос на получение состояния базы данных для импорта.</span><span class="sxs-lookup"><span data-stu-id="db91a-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="db91a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db91a-108">EXAMPLES</span></span>

### <span data-ttu-id="db91a-109">Пример 1: Создание запроса на импорт для BACPAC-файла</span><span class="sxs-lookup"><span data-stu-id="db91a-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="db91a-110">Эта команда создает запрос на импорт для импорта BACPAC-пакета в новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="db91a-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="db91a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db91a-111">PARAMETERS</span></span>

### <span data-ttu-id="db91a-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="db91a-112">-AdministratorLogin</span></span>
<span data-ttu-id="db91a-113">Указывает имя администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="db91a-113">Specifies the name of the SQL administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="db91a-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="db91a-115">Указывает пароль администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="db91a-115">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="db91a-116">-AuthenticationType</span></span>
<span data-ttu-id="db91a-117">Указывает тип проверки подлинности, используемой для доступа к серверу.</span><span class="sxs-lookup"><span data-stu-id="db91a-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="db91a-118">Этот параметр по умолчанию имеет значение SQL, если не задан тип проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="db91a-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="db91a-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="db91a-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db91a-120">Microsoft.</span><span class="sxs-lookup"><span data-stu-id="db91a-120">SQL.</span></span>
<span data-ttu-id="db91a-121">Проверка подлинности SQL.</span><span class="sxs-lookup"><span data-stu-id="db91a-121">SQL authentication.</span></span>
<span data-ttu-id="db91a-122">Задайте для параметров *AdministratorLogin* и *AdministratorLoginPassword* имя пользователя и пароль администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="db91a-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="db91a-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="db91a-123">ADPassword.</span></span>
<span data-ttu-id="db91a-124">Проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db91a-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="db91a-125">Настройте *AdministratorLogin* и *AdministratorLoginPassword* на имя пользователя и пароль администратора Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db91a-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="db91a-126">Этот параметр доступен только на серверах SQL Database версии 12.</span><span class="sxs-lookup"><span data-stu-id="db91a-126">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="db91a-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="db91a-128">Задает максимальный размер для новой импортированной базы данных.</span><span class="sxs-lookup"><span data-stu-id="db91a-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="db91a-129">-DatabaseName</span></span>
<span data-ttu-id="db91a-130">Указывает имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="db91a-130">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db91a-131">-DefaultProfile</span></span>
<span data-ttu-id="db91a-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="db91a-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db91a-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="db91a-133">-Edition</span></span>
<span data-ttu-id="db91a-134">Определяет версию новой базы данных, в которую будет импортироваться элемент.</span><span class="sxs-lookup"><span data-stu-id="db91a-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="db91a-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="db91a-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db91a-136">Версию</span><span class="sxs-lookup"><span data-stu-id="db91a-136">Premium</span></span>
- <span data-ttu-id="db91a-137">Базового</span><span class="sxs-lookup"><span data-stu-id="db91a-137">Basic</span></span>
- <span data-ttu-id="db91a-138">Стандартная</span><span class="sxs-lookup"><span data-stu-id="db91a-138">Standard</span></span>
- <span data-ttu-id="db91a-139">Хранилище Datawarehouse</span><span class="sxs-lookup"><span data-stu-id="db91a-139">DataWarehouse</span></span>
- <span data-ttu-id="db91a-140">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="db91a-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db91a-141">-ResourceGroupName</span></span>
<span data-ttu-id="db91a-142">Указывает имя группы ресурсов для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="db91a-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="db91a-143">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="db91a-143">-ServerName</span></span>
<span data-ttu-id="db91a-144">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="db91a-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="db91a-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="db91a-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="db91a-146">Указывает имя цели обслуживания, которую нужно назначить базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="db91a-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-147">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="db91a-147">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="db91a-148">Идентификатор ресурса SQL Server для создания частной ссылки</span><span class="sxs-lookup"><span data-stu-id="db91a-148">The sql server resource id to create private link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-149">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="db91a-149">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="db91a-150">Идентификатор ресурса учетной записи хранения для создания частной ссылки</span><span class="sxs-lookup"><span data-stu-id="db91a-150">The storage account resource id to create private link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-151">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="db91a-151">-StorageKey</span></span>
<span data-ttu-id="db91a-152">Задает клавишу доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="db91a-152">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="db91a-153">-StorageKeyType</span></span>
<span data-ttu-id="db91a-154">Указывает тип клавиши доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="db91a-154">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="db91a-155">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="db91a-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db91a-156">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="db91a-156">StorageAccessKey.</span></span>
<span data-ttu-id="db91a-157">Использует ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="db91a-157">Uses the storage account key.</span></span> 
- <span data-ttu-id="db91a-158">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="db91a-158">SharedAccessKey.</span></span>
<span data-ttu-id="db91a-159">Использует ключ подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="db91a-159">Uses the Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-160">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="db91a-160">-StorageUri</span></span>
<span data-ttu-id="db91a-161">Указывает URI BLOB-объектов для BACPAC-файла.</span><span class="sxs-lookup"><span data-stu-id="db91a-161">Specifies the blob URI of the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-162">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="db91a-162">-UseNetworkIsolation</span></span>
<span data-ttu-id="db91a-163">Если этот параметр установлен, будет создана частная ссылка для учетной записи хранения и (или) сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="db91a-163">If set, will create private link for storage account and/or SQL server</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db91a-164">-Confirm</span></span>
<span data-ttu-id="db91a-165">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db91a-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db91a-166">-WhatIf</span></span>
<span data-ttu-id="db91a-167">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db91a-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db91a-168">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db91a-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db91a-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db91a-169">CommonParameters</span></span>
<span data-ttu-id="db91a-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db91a-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db91a-171">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db91a-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db91a-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db91a-172">INPUTS</span></span>

### <span data-ttu-id="db91a-173">System. String</span><span class="sxs-lookup"><span data-stu-id="db91a-173">System.String</span></span>

## <span data-ttu-id="db91a-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db91a-174">OUTPUTS</span></span>

### <span data-ttu-id="db91a-175">Microsoft. Azure. Commands. SQL. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="db91a-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="db91a-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="db91a-176">NOTES</span></span>
* <span data-ttu-id="db91a-177">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="db91a-177">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="db91a-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db91a-178">RELATED LINKS</span></span>

[<span data-ttu-id="db91a-179">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="db91a-179">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="db91a-180">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="db91a-180">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="db91a-181">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="db91a-181">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

