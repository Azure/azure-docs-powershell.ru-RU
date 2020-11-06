---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 8480037bf4b756a03a40ad1c1dff01ab1d28ac69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566263"
---
# <span data-ttu-id="dddaf-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="dddaf-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="dddaf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dddaf-102">SYNOPSIS</span></span>
<span data-ttu-id="dddaf-103">Изменяет параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddaf-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dddaf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dddaf-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dddaf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dddaf-105">DESCRIPTION</span></span>
<span data-ttu-id="dddaf-106">Командлет **Set-AzureRmSqlServerAuditing** изменяет параметры аудита для Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddaf-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="dddaf-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* и *ServerName* для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="dddaf-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="dddaf-108">Укажите параметр *StorageAccountName* , чтобы указать учетную запись хранения для журналов аудита и параметр *StorageKeyType* , чтобы определить ключи хранилища.</span><span class="sxs-lookup"><span data-stu-id="dddaf-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="dddaf-109">Используйте параметр *State* для включения или отключения политики.</span><span class="sxs-lookup"><span data-stu-id="dddaf-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="dddaf-110">Вы также можете определить хранение журналов аудита, задав значение параметра *RetentionInDays* , чтобы определить период для журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="dddaf-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="dddaf-111">После успешного выполнения командлета выполняется аудит баз данных Azure SQL Server, определенных в указанном сервере Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dddaf-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="dddaf-112">Если командлет завершился успешно и вы используете параметр *PassThru* , он возвращает объект, описывающий текущую политику аудита BLOB-объектов, в дополнение к идентификаторам сервера.</span><span class="sxs-lookup"><span data-stu-id="dddaf-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="dddaf-113">Идентификаторы сервера включают, но не ограничиваются **ResourceGroupName** и **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="dddaf-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="dddaf-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dddaf-114">EXAMPLES</span></span>

### <span data-ttu-id="dddaf-115">Пример 1: Включение политики аудита для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="dddaf-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="dddaf-116">Пример 2: отключение политики аудита для Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="dddaf-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="dddaf-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dddaf-117">PARAMETERS</span></span>

### <span data-ttu-id="dddaf-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="dddaf-118">-AuditActionGroup</span></span>
<span data-ttu-id="dddaf-119">Набор групп действий аудита</span><span class="sxs-lookup"><span data-stu-id="dddaf-119">The set of the audit action groups</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases: 
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddaf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dddaf-120">-PassThru</span></span>
<span data-ttu-id="dddaf-121">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="dddaf-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="dddaf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dddaf-122">-ResourceGroupName</span></span>
<span data-ttu-id="dddaf-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dddaf-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="dddaf-124">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="dddaf-124">-RetentionInDays</span></span>
<span data-ttu-id="dddaf-125">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="dddaf-125">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddaf-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="dddaf-126">-ServerName</span></span>
<span data-ttu-id="dddaf-127">Имя сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dddaf-127">SQL server name.</span></span>

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

### <span data-ttu-id="dddaf-128">-State</span><span class="sxs-lookup"><span data-stu-id="dddaf-128">-State</span></span>
<span data-ttu-id="dddaf-129">Состояние политики аудита</span><span class="sxs-lookup"><span data-stu-id="dddaf-129">The state of the auditing policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddaf-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dddaf-130">-StorageAccountName</span></span>
<span data-ttu-id="dddaf-131">Имя учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="dddaf-131">The name of the storage account</span></span>

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

### <span data-ttu-id="dddaf-132">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="dddaf-132">-StorageKeyType</span></span>
<span data-ttu-id="dddaf-133">Тип ключа хранилища</span><span class="sxs-lookup"><span data-stu-id="dddaf-133">The type of the storage key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dddaf-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dddaf-134">-Confirm</span></span>
<span data-ttu-id="dddaf-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dddaf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dddaf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dddaf-136">-WhatIf</span></span>
<span data-ttu-id="dddaf-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dddaf-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dddaf-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dddaf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dddaf-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dddaf-139">-DefaultProfile</span></span>
<span data-ttu-id="dddaf-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dddaf-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dddaf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dddaf-141">CommonParameters</span></span>
<span data-ttu-id="dddaf-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dddaf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dddaf-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dddaf-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dddaf-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dddaf-144">INPUTS</span></span>

## <span data-ttu-id="dddaf-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dddaf-145">OUTPUTS</span></span>

### <span data-ttu-id="dddaf-146">Microsoft. Azure. Commands. SQL. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="dddaf-146">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="dddaf-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="dddaf-147">NOTES</span></span>

## <span data-ttu-id="dddaf-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dddaf-148">RELATED LINKS</span></span>

