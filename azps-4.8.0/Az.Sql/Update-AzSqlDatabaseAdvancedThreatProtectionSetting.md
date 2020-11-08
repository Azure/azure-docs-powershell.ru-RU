---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 1bd5906ac4736fc2aace122070edfebe1e59fe3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235758"
---
# <span data-ttu-id="9dc22-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="9dc22-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="9dc22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9dc22-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc22-103">Задает дополнительные параметры защиты от угроз в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9dc22-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="9dc22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9dc22-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dc22-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dc22-105">DESCRIPTION</span></span>
<span data-ttu-id="9dc22-106">Командлет **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** задает расширенные параметры защиты от угроз в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9dc22-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="9dc22-107">Для включения расширенной защиты от угроз для базы данных параметры аудита должны быть включены в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="9dc22-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="9dc22-108">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* , *ServerName* и *DatabaseName* , чтобы идентифицировать базу данных.</span><span class="sxs-lookup"><span data-stu-id="9dc22-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="9dc22-109">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="9dc22-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9dc22-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9dc22-110">EXAMPLES</span></span>

### <span data-ttu-id="9dc22-111">Пример 1: Настройка расширенных параметров защиты от угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="9dc22-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="9dc22-112">Эта команда задает расширенные параметры защиты от угроз для базы данных с именем Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="9dc22-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="9dc22-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9dc22-113">PARAMETERS</span></span>

### <span data-ttu-id="9dc22-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9dc22-114">-DatabaseName</span></span>
<span data-ttu-id="9dc22-115">Указывает имя базы данных, в которой заданы параметры.</span><span class="sxs-lookup"><span data-stu-id="9dc22-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="9dc22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc22-116">-DefaultProfile</span></span>
<span data-ttu-id="9dc22-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9dc22-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dc22-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="9dc22-118">-EmailAdmins</span></span>
<span data-ttu-id="9dc22-119">Указывает, имеют ли дополнительные параметры защиты от угроз администраторам контакты с помощью электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9dc22-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc22-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="9dc22-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="9dc22-121">Указывает массив типов обнаружения, исключаемых из параметров.</span><span class="sxs-lookup"><span data-stu-id="9dc22-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="9dc22-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9dc22-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9dc22-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="9dc22-123">Sql_Injection</span></span> 
- <span data-ttu-id="9dc22-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="9dc22-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="9dc22-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="9dc22-125">Access_Anomaly</span></span> 
- <span data-ttu-id="9dc22-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="9dc22-126">None</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc22-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="9dc22-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="9dc22-128">Указывает список адресов электронной почты, разделенных точкой с запятой, по которым параметры отправляют оповещения.</span><span class="sxs-lookup"><span data-stu-id="9dc22-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="9dc22-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dc22-129">-PassThru</span></span>
<span data-ttu-id="9dc22-130">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9dc22-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9dc22-131">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9dc22-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9dc22-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dc22-132">-ResourceGroupName</span></span>
<span data-ttu-id="9dc22-133">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="9dc22-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9dc22-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9dc22-134">-RetentionInDays</span></span>
<span data-ttu-id="9dc22-135">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="9dc22-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="9dc22-136">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9dc22-136">-ServerName</span></span>
<span data-ttu-id="9dc22-137">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="9dc22-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="9dc22-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9dc22-138">-StorageAccountName</span></span>
<span data-ttu-id="9dc22-139">Указывает имя учетной записи хранения, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="9dc22-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="9dc22-140">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="9dc22-140">Wildcards are not permitted.</span></span> <span data-ttu-id="9dc22-141">Этот параметр не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9dc22-141">This parameter is not required.</span></span> <span data-ttu-id="9dc22-142">Если этот параметр не указан, командлет будет использовать учетную запись хранения, которая была ранее определена как часть параметров расширенной защиты от угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="9dc22-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="9dc22-143">Если при первом определении параметров защиты от угроз для базы данных этот параметр не указан, командлет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="9dc22-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="9dc22-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dc22-144">-Confirm</span></span>
<span data-ttu-id="9dc22-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9dc22-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dc22-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dc22-146">-WhatIf</span></span>
<span data-ttu-id="9dc22-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9dc22-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dc22-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9dc22-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dc22-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc22-149">CommonParameters</span></span>
<span data-ttu-id="9dc22-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9dc22-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc22-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dc22-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc22-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9dc22-152">INPUTS</span></span>

### <span data-ttu-id="9dc22-153">System. String</span><span class="sxs-lookup"><span data-stu-id="9dc22-153">System.String</span></span>

### <span data-ttu-id="9dc22-154">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9dc22-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9dc22-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="9dc22-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="9dc22-156">System. Nullable "1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9dc22-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9dc22-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dc22-157">OUTPUTS</span></span>

### <span data-ttu-id="9dc22-158">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="9dc22-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="9dc22-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="9dc22-159">NOTES</span></span>

## <span data-ttu-id="9dc22-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dc22-160">RELATED LINKS</span></span>

[<span data-ttu-id="9dc22-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="9dc22-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="9dc22-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="9dc22-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="9dc22-163">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="9dc22-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


