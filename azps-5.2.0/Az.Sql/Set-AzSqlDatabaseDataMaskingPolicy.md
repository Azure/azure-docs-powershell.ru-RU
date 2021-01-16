---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407652"
---
# <span data-ttu-id="78707-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="78707-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="78707-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78707-102">SYNOPSIS</span></span>
<span data-ttu-id="78707-103">Задает маску данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="78707-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="78707-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78707-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78707-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78707-105">DESCRIPTION</span></span>
<span data-ttu-id="78707-106">Для базы данных Azure SQL политика маскровки данных задана с SQL **AzSqlDataBaseDataMaskingPolicy.**</span><span class="sxs-lookup"><span data-stu-id="78707-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="78707-107">Чтобы использовать этот cmdlet, используйте параметры *ResourceGroupName,* *ServerName* и *DatabaseName* для определения базы данных.</span><span class="sxs-lookup"><span data-stu-id="78707-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="78707-108">Вы можете задать параметр *DataMaskingState,* чтобы указать, включены ли операции маскровки данных.</span><span class="sxs-lookup"><span data-stu-id="78707-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="78707-109">В случае успешного использования параметра *PassThru* возвращается объект, в дополнение к идентификаторам базы данных, который описывает текущую политику маскровки данных.</span><span class="sxs-lookup"><span data-stu-id="78707-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="78707-110">Идентификаторы баз данных включают, но не ограничив их, **ResourceGroupName,** **ServerName** и **DatabaseName.**</span><span class="sxs-lookup"><span data-stu-id="78707-110">Database identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, and **DatabaseName**.</span></span>
<span data-ttu-id="78707-111">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="78707-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="78707-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78707-112">EXAMPLES</span></span>

### <span data-ttu-id="78707-113">Пример 1. Настройка политики маскровки данных для базы данных</span><span class="sxs-lookup"><span data-stu-id="78707-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="78707-114">Эта команда задает политику маскровки данных для базы данных с именем database01 на сервере с именем server01.</span><span class="sxs-lookup"><span data-stu-id="78707-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="78707-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78707-115">PARAMETERS</span></span>

### <span data-ttu-id="78707-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="78707-116">-DatabaseName</span></span>
<span data-ttu-id="78707-117">Указывает имя базы данных, для которой задана политика.</span><span class="sxs-lookup"><span data-stu-id="78707-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="78707-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="78707-118">-DataMaskingState</span></span>
<span data-ttu-id="78707-119">Указывает, включена ли или отключена операция маскровки данных.</span><span class="sxs-lookup"><span data-stu-id="78707-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="78707-120">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="78707-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="78707-121">Включено</span><span class="sxs-lookup"><span data-stu-id="78707-121">Enabled</span></span>
- <span data-ttu-id="78707-122">Отключено значение по умолчанию включено.</span><span class="sxs-lookup"><span data-stu-id="78707-122">Disabled The default value is Enabled.</span></span>

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

### <span data-ttu-id="78707-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78707-123">-DefaultProfile</span></span>
<span data-ttu-id="78707-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="78707-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78707-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78707-125">-PassThru</span></span>
<span data-ttu-id="78707-126">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="78707-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78707-127">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="78707-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="78707-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="78707-128">-PrivilegedUsers</span></span>
<span data-ttu-id="78707-129">Список привилегированных ид пользователей, разделенных заточкими.</span><span class="sxs-lookup"><span data-stu-id="78707-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="78707-130">Таким пользователям разрешено просматривать маскировать данные.</span><span class="sxs-lookup"><span data-stu-id="78707-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="78707-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78707-131">-ResourceGroupName</span></span>
<span data-ttu-id="78707-132">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="78707-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="78707-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="78707-133">-ServerName</span></span>
<span data-ttu-id="78707-134">Указывает имя сервера, на который размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="78707-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="78707-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78707-135">-Confirm</span></span>
<span data-ttu-id="78707-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="78707-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78707-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78707-137">-WhatIf</span></span>
<span data-ttu-id="78707-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78707-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78707-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="78707-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78707-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78707-140">CommonParameters</span></span>
<span data-ttu-id="78707-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78707-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78707-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78707-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78707-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78707-143">INPUTS</span></span>

### <span data-ttu-id="78707-144">System.String</span><span class="sxs-lookup"><span data-stu-id="78707-144">System.String</span></span>

## <span data-ttu-id="78707-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78707-145">OUTPUTS</span></span>

### <span data-ttu-id="78707-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="78707-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="78707-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78707-147">NOTES</span></span>

## <span data-ttu-id="78707-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78707-148">RELATED LINKS</span></span>

[<span data-ttu-id="78707-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="78707-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="78707-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="78707-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="78707-151">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="78707-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="78707-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="78707-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="78707-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="78707-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="78707-154">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="78707-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


