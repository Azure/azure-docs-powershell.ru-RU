---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 18d387aeb8ca9e777af0767ce407e373fc2adf09
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236607"
---
# <span data-ttu-id="eae1b-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="eae1b-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="eae1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eae1b-102">SYNOPSIS</span></span>
<span data-ttu-id="eae1b-103">Возвращает базу данных и ее развернутые значения свойств.</span><span class="sxs-lookup"><span data-stu-id="eae1b-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="eae1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eae1b-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eae1b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eae1b-105">DESCRIPTION</span></span>
<span data-ttu-id="eae1b-106">Командлет **Get-AzSqlDatabaseExpanded** получает базу данных и ее развернутые значения свойств.</span><span class="sxs-lookup"><span data-stu-id="eae1b-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="eae1b-107">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="eae1b-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="eae1b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eae1b-108">EXAMPLES</span></span>

### <span data-ttu-id="eae1b-109">Пример 1: получение объекта базы данных с данными советника по уровню обслуживания</span><span class="sxs-lookup"><span data-stu-id="eae1b-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="eae1b-110">Эта команда возвращает базу данных с развернутыми свойствами, содержащими данные советника по уровню обслуживания.</span><span class="sxs-lookup"><span data-stu-id="eae1b-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="eae1b-111">Пример 2: перечисление объектов базы данных с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="eae1b-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="eae1b-112">Эта команда возвращает развернутый объект базы данных для всех баз данных в Server01, которые начинаются с "Database".</span><span class="sxs-lookup"><span data-stu-id="eae1b-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="eae1b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eae1b-113">PARAMETERS</span></span>

### <span data-ttu-id="eae1b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eae1b-114">-DatabaseName</span></span>
<span data-ttu-id="eae1b-115">Указывает имя базы данных, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="eae1b-115">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="eae1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eae1b-116">-DefaultProfile</span></span>
<span data-ttu-id="eae1b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eae1b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eae1b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eae1b-118">-ResourceGroupName</span></span>
<span data-ttu-id="eae1b-119">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="eae1b-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="eae1b-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="eae1b-120">-ServerName</span></span>
<span data-ttu-id="eae1b-121">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="eae1b-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="eae1b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eae1b-122">-Confirm</span></span>
<span data-ttu-id="eae1b-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eae1b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eae1b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eae1b-124">-WhatIf</span></span>
<span data-ttu-id="eae1b-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eae1b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eae1b-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eae1b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eae1b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eae1b-127">CommonParameters</span></span>
<span data-ttu-id="eae1b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eae1b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eae1b-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eae1b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eae1b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eae1b-130">INPUTS</span></span>

### <span data-ttu-id="eae1b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="eae1b-131">System.String</span></span>

## <span data-ttu-id="eae1b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eae1b-132">OUTPUTS</span></span>

### <span data-ttu-id="eae1b-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="eae1b-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="eae1b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="eae1b-134">NOTES</span></span>

## <span data-ttu-id="eae1b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eae1b-135">RELATED LINKS</span></span>

[<span data-ttu-id="eae1b-136">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="eae1b-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
