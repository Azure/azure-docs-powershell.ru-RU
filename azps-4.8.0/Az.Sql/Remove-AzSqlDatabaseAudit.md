---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: caca08a5a9390d3e80fdef8309244a8a4d29aec0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235808"
---
# <span data-ttu-id="d0cbd-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d0cbd-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="d0cbd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0cbd-102">SYNOPSIS</span></span>
<span data-ttu-id="d0cbd-103">Удаляет параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="d0cbd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0cbd-104">SYNTAX</span></span>

### <span data-ttu-id="d0cbd-105">DatabaseParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0cbd-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0cbd-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0cbd-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0cbd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0cbd-107">DESCRIPTION</span></span>
<span data-ttu-id="d0cbd-108">Командлет **Remove-AzSqlDatabaseAudit** удаляет параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="d0cbd-109">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="d0cbd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0cbd-110">EXAMPLES</span></span>

### <span data-ttu-id="d0cbd-111">Пример 1: удаление параметров аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="d0cbd-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="d0cbd-112">Пример 2: удаление с помощью конвейера параметры аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="d0cbd-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="d0cbd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0cbd-113">PARAMETERS</span></span>

### <span data-ttu-id="d0cbd-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0cbd-114">-DatabaseName</span></span>
<span data-ttu-id="d0cbd-115">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0cbd-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="d0cbd-116">-DatabaseObject</span></span>
<span data-ttu-id="d0cbd-117">Объект базы данных для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0cbd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0cbd-118">-DefaultProfile</span></span>
<span data-ttu-id="d0cbd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0cbd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0cbd-120">-ResourceGroupName</span></span>
<span data-ttu-id="d0cbd-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0cbd-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d0cbd-122">-ServerName</span></span>
<span data-ttu-id="d0cbd-123">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0cbd-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0cbd-124">-Confirm</span></span>
<span data-ttu-id="d0cbd-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0cbd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0cbd-126">-WhatIf</span></span>
<span data-ttu-id="d0cbd-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0cbd-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0cbd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0cbd-129">CommonParameters</span></span>
<span data-ttu-id="d0cbd-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0cbd-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0cbd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0cbd-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0cbd-132">INPUTS</span></span>

### <span data-ttu-id="d0cbd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d0cbd-133">System.String</span></span>

### <span data-ttu-id="d0cbd-134">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d0cbd-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d0cbd-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0cbd-135">OUTPUTS</span></span>

### <span data-ttu-id="d0cbd-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0cbd-136">System.Boolean</span></span>

## <span data-ttu-id="d0cbd-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0cbd-137">NOTES</span></span>

## <span data-ttu-id="d0cbd-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0cbd-138">RELATED LINKS</span></span>
