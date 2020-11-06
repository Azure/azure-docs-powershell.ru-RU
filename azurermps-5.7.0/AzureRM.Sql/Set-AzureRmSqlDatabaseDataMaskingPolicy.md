---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 26d056b5ad9cdff22f0419f90fad17c3147e0e14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561356"
---
# <span data-ttu-id="80151-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="80151-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="80151-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80151-102">SYNOPSIS</span></span>
<span data-ttu-id="80151-103">Задает Маскирование данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="80151-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80151-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80151-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80151-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80151-105">DESCRIPTION</span></span>
<span data-ttu-id="80151-106">Командлет **Set-AzureRmSqlDatabaseDataMaskingPolicy** задает политику масок данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="80151-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="80151-107">Для использования этого командлета используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="80151-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="80151-108">Вы можете задать параметр *DataMaskingState* , чтобы указать, включены ли операции маскирования данных или выключены.</span><span class="sxs-lookup"><span data-stu-id="80151-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>

<span data-ttu-id="80151-109">Вы также можете задать параметр *PrivilegedLogins* , чтобы указать, какие пользователи могут видеть немаскированные данные.</span><span class="sxs-lookup"><span data-stu-id="80151-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="80151-110">Если командлет завершается успешно и используется параметр *PassThru* , он возвращает объект, описывающий текущую политику масок данных в дополнение к идентификаторам базы данных.</span><span class="sxs-lookup"><span data-stu-id="80151-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="80151-111">Идентификаторы баз данных включают, но не ограничиваются, **ResourceGroupName** , **ServerName** и **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="80151-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="80151-112">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="80151-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="80151-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80151-113">EXAMPLES</span></span>

### <span data-ttu-id="80151-114">Пример 1: Настройка политики маскирования данных для базы данных</span><span class="sxs-lookup"><span data-stu-id="80151-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="80151-115">Эта команда задает политику масок данных для базы данных с именем Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="80151-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="80151-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80151-116">PARAMETERS</span></span>

### <span data-ttu-id="80151-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="80151-117">-DatabaseName</span></span>
<span data-ttu-id="80151-118">Указывает имя базы данных, в которой задана политика.</span><span class="sxs-lookup"><span data-stu-id="80151-118">Specifies the name of the database where the policy is set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80151-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="80151-119">-DataMaskingState</span></span>
<span data-ttu-id="80151-120">Указывает, включена или отключена операция маскировки данных.</span><span class="sxs-lookup"><span data-stu-id="80151-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="80151-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="80151-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80151-122">Включаем</span><span class="sxs-lookup"><span data-stu-id="80151-122">Enabled</span></span>
- <span data-ttu-id="80151-123">Отключает</span><span class="sxs-lookup"><span data-stu-id="80151-123">Disabled</span></span>

<span data-ttu-id="80151-124">Значение по умолчанию — Enabled (включено).</span><span class="sxs-lookup"><span data-stu-id="80151-124">The default value is Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80151-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80151-125">-DefaultProfile</span></span>
<span data-ttu-id="80151-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="80151-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80151-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80151-127">-PassThru</span></span>
<span data-ttu-id="80151-128">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="80151-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="80151-129">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="80151-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80151-130">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="80151-130">-PrivilegedLogins</span></span>
<span data-ttu-id="80151-131">Указывает, какие пользователи SQL будут исключены из масок.</span><span class="sxs-lookup"><span data-stu-id="80151-131">Specifies which SQL users are excluded from masking.</span></span>

<span data-ttu-id="80151-132">Этот параметр устарел и будет удален из будущих выпусков.</span><span class="sxs-lookup"><span data-stu-id="80151-132">This parameter is deprecated and will be removed from future releases.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80151-133">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="80151-133">-PrivilegedUsers</span></span>
<span data-ttu-id="80151-134">Указывает список привилегированных идентификаторов пользователей, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="80151-134">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="80151-135">Этим пользователям разрешено просматривать данные с маскированием.</span><span class="sxs-lookup"><span data-stu-id="80151-135">These users are allowed to view the masking data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80151-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80151-136">-ResourceGroupName</span></span>
<span data-ttu-id="80151-137">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="80151-137">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80151-138">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="80151-138">-ServerName</span></span>
<span data-ttu-id="80151-139">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="80151-139">Specifies the name of the server hosting the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80151-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80151-140">-Confirm</span></span>
<span data-ttu-id="80151-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="80151-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80151-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80151-142">-WhatIf</span></span>
<span data-ttu-id="80151-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="80151-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80151-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="80151-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80151-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80151-145">CommonParameters</span></span>
<span data-ttu-id="80151-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80151-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80151-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80151-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80151-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80151-148">INPUTS</span></span>

### <span data-ttu-id="80151-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="80151-149">None</span></span>
<span data-ttu-id="80151-150">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="80151-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="80151-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80151-151">OUTPUTS</span></span>

### <span data-ttu-id="80151-152">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="80151-152">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="80151-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="80151-153">NOTES</span></span>

## <span data-ttu-id="80151-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80151-154">RELATED LINKS</span></span>

[<span data-ttu-id="80151-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="80151-155">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="80151-156">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="80151-156">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="80151-157">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="80151-157">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="80151-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="80151-158">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="80151-159">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="80151-159">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="80151-160">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="80151-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


