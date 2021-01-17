---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 1bd5906ac4736fc2aace122070edfebe1e59fe3f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393063"
---
# <span data-ttu-id="9b331-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="9b331-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="9b331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b331-102">SYNOPSIS</span></span>
<span data-ttu-id="9b331-103">Задает дополнительные параметры защиты от угроз в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9b331-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="9b331-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b331-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b331-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b331-105">DESCRIPTION</span></span>
<span data-ttu-id="9b331-106">С **его** использованием можно настраивать дополнительные параметры защиты от угроз в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9b331-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="9b331-107">Чтобы включить в базе данных расширенные параметры защиты от угроз, необходимо включить для нее параметры аудита.</span><span class="sxs-lookup"><span data-stu-id="9b331-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="9b331-108">Чтобы использовать этот cmdlet, укажите параметры *ResourceGroupName,* *ServerName* и *DatabaseName* для идентификации базы данных.</span><span class="sxs-lookup"><span data-stu-id="9b331-108">To use this cmdlet, specify the *ResourceGroupName*, *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="9b331-109">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="9b331-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9b331-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b331-110">EXAMPLES</span></span>

### <span data-ttu-id="9b331-111">Пример 1. Настройка дополнительных параметров защиты от угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="9b331-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="9b331-112">Эта команда задает дополнительные параметры защиты от угроз для базы данных Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="9b331-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="9b331-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b331-113">PARAMETERS</span></span>

### <span data-ttu-id="9b331-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9b331-114">-DatabaseName</span></span>
<span data-ttu-id="9b331-115">Имя базы данных, для которой заданы параметры.</span><span class="sxs-lookup"><span data-stu-id="9b331-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="9b331-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b331-116">-DefaultProfile</span></span>
<span data-ttu-id="9b331-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9b331-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b331-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="9b331-118">-EmailAdmins</span></span>
<span data-ttu-id="9b331-119">Определяет, следует ли расширенные параметры защиты от угроз связываться с администраторами с помощью электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9b331-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="9b331-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="9b331-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="9b331-121">Указывает массив типов обнаружения, которые нужно исключить из параметров.</span><span class="sxs-lookup"><span data-stu-id="9b331-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="9b331-122">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="9b331-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9b331-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="9b331-123">Sql_Injection</span></span> 
- <span data-ttu-id="9b331-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="9b331-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="9b331-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="9b331-125">Access_Anomaly</span></span> 
- <span data-ttu-id="9b331-126">Нет</span><span class="sxs-lookup"><span data-stu-id="9b331-126">None</span></span>

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

### <span data-ttu-id="9b331-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="9b331-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="9b331-128">Определяет список адресов электронной почты, на которые параметры отправляют оповещения, разделив их за semicolon.</span><span class="sxs-lookup"><span data-stu-id="9b331-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="9b331-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b331-129">-PassThru</span></span>
<span data-ttu-id="9b331-130">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9b331-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9b331-131">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9b331-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9b331-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b331-132">-ResourceGroupName</span></span>
<span data-ttu-id="9b331-133">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="9b331-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9b331-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9b331-134">-RetentionInDays</span></span>
<span data-ttu-id="9b331-135">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="9b331-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="9b331-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9b331-136">-ServerName</span></span>
<span data-ttu-id="9b331-137">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="9b331-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="9b331-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9b331-138">-StorageAccountName</span></span>
<span data-ttu-id="9b331-139">Имя используемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9b331-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="9b331-140">Поддиавные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="9b331-140">Wildcards are not permitted.</span></span> <span data-ttu-id="9b331-141">Этот параметр не является нужным.</span><span class="sxs-lookup"><span data-stu-id="9b331-141">This parameter is not required.</span></span> <span data-ttu-id="9b331-142">Если этот параметр не задан, используется учетная запись хранения, которая была определена ранее в параметрах advanced threat protection базы данных.</span><span class="sxs-lookup"><span data-stu-id="9b331-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="9b331-143">Если в базе данных впервые заданы дополнительные параметры защиты от угроз и этот параметр не задан, при этом будет сбой cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b331-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="9b331-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b331-144">-Confirm</span></span>
<span data-ttu-id="9b331-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9b331-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b331-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b331-146">-WhatIf</span></span>
<span data-ttu-id="9b331-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b331-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b331-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9b331-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b331-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b331-149">CommonParameters</span></span>
<span data-ttu-id="9b331-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b331-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b331-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b331-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b331-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b331-152">INPUTS</span></span>

### <span data-ttu-id="9b331-153">System.String</span><span class="sxs-lookup"><span data-stu-id="9b331-153">System.String</span></span>

### <span data-ttu-id="9b331-154">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9b331-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9b331-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="9b331-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="9b331-156">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9b331-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9b331-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b331-157">OUTPUTS</span></span>

### <span data-ttu-id="9b331-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="9b331-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="9b331-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b331-159">NOTES</span></span>

## <span data-ttu-id="9b331-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b331-160">RELATED LINKS</span></span>

[<span data-ttu-id="9b331-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="9b331-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="9b331-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="9b331-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="9b331-163">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="9b331-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


