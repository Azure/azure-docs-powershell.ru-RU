---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 1660c92ef4bef4cd832bc60506f7ef24d8927313
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570059"
---
# <span data-ttu-id="5e291-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5e291-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="5e291-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e291-102">SYNOPSIS</span></span>
<span data-ttu-id="5e291-103">Удаляет базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5e291-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e291-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e291-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e291-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e291-105">DESCRIPTION</span></span>
<span data-ttu-id="5e291-106">Командлет **Remove-AzureRmSqlDatabase** удаляет базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5e291-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="5e291-107">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="5e291-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5e291-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e291-108">EXAMPLES</span></span>

### <span data-ttu-id="5e291-109">Пример 1: Удаление базы данных из Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="5e291-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="5e291-110">Эта команда удаляет базу данных с именем Database01 из сервера SERVER01.</span><span class="sxs-lookup"><span data-stu-id="5e291-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="5e291-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e291-111">PARAMETERS</span></span>

### <span data-ttu-id="5e291-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e291-112">-DatabaseName</span></span>
<span data-ttu-id="5e291-113">Указывает имя базы данных, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5e291-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e291-114">-Force</span><span class="sxs-lookup"><span data-stu-id="5e291-114">-Force</span></span>
<span data-ttu-id="5e291-115">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5e291-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5e291-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e291-116">-ResourceGroupName</span></span>
<span data-ttu-id="5e291-117">Указывает имя группы ресурсов Azure, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="5e291-117">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5e291-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5e291-118">-ServerName</span></span>
<span data-ttu-id="5e291-119">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="5e291-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5e291-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e291-120">-Confirm</span></span>
<span data-ttu-id="5e291-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5e291-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e291-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e291-122">-WhatIf</span></span>
<span data-ttu-id="5e291-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5e291-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e291-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5e291-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e291-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e291-125">-DefaultProfile</span></span>
<span data-ttu-id="5e291-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e291-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e291-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e291-127">CommonParameters</span></span>
<span data-ttu-id="5e291-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e291-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e291-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e291-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e291-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e291-130">INPUTS</span></span>

### <span data-ttu-id="5e291-131">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5e291-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5e291-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e291-132">OUTPUTS</span></span>

### <span data-ttu-id="5e291-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5e291-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5e291-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e291-134">NOTES</span></span>

## <span data-ttu-id="5e291-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e291-135">RELATED LINKS</span></span>

[<span data-ttu-id="5e291-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5e291-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="5e291-137">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5e291-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="5e291-138">Возобновить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5e291-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="5e291-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5e291-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="5e291-140">Приостановить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5e291-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="5e291-141">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="5e291-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


