---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: ad0103e2a4d529a4f306749a1d55ca0b6eadc013
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906546"
---
# <span data-ttu-id="7e7d7-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7e7d7-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="7e7d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="7e7d7-103">Удаляет параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7e7d7-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="7e7d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e7d7-104">SYNTAX</span></span>

### <span data-ttu-id="7e7d7-105">DatabaseParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e7d7-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e7d7-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e7d7-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e7d7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e7d7-107">DESCRIPTION</span></span>
<span data-ttu-id="7e7d7-108">Командлет **Remove-AzSqlDatabaseAudit** удаляет параметры аудита для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7e7d7-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="7e7d7-109">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="7e7d7-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="7e7d7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e7d7-110">EXAMPLES</span></span>

### <span data-ttu-id="7e7d7-111">Пример 1: удаление параметров аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="7e7d7-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="7e7d7-112">Пример 2: удаление с помощью конвейера параметры аудита для базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="7e7d7-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="7e7d7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e7d7-113">PARAMETERS</span></span>

### <span data-ttu-id="7e7d7-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e7d7-114">-DatabaseName</span></span>
<span data-ttu-id="7e7d7-115">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="7e7d7-115">SQL Database name.</span></span>

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

### <span data-ttu-id="7e7d7-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7e7d7-116">-DatabaseObject</span></span>
<span data-ttu-id="7e7d7-117">Объект базы данных для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="7e7d7-117">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="7e7d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e7d7-118">-DefaultProfile</span></span>
<span data-ttu-id="7e7d7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e7d7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e7d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e7d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="7e7d7-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e7d7-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e7d7-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="7e7d7-122">-ServerName</span></span>
<span data-ttu-id="7e7d7-123">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7e7d7-123">SQL server name.</span></span>

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

### <span data-ttu-id="7e7d7-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e7d7-124">-Confirm</span></span>
<span data-ttu-id="7e7d7-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e7d7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e7d7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e7d7-126">-WhatIf</span></span>
<span data-ttu-id="7e7d7-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7e7d7-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e7d7-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e7d7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e7d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e7d7-129">CommonParameters</span></span>
<span data-ttu-id="7e7d7-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e7d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e7d7-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e7d7-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e7d7-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e7d7-132">INPUTS</span></span>

### <span data-ttu-id="7e7d7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7e7d7-133">System.String</span></span>

### <span data-ttu-id="7e7d7-134">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7e7d7-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="7e7d7-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e7d7-135">OUTPUTS</span></span>

### <span data-ttu-id="7e7d7-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e7d7-136">System.Boolean</span></span>

## <span data-ttu-id="7e7d7-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e7d7-137">NOTES</span></span>

## <span data-ttu-id="7e7d7-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e7d7-138">RELATED LINKS</span></span>
