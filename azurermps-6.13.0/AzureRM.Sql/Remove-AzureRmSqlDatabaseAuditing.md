---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D3BA6534-CAAC-41E2-8442-0606B712E2B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a7cf769b1150ef7e209bd02234674bb26927f9a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565789"
---
# <span data-ttu-id="d8054-101">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="d8054-101">Remove-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="d8054-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8054-102">SYNOPSIS</span></span>
<span data-ttu-id="d8054-103">Удаляет аудит базы данных.</span><span class="sxs-lookup"><span data-stu-id="d8054-103">Removes the auditing of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8054-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8054-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseAuditing [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8054-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8054-105">DESCRIPTION</span></span>
<span data-ttu-id="d8054-106">Командлет **Remove-AzureRmSqlDatabaseAuditing** удаляет аудит базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d8054-106">The **Remove-AzureRmSqlDatabaseAuditing** cmdlet removes the auditing of an Azure SQL database.</span></span>
<span data-ttu-id="d8054-107">Для использования этого командлета используйте параметры *ResourceGroupName* , *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="d8054-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d8054-108">После запуска этого командлета аудит базы данных не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8054-108">After you run this cmdlet, auditing of the database is not performed.</span></span>
<span data-ttu-id="d8054-109">Если команда пройдет успешно и вы использовали параметр *PassThru* , командлет возвращает объект, который описывает текущую политику аудита, а также идентификаторы базы данных.</span><span class="sxs-lookup"><span data-stu-id="d8054-109">If the command succeeds and you have used the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, in addition to the database identifiers.</span></span>
<span data-ttu-id="d8054-110">Идентификаторы базы данных включают (но не ограничиваются) **ResourceGroupName** , **ServerName** и **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="d8054-110">Database identifiers include, but are not limited to, the **ResourceGroupName** , **ServerName** and **DatabaseName**.</span></span>
<span data-ttu-id="d8054-111">Если вы удалите аудит базы данных Azure SQL, обнаружение угроз также будет удалено.</span><span class="sxs-lookup"><span data-stu-id="d8054-111">If you remove auditing of an Azure SQL database, threat detection is also removed.</span></span>
<span data-ttu-id="d8054-112">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="d8054-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d8054-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8054-113">EXAMPLES</span></span>

### <span data-ttu-id="d8054-114">Пример 1: удаление аудита базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="d8054-114">Example 1: Remove the auditing of an Azure SQL database</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d8054-115">Эта команда удаляет аудит базы данных с именем Database01.</span><span class="sxs-lookup"><span data-stu-id="d8054-115">This command removes the auditing of database named Database01.</span></span>
<span data-ttu-id="d8054-116">Эта база данных находится в Server01, которая назначена группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d8054-116">That database is located on Server01, which is assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="d8054-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8054-117">PARAMETERS</span></span>

### <span data-ttu-id="d8054-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8054-118">-DatabaseName</span></span>
<span data-ttu-id="d8054-119">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d8054-119">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="d8054-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8054-120">-DefaultProfile</span></span>
<span data-ttu-id="d8054-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d8054-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8054-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8054-122">-PassThru</span></span>
<span data-ttu-id="d8054-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d8054-123">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="d8054-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d8054-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d8054-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8054-125">-ResourceGroupName</span></span>
<span data-ttu-id="d8054-126">Указывает имя группы ресурсов, содержащей базу данных.</span><span class="sxs-lookup"><span data-stu-id="d8054-126">Specifies the name of the resource group containing the database.</span></span>

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

### <span data-ttu-id="d8054-127">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d8054-127">-ServerName</span></span>
<span data-ttu-id="d8054-128">Указывает имя сервера, содержащего базу данных.</span><span class="sxs-lookup"><span data-stu-id="d8054-128">Specifies the name of the server containing the database.</span></span>

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

### <span data-ttu-id="d8054-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8054-129">-Confirm</span></span>
<span data-ttu-id="d8054-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8054-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8054-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8054-131">-WhatIf</span></span>
<span data-ttu-id="d8054-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8054-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8054-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8054-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8054-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8054-134">CommonParameters</span></span>
<span data-ttu-id="d8054-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8054-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8054-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8054-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8054-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8054-137">INPUTS</span></span>

### <span data-ttu-id="d8054-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d8054-138">System.String</span></span>

## <span data-ttu-id="d8054-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8054-139">OUTPUTS</span></span>

### <span data-ttu-id="d8054-140">Microsoft. Azure. Commands. SQL. Audit. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d8054-140">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="d8054-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8054-141">NOTES</span></span>

## <span data-ttu-id="d8054-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8054-142">RELATED LINKS</span></span>

[<span data-ttu-id="d8054-143">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d8054-143">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d8054-144">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d8054-144">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d8054-145">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="d8054-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


