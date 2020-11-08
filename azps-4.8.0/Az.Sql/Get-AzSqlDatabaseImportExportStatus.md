---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: c64f726e8ff553aa42cb8580cee2349b35de519e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243264"
---
# <span data-ttu-id="0c024-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="0c024-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="0c024-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c024-102">SYNOPSIS</span></span>
<span data-ttu-id="0c024-103">Получает подробные сведения о импорте или экспорте базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0c024-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="0c024-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c024-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c024-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c024-105">DESCRIPTION</span></span>
<span data-ttu-id="0c024-106">Командлет **Get-AzSqlDatabaseImportExportStatus** получает сведения о файле BACPAC — импорт из учетной записи хранения в базу данных Azure SQL или экспорт базы данных SQL Azure в качестве BACPAC-файла в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="0c024-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="0c024-107">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="0c024-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0c024-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c024-108">EXAMPLES</span></span>

### <span data-ttu-id="0c024-109">Пример 1: получение состояния импорта и экспорта базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="0c024-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="0c024-110">Эта команда возвращает состояние запроса на импорт или экспорт для базы данных по указанному URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="0c024-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="0c024-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c024-111">PARAMETERS</span></span>

### <span data-ttu-id="0c024-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c024-112">-DefaultProfile</span></span>
<span data-ttu-id="0c024-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0c024-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c024-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="0c024-114">-OperationStatusLink</span></span>
<span data-ttu-id="0c024-115">Указывает ссылку на состояние, возвращаемую командлетами New-AzSqlDatabaseExport и New-AzSqlDatabaseImport.</span><span class="sxs-lookup"><span data-stu-id="0c024-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="0c024-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c024-116">-Confirm</span></span>
<span data-ttu-id="0c024-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0c024-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c024-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c024-118">-WhatIf</span></span>
<span data-ttu-id="0c024-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0c024-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c024-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0c024-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c024-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c024-121">CommonParameters</span></span>
<span data-ttu-id="0c024-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c024-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c024-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c024-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c024-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c024-124">INPUTS</span></span>

### <span data-ttu-id="0c024-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0c024-125">System.String</span></span>

## <span data-ttu-id="0c024-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c024-126">OUTPUTS</span></span>

### <span data-ttu-id="0c024-127">Microsoft. Azure. Commands. SQL. ImportExport. Model. AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="0c024-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="0c024-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c024-128">NOTES</span></span>
* <span data-ttu-id="0c024-129">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="0c024-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="0c024-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c024-130">RELATED LINKS</span></span>

[<span data-ttu-id="0c024-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="0c024-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="0c024-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="0c024-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="0c024-133">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="0c024-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
