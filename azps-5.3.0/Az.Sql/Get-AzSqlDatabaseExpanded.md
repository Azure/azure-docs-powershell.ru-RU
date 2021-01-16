---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 18d387aeb8ca9e777af0767ce407e373fc2adf09
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419383"
---
# <span data-ttu-id="1ec76-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="1ec76-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="1ec76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ec76-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec76-103">Получает базу данных и значения ее расширенных свойств.</span><span class="sxs-lookup"><span data-stu-id="1ec76-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="1ec76-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1ec76-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ec76-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ec76-105">DESCRIPTION</span></span>
<span data-ttu-id="1ec76-106">Cmdlet **Get-AzSqlDatabaseExpanded** получает базу данных и значения ее расширенных свойств.</span><span class="sxs-lookup"><span data-stu-id="1ec76-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="1ec76-107">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec76-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1ec76-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1ec76-108">EXAMPLES</span></span>

### <span data-ttu-id="1ec76-109">Пример 1. Получить объект базы данных со сведениями консультанта уровня обслуживания</span><span class="sxs-lookup"><span data-stu-id="1ec76-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="1ec76-110">Эта команда возвращает базу данных с расширенными свойствами, которые содержат сведения помощника для уровня обслуживания.</span><span class="sxs-lookup"><span data-stu-id="1ec76-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="1ec76-111">Пример 2. Список объектов базы данных с использованием фильтрации</span><span class="sxs-lookup"><span data-stu-id="1ec76-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="1ec76-112">Эта команда возвращает расширенный объект базы данных для всех баз данных Сервера01, которые начинаются с "База данных".</span><span class="sxs-lookup"><span data-stu-id="1ec76-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="1ec76-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ec76-113">PARAMETERS</span></span>

### <span data-ttu-id="1ec76-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1ec76-114">-DatabaseName</span></span>
<span data-ttu-id="1ec76-115">Имя базы данных, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="1ec76-115">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec76-116">-DefaultProfile</span></span>
<span data-ttu-id="1ec76-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1ec76-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ec76-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec76-118">-ResourceGroupName</span></span>
<span data-ttu-id="1ec76-119">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="1ec76-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1ec76-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1ec76-120">-ServerName</span></span>
<span data-ttu-id="1ec76-121">Имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="1ec76-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1ec76-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ec76-122">-Confirm</span></span>
<span data-ttu-id="1ec76-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ec76-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ec76-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec76-124">-WhatIf</span></span>
<span data-ttu-id="1ec76-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ec76-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ec76-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1ec76-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ec76-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec76-127">CommonParameters</span></span>
<span data-ttu-id="1ec76-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec76-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec76-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ec76-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec76-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ec76-130">INPUTS</span></span>

### <span data-ttu-id="1ec76-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1ec76-131">System.String</span></span>

## <span data-ttu-id="1ec76-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1ec76-132">OUTPUTS</span></span>

### <span data-ttu-id="1ec76-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="1ec76-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="1ec76-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1ec76-134">NOTES</span></span>

## <span data-ttu-id="1ec76-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ec76-135">RELATED LINKS</span></span>

[<span data-ttu-id="1ec76-136">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="1ec76-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
