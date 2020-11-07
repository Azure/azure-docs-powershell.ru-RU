---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: e0af0c6d741e45c2e00e958342fad940acc2c3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728798"
---
# <span data-ttu-id="b62aa-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="b62aa-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="b62aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b62aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b62aa-103">Задает Маскирование данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="b62aa-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="b62aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b62aa-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b62aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b62aa-105">DESCRIPTION</span></span>
<span data-ttu-id="b62aa-106">Командлет **Set-AzSqlDatabaseDataMaskingPolicy** задает политику масок данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b62aa-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="b62aa-107">Для использования этого командлета используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="b62aa-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="b62aa-108">Вы можете задать параметр *DataMaskingState* , чтобы указать, включены ли операции маскирования данных или выключены.</span><span class="sxs-lookup"><span data-stu-id="b62aa-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="b62aa-109">Если командлет завершается успешно и используется параметр *PassThru* , он возвращает объект, описывающий текущую политику масок данных в дополнение к идентификаторам базы данных.</span><span class="sxs-lookup"><span data-stu-id="b62aa-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="b62aa-110">Идентификаторы баз данных включают, но не ограничиваются, **ResourceGroupName** , **ServerName** и **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="b62aa-110">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="b62aa-111">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="b62aa-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b62aa-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b62aa-112">EXAMPLES</span></span>

### <span data-ttu-id="b62aa-113">Пример 1: Настройка политики маскирования данных для базы данных</span><span class="sxs-lookup"><span data-stu-id="b62aa-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="b62aa-114">Эта команда задает политику масок данных для базы данных с именем Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="b62aa-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="b62aa-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b62aa-115">PARAMETERS</span></span>

### <span data-ttu-id="b62aa-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b62aa-116">-DatabaseName</span></span>
<span data-ttu-id="b62aa-117">Указывает имя базы данных, в которой задана политика.</span><span class="sxs-lookup"><span data-stu-id="b62aa-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="b62aa-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="b62aa-118">-DataMaskingState</span></span>
<span data-ttu-id="b62aa-119">Указывает, включена или отключена операция маскировки данных.</span><span class="sxs-lookup"><span data-stu-id="b62aa-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="b62aa-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b62aa-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b62aa-121">Включаем</span><span class="sxs-lookup"><span data-stu-id="b62aa-121">Enabled</span></span>
- <span data-ttu-id="b62aa-122">Отключено значение по умолчанию — Enabled.</span><span class="sxs-lookup"><span data-stu-id="b62aa-122">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62aa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62aa-123">-DefaultProfile</span></span>
<span data-ttu-id="b62aa-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b62aa-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b62aa-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b62aa-125">-PassThru</span></span>
<span data-ttu-id="b62aa-126">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b62aa-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b62aa-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b62aa-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b62aa-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="b62aa-128">-PrivilegedUsers</span></span>
<span data-ttu-id="b62aa-129">Указывает список привилегированных идентификаторов пользователей, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="b62aa-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="b62aa-130">Этим пользователям разрешено просматривать данные с маскированием.</span><span class="sxs-lookup"><span data-stu-id="b62aa-130">These users are allowed to view the masking data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62aa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b62aa-131">-ResourceGroupName</span></span>
<span data-ttu-id="b62aa-132">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="b62aa-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b62aa-133">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b62aa-133">-ServerName</span></span>
<span data-ttu-id="b62aa-134">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="b62aa-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="b62aa-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b62aa-135">-Confirm</span></span>
<span data-ttu-id="b62aa-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b62aa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b62aa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b62aa-137">-WhatIf</span></span>
<span data-ttu-id="b62aa-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b62aa-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b62aa-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b62aa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b62aa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62aa-140">CommonParameters</span></span>
<span data-ttu-id="b62aa-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b62aa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62aa-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b62aa-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62aa-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b62aa-143">INPUTS</span></span>

### <span data-ttu-id="b62aa-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b62aa-144">System.String</span></span>

## <span data-ttu-id="b62aa-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b62aa-145">OUTPUTS</span></span>

### <span data-ttu-id="b62aa-146">Microsoft. Azure. Commands. SQL. маскирует. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b62aa-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="b62aa-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="b62aa-147">NOTES</span></span>

## <span data-ttu-id="b62aa-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b62aa-148">RELATED LINKS</span></span>

[<span data-ttu-id="b62aa-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="b62aa-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="b62aa-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b62aa-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b62aa-151">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b62aa-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b62aa-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b62aa-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b62aa-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="b62aa-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="b62aa-154">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="b62aa-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


