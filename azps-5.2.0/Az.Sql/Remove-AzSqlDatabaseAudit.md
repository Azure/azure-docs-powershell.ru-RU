---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: caca08a5a9390d3e80fdef8309244a8a4d29aec0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327897"
---
# <span data-ttu-id="9f9d2-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="9f9d2-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="9f9d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f9d2-102">SYNOPSIS</span></span>
<span data-ttu-id="9f9d2-103">Удаляет параметры аудита базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="9f9d2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f9d2-104">SYNTAX</span></span>

### <span data-ttu-id="9f9d2-105">DatabaseParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f9d2-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f9d2-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f9d2-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f9d2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f9d2-107">DESCRIPTION</span></span>
<span data-ttu-id="9f9d2-108">Для **удаления azSqlDatabaseAudit** удаляются параметры аудита для базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="9f9d2-109">Чтобы использовать этот cmdlet, используйте *параметры ResourceGroupName,* *ServerName* и *DatabaseName* для определения базы данных.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="9f9d2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f9d2-110">EXAMPLES</span></span>

### <span data-ttu-id="9f9d2-111">Пример 1. Удаление параметров аудита базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="9f9d2-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="9f9d2-112">Пример 2. Удаление через канал параметров аудита базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="9f9d2-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="9f9d2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f9d2-113">PARAMETERS</span></span>

### <span data-ttu-id="9f9d2-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9f9d2-114">-DatabaseName</span></span>
<span data-ttu-id="9f9d2-115">SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-115">SQL Database name.</span></span>

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

### <span data-ttu-id="9f9d2-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9f9d2-116">-DatabaseObject</span></span>
<span data-ttu-id="9f9d2-117">Объект базы данных для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-117">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="9f9d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f9d2-118">-DefaultProfile</span></span>
<span data-ttu-id="9f9d2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f9d2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f9d2-120">-ResourceGroupName</span></span>
<span data-ttu-id="9f9d2-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="9f9d2-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9f9d2-122">-ServerName</span></span>
<span data-ttu-id="9f9d2-123">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-123">SQL server name.</span></span>

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

### <span data-ttu-id="9f9d2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f9d2-124">-Confirm</span></span>
<span data-ttu-id="9f9d2-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f9d2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f9d2-126">-WhatIf</span></span>
<span data-ttu-id="9f9d2-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f9d2-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f9d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f9d2-129">CommonParameters</span></span>
<span data-ttu-id="9f9d2-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f9d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f9d2-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f9d2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f9d2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f9d2-132">INPUTS</span></span>

### <span data-ttu-id="9f9d2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9f9d2-133">System.String</span></span>

### <span data-ttu-id="9f9d2-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9f9d2-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="9f9d2-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f9d2-135">OUTPUTS</span></span>

### <span data-ttu-id="9f9d2-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f9d2-136">System.Boolean</span></span>

## <span data-ttu-id="9f9d2-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f9d2-137">NOTES</span></span>

## <span data-ttu-id="9f9d2-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f9d2-138">RELATED LINKS</span></span>
