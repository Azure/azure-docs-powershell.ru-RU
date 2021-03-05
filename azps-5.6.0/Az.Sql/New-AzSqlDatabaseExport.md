---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 198692c73609f6e3e88be0ccbe270c60bc679020
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979208"
---
# <span data-ttu-id="b571e-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="b571e-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="b571e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b571e-102">SYNOPSIS</span></span>
<span data-ttu-id="b571e-103">Экспорт базы данных Azure SQL в качестве BACPAC-файла в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="b571e-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="b571e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b571e-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b571e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b571e-105">DESCRIPTION</span></span>
<span data-ttu-id="b571e-106">Для этого в учетную запись хранения будет экспортироваться база данных Azure SQL **AzSqlDataExport** в качестве ФАЙЛА BACPAC.</span><span class="sxs-lookup"><span data-stu-id="b571e-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="b571e-107">Запрос на экспорт базы данных может быть отправлен для получения сведений о состоянии для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="b571e-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="b571e-108">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="b571e-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b571e-109">Для использования этого брандмауэра на сервере Azure SQL Server необходимо настроить "Разрешить службам и ресурсам Azure доступ к этому серверу".</span><span class="sxs-lookup"><span data-stu-id="b571e-109">In order to make use of this cmdlet the firewall on the Azure SQL Server will need to be configured to "Allow Azure services and resources to access this server".</span></span> <span data-ttu-id="b571e-110">Если это не так, будут ошибки GatewayTimeout.</span><span class="sxs-lookup"><span data-stu-id="b571e-110">If this is not configured then GatewayTimeout errors will be experienced.</span></span>

## <span data-ttu-id="b571e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b571e-111">EXAMPLES</span></span>

### <span data-ttu-id="b571e-112">Пример 1. Создание запроса на экспорт базы данных</span><span class="sxs-lookup"><span data-stu-id="b571e-112">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="b571e-113">Эта команда создает запрос на экспорт для указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="b571e-113">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="b571e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b571e-114">PARAMETERS</span></span>

### <span data-ttu-id="b571e-115">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="b571e-115">-AdministratorLogin</span></span>
<span data-ttu-id="b571e-116">Указывает имя администратора SQL.</span><span class="sxs-lookup"><span data-stu-id="b571e-116">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="b571e-117">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b571e-117">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b571e-118">Пароль администратора SQL пользователя.</span><span class="sxs-lookup"><span data-stu-id="b571e-118">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="b571e-119">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="b571e-119">-AuthenticationType</span></span>
<span data-ttu-id="b571e-120">Определяет тип проверки подлинности, используемой для доступа к серверу.</span><span class="sxs-lookup"><span data-stu-id="b571e-120">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="b571e-121">Значение по умолчанию — SQL, если тип проверки подлинности не за установлен.</span><span class="sxs-lookup"><span data-stu-id="b571e-121">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="b571e-122">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="b571e-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b571e-123">SQL.</span><span class="sxs-lookup"><span data-stu-id="b571e-123">Sql.</span></span>
<span data-ttu-id="b571e-124">SQL проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b571e-124">SQL authentication.</span></span>
<span data-ttu-id="b571e-125">*Задайте для administratorLogin* и *AdministratorLoginPassword* имя SQL и пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="b571e-125">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="b571e-126">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="b571e-126">ADPassword.</span></span>
<span data-ttu-id="b571e-127">Проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b571e-127">Azure Active Directory authentication.</span></span>
<span data-ttu-id="b571e-128">*Задайте для administratorLogin* и *AdministratorLoginPassword* имя пользователя и пароль администратора Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b571e-128">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="b571e-129">Этот параметр доступен только на серверах SQL Database V12.</span><span class="sxs-lookup"><span data-stu-id="b571e-129">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="b571e-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b571e-130">-DatabaseName</span></span>
<span data-ttu-id="b571e-131">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="b571e-131">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="b571e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b571e-132">-DefaultProfile</span></span>
<span data-ttu-id="b571e-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b571e-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b571e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b571e-134">-ResourceGroupName</span></span>
<span data-ttu-id="b571e-135">Имя группы ресурсов для сервера SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="b571e-135">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="b571e-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b571e-136">-ServerName</span></span>
<span data-ttu-id="b571e-137">Указывает имя сервера базы SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="b571e-137">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="b571e-138">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="b571e-138">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="b571e-139">The sql server resource id to create private link</span><span class="sxs-lookup"><span data-stu-id="b571e-139">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="b571e-140">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="b571e-140">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="b571e-141">ИД ресурса учетной записи хранения для создания частной ссылки</span><span class="sxs-lookup"><span data-stu-id="b571e-141">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="b571e-142">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="b571e-142">-StorageKey</span></span>
<span data-ttu-id="b571e-143">Указывает ключ доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b571e-143">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="b571e-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="b571e-144">-StorageKeyType</span></span>
<span data-ttu-id="b571e-145">Определяет тип ключа доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b571e-145">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="b571e-146">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="b571e-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b571e-147">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="b571e-147">StorageAccessKey.</span></span>
<span data-ttu-id="b571e-148">Для этого значения используется ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b571e-148">This value uses a storage account key.</span></span> 
- <span data-ttu-id="b571e-149">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="b571e-149">SharedAccessKey.</span></span>
<span data-ttu-id="b571e-150">Это значение использует ключ подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="b571e-150">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="b571e-151">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="b571e-151">-StorageUri</span></span>
<span data-ttu-id="b571e-152">Указывает ссылку bLOB-файла (в качестве URL-адреса) на BACPAC-файл.</span><span class="sxs-lookup"><span data-stu-id="b571e-152">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="b571e-153">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="b571e-153">-UseNetworkIsolation</span></span>
<span data-ttu-id="b571e-154">Если задается этот условия, будет создана частная ссылка для учетной записи хранения и (или) SQL сервера</span><span class="sxs-lookup"><span data-stu-id="b571e-154">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="b571e-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b571e-155">-Confirm</span></span>
<span data-ttu-id="b571e-156">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b571e-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b571e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b571e-157">-WhatIf</span></span>
<span data-ttu-id="b571e-158">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b571e-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b571e-159">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b571e-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b571e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b571e-160">CommonParameters</span></span>
<span data-ttu-id="b571e-161">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b571e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b571e-162">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b571e-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b571e-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b571e-163">INPUTS</span></span>

### <span data-ttu-id="b571e-164">System.String</span><span class="sxs-lookup"><span data-stu-id="b571e-164">System.String</span></span>

## <span data-ttu-id="b571e-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b571e-165">OUTPUTS</span></span>

### <span data-ttu-id="b571e-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="b571e-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="b571e-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b571e-167">NOTES</span></span>
* <span data-ttu-id="b571e-168">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="b571e-168">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="b571e-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b571e-169">RELATED LINKS</span></span>

[<span data-ttu-id="b571e-170">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="b571e-170">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="b571e-171">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="b571e-171">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="b571e-172">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="b571e-172">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
