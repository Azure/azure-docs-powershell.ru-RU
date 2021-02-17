---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 079a1254865821b77ca48a94256dbe1a9e4cb431
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415331"
---
# <span data-ttu-id="34f6c-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="34f6c-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="34f6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="34f6c-103">Задает на сервере дополнительные параметры защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="34f6c-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="34f6c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="34f6c-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34f6c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34f6c-105">DESCRIPTION</span></span>
<span data-ttu-id="34f6c-106">Для **azureSqlServerAdvancedThreatProtectionSetting** задает дополнительные параметры защиты от угроз на сервере Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="34f6c-106">The **Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="34f6c-107">Чтобы включить на сервере расширенные параметры защиты от угроз, на сервере должны быть включены параметры аудита.</span><span class="sxs-lookup"><span data-stu-id="34f6c-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="34f6c-108">Чтобы использовать этот cmdlet, укажите параметры *ResourceGroupName* и ServerName для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="34f6c-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="34f6c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="34f6c-109">EXAMPLES</span></span>

### <span data-ttu-id="34f6c-110">Пример 1. Настройка дополнительных параметров защиты от угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="34f6c-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="34f6c-111">Эта команда задает дополнительные параметры защиты от угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="34f6c-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="34f6c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34f6c-112">PARAMETERS</span></span>

### <span data-ttu-id="34f6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f6c-113">-DefaultProfile</span></span>
<span data-ttu-id="34f6c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="34f6c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34f6c-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="34f6c-115">-EmailAdmins</span></span>
<span data-ttu-id="34f6c-116">Определяет, следует ли расширенные параметры защиты от угроз связываться с администраторами по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="34f6c-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="34f6c-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="34f6c-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="34f6c-118">Указывает массив типов обнаружения, которые нужно исключить из параметров.</span><span class="sxs-lookup"><span data-stu-id="34f6c-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="34f6c-119">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="34f6c-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34f6c-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="34f6c-120">Sql_Injection</span></span>
- <span data-ttu-id="34f6c-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="34f6c-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="34f6c-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="34f6c-122">Access_Anomaly</span></span>
- <span data-ttu-id="34f6c-123">Нет</span><span class="sxs-lookup"><span data-stu-id="34f6c-123">None</span></span>

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

### <span data-ttu-id="34f6c-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="34f6c-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="34f6c-125">Определяет список адресов электронной почты, на которые параметры отправляют оповещения, разделив их за semicolon.</span><span class="sxs-lookup"><span data-stu-id="34f6c-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="34f6c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34f6c-126">-PassThru</span></span>
<span data-ttu-id="34f6c-127">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="34f6c-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="34f6c-128">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="34f6c-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="34f6c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f6c-129">-ResourceGroupName</span></span>
<span data-ttu-id="34f6c-130">Имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="34f6c-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="34f6c-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="34f6c-131">-RetentionInDays</span></span>
<span data-ttu-id="34f6c-132">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="34f6c-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="34f6c-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="34f6c-133">-ServerName</span></span>
<span data-ttu-id="34f6c-134">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="34f6c-134">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34f6c-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="34f6c-135">-StorageAccountName</span></span>
<span data-ttu-id="34f6c-136">Имя используемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="34f6c-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="34f6c-137">Поддиавные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="34f6c-137">Wildcards are not permitted.</span></span> <span data-ttu-id="34f6c-138">Этот параметр не является нужным.</span><span class="sxs-lookup"><span data-stu-id="34f6c-138">This parameter is not required.</span></span> <span data-ttu-id="34f6c-139">Если этот параметр не задан, используется учетная запись хранения, которая была определена ранее в параметрах advanced threat protection базы данных.</span><span class="sxs-lookup"><span data-stu-id="34f6c-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="34f6c-140">Если параметры обнаружения угроз в базе данных заданы впервые и этот параметр не задан, то при этом проектлет не будет работать.</span><span class="sxs-lookup"><span data-stu-id="34f6c-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="34f6c-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34f6c-141">-Confirm</span></span>
<span data-ttu-id="34f6c-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="34f6c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34f6c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f6c-143">-WhatIf</span></span>
<span data-ttu-id="34f6c-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f6c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34f6c-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="34f6c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34f6c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f6c-146">CommonParameters</span></span>
<span data-ttu-id="34f6c-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34f6c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f6c-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34f6c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f6c-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34f6c-149">INPUTS</span></span>

### <span data-ttu-id="34f6c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="34f6c-150">System.String</span></span>

### <span data-ttu-id="34f6c-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="34f6c-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="34f6c-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="34f6c-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="34f6c-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="34f6c-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="34f6c-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="34f6c-154">OUTPUTS</span></span>

### <span data-ttu-id="34f6c-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="34f6c-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="34f6c-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="34f6c-156">NOTES</span></span>

## <span data-ttu-id="34f6c-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34f6c-157">RELATED LINKS</span></span>

[<span data-ttu-id="34f6c-158">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="34f6c-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
