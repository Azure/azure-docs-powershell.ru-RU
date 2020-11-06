---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 34eedd81d5e8625ed957cba16d3cec1ea33a0c32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565111"
---
# <span data-ttu-id="9ed07-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="9ed07-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="9ed07-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ed07-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed07-103">Возвращает политику аудита сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9ed07-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ed07-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ed07-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ed07-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ed07-105">DESCRIPTION</span></span>
<span data-ttu-id="9ed07-106">Командлет **Get-AzureRmSqlServerAuditingPolicy** получает политику аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9ed07-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="9ed07-107">Укажите параметры *ResourceGroupName* , *ServerName* и *DatabaseName* , чтобы идентифицировать базу данных.</span><span class="sxs-lookup"><span data-stu-id="9ed07-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="9ed07-108">Этот командлет возвращает политику, которая используется в базах данных Azure SQL, которые определены в указанном сервере Azure SQL Server и используют его политику аудита.</span><span class="sxs-lookup"><span data-stu-id="9ed07-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="9ed07-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ed07-109">EXAMPLES</span></span>

### <span data-ttu-id="9ed07-110">Пример 1: получение политики аудита для Azure SQL Server с определенными для него разаудитом таблиц</span><span class="sxs-lookup"><span data-stu-id="9ed07-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="9ed07-111">Пример 2: получение политики аудита для Azure SQL Server с определенными аудитом больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="9ed07-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="9ed07-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ed07-112">PARAMETERS</span></span>

### <span data-ttu-id="9ed07-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed07-113">-ResourceGroupName</span></span>
<span data-ttu-id="9ed07-114">Указывает имя группы ресурсов, которой назначен Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9ed07-114">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="9ed07-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9ed07-115">-ServerName</span></span>
<span data-ttu-id="9ed07-116">Указывает имя сервера Azure SQL Server, для которого этот командлет получает политику аудита.</span><span class="sxs-lookup"><span data-stu-id="9ed07-116">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ed07-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ed07-117">-Confirm</span></span>
<span data-ttu-id="9ed07-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9ed07-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ed07-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ed07-119">-WhatIf</span></span>
<span data-ttu-id="9ed07-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9ed07-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ed07-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9ed07-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ed07-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed07-122">-DefaultProfile</span></span>
<span data-ttu-id="9ed07-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed07-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ed07-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed07-124">CommonParameters</span></span>
<span data-ttu-id="9ed07-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ed07-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed07-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ed07-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed07-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ed07-127">INPUTS</span></span>

## <span data-ttu-id="9ed07-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ed07-128">OUTPUTS</span></span>

### <span data-ttu-id="9ed07-129">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9ed07-129">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="9ed07-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ed07-130">NOTES</span></span>

## <span data-ttu-id="9ed07-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ed07-131">RELATED LINKS</span></span>

[<span data-ttu-id="9ed07-132">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="9ed07-132">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="9ed07-133">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="9ed07-133">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="9ed07-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="9ed07-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


