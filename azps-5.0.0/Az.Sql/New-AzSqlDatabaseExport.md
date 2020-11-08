---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: c5b0295458d0efe443dc20ab069ccfb62a44eb49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246536"
---
# <span data-ttu-id="bec14-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="bec14-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="bec14-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bec14-102">SYNOPSIS</span></span>
<span data-ttu-id="bec14-103">Экспортирует базу данных SQL Azure в виде BACPAC-файла в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="bec14-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="bec14-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bec14-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bec14-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bec14-105">DESCRIPTION</span></span>
<span data-ttu-id="bec14-106">Командлет **New-AzSqlDatabaseExport** экспортирует базу данных SQL Azure в виде BACPAC-файла в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="bec14-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="bec14-107">Чтобы получить сведения о состоянии этого запроса, может быть отправлен запрос на получение состояния базы данных для экспорта.</span><span class="sxs-lookup"><span data-stu-id="bec14-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="bec14-108">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="bec14-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="bec14-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bec14-109">EXAMPLES</span></span>

### <span data-ttu-id="bec14-110">Пример 1: Создание запроса на экспорт для базы данных</span><span class="sxs-lookup"><span data-stu-id="bec14-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="bec14-111">Эта команда создает запрос на экспорт для указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="bec14-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="bec14-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bec14-112">PARAMETERS</span></span>

### <span data-ttu-id="bec14-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="bec14-113">-AdministratorLogin</span></span>
<span data-ttu-id="bec14-114">Указывает имя администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="bec14-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="bec14-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="bec14-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="bec14-116">Указывает пароль администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="bec14-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="bec14-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="bec14-117">-AuthenticationType</span></span>
<span data-ttu-id="bec14-118">Указывает тип проверки подлинности, используемой для доступа к серверу.</span><span class="sxs-lookup"><span data-stu-id="bec14-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="bec14-119">Если тип проверки подлинности не задан, значение по умолчанию — SQL.</span><span class="sxs-lookup"><span data-stu-id="bec14-119">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="bec14-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bec14-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bec14-121">Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bec14-121">Sql.</span></span>
<span data-ttu-id="bec14-122">Проверка подлинности SQL.</span><span class="sxs-lookup"><span data-stu-id="bec14-122">SQL authentication.</span></span>
<span data-ttu-id="bec14-123">Задайте для свойства *AdministratorLogin* и *AdministratorLoginPassword* имя пользователя и пароль администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="bec14-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="bec14-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="bec14-124">ADPassword.</span></span>
<span data-ttu-id="bec14-125">Проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bec14-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="bec14-126">Укажите имя пользователя и пароль администратора Azure AD в *AdministratorLogin* и *AdministratorLoginPassword* .</span><span class="sxs-lookup"><span data-stu-id="bec14-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="bec14-127">Этот параметр доступен только на серверах SQL Database версии 12.</span><span class="sxs-lookup"><span data-stu-id="bec14-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="bec14-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bec14-128">-DatabaseName</span></span>
<span data-ttu-id="bec14-129">Указывает имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bec14-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="bec14-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec14-130">-DefaultProfile</span></span>
<span data-ttu-id="bec14-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bec14-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bec14-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec14-132">-ResourceGroupName</span></span>
<span data-ttu-id="bec14-133">Указывает имя группы ресурсов для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bec14-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="bec14-134">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bec14-134">-ServerName</span></span>
<span data-ttu-id="bec14-135">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="bec14-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="bec14-136">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="bec14-136">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="bec14-137">Идентификатор ресурса SQL Server для создания частной ссылки</span><span class="sxs-lookup"><span data-stu-id="bec14-137">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="bec14-138">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="bec14-138">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="bec14-139">Идентификатор ресурса учетной записи хранения для создания частной ссылки</span><span class="sxs-lookup"><span data-stu-id="bec14-139">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="bec14-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="bec14-140">-StorageKey</span></span>
<span data-ttu-id="bec14-141">Задает клавишу доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bec14-141">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="bec14-142">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="bec14-142">-StorageKeyType</span></span>
<span data-ttu-id="bec14-143">Указывает тип клавиши доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bec14-143">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="bec14-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bec14-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bec14-145">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="bec14-145">StorageAccessKey.</span></span>
<span data-ttu-id="bec14-146">Это значение использует ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bec14-146">This value uses a storage account key.</span></span> 
- <span data-ttu-id="bec14-147">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="bec14-147">SharedAccessKey.</span></span>
<span data-ttu-id="bec14-148">Это значение использует ключ подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="bec14-148">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="bec14-149">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="bec14-149">-StorageUri</span></span>
<span data-ttu-id="bec14-150">Указывает ссылку на большой двоичный объект в виде URL-адреса на файл. BACPAC.</span><span class="sxs-lookup"><span data-stu-id="bec14-150">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="bec14-151">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="bec14-151">-UseNetworkIsolation</span></span>
<span data-ttu-id="bec14-152">Если этот параметр установлен, будет создана частная ссылка для учетной записи хранения и (или) сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bec14-152">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="bec14-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bec14-153">-Confirm</span></span>
<span data-ttu-id="bec14-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bec14-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec14-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec14-155">-WhatIf</span></span>
<span data-ttu-id="bec14-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bec14-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bec14-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bec14-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec14-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec14-158">CommonParameters</span></span>
<span data-ttu-id="bec14-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bec14-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec14-160">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bec14-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec14-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bec14-161">INPUTS</span></span>

### <span data-ttu-id="bec14-162">System. String</span><span class="sxs-lookup"><span data-stu-id="bec14-162">System.String</span></span>

## <span data-ttu-id="bec14-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bec14-163">OUTPUTS</span></span>

### <span data-ttu-id="bec14-164">Microsoft. Azure. Commands. SQL. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="bec14-164">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="bec14-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="bec14-165">NOTES</span></span>
* <span data-ttu-id="bec14-166">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="bec14-166">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="bec14-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bec14-167">RELATED LINKS</span></span>

[<span data-ttu-id="bec14-168">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="bec14-168">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="bec14-169">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="bec14-169">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="bec14-170">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="bec14-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
