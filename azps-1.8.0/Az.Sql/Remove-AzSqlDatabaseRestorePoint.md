---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 0351e720d2f9a93a8c3a4a220c6a4d8844ebfecd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728857"
---
# <span data-ttu-id="e6377-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="e6377-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="e6377-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6377-102">SYNOPSIS</span></span>
<span data-ttu-id="e6377-103">Удаляет указанную точку восстановления из базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e6377-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="e6377-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6377-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6377-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6377-105">DESCRIPTION</span></span>
<span data-ttu-id="e6377-106">Командлет **Remove-AzSqlDatabaseRestorePoint** удаляет указанную точку восстановления из базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e6377-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="e6377-107">Этот командлет в настоящее время поддерживается службой хранилища данных SQL Server в Azure.</span><span class="sxs-lookup"><span data-stu-id="e6377-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="e6377-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6377-108">EXAMPLES</span></span>

### <span data-ttu-id="e6377-109">Пример 1: Удаление точки восстановления</span><span class="sxs-lookup"><span data-stu-id="e6377-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="e6377-110">Эта команда удаляет точку восстановления для базы данных SQL Azure, заданной датой создания.</span><span class="sxs-lookup"><span data-stu-id="e6377-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="e6377-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6377-111">PARAMETERS</span></span>

### <span data-ttu-id="e6377-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e6377-112">-DatabaseName</span></span>
<span data-ttu-id="e6377-113">Указывает имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e6377-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="e6377-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6377-114">-DefaultProfile</span></span>
<span data-ttu-id="e6377-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e6377-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6377-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6377-116">-PassThru</span></span>
<span data-ttu-id="e6377-117">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="e6377-117">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6377-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6377-118">-ResourceGroupName</span></span>
<span data-ttu-id="e6377-119">Указывает имя группы ресурсов, которой назначена база данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e6377-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="e6377-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="e6377-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="e6377-121">Указывает дату создания точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="e6377-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6377-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e6377-122">-ServerName</span></span>
<span data-ttu-id="e6377-123">Указывает имя сервера AzureSQL, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="e6377-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="e6377-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6377-124">-Confirm</span></span>
<span data-ttu-id="e6377-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e6377-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6377-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6377-126">-WhatIf</span></span>
<span data-ttu-id="e6377-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e6377-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6377-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6377-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6377-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6377-129">CommonParameters</span></span>
<span data-ttu-id="e6377-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6377-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6377-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6377-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6377-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6377-132">INPUTS</span></span>

### <span data-ttu-id="e6377-133">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="e6377-133">System.DateTime</span></span>

### <span data-ttu-id="e6377-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e6377-134">System.String</span></span>

## <span data-ttu-id="e6377-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6377-135">OUTPUTS</span></span>

### <span data-ttu-id="e6377-136">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="e6377-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="e6377-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6377-137">NOTES</span></span>

## <span data-ttu-id="e6377-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6377-138">RELATED LINKS</span></span>
