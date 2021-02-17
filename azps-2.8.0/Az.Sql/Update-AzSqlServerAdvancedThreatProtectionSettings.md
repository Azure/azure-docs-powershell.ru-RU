---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 0567454db7421e47faa6690a5c4ad698287ada6a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413325"
---
# <span data-ttu-id="e9137-101">Update-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="e9137-101">Update-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="e9137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9137-102">SYNOPSIS</span></span>
<span data-ttu-id="e9137-103">Задает на сервере дополнительные параметры защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="e9137-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="e9137-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e9137-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSettings [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9137-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9137-105">DESCRIPTION</span></span>
<span data-ttu-id="e9137-106">Для **azureSqlServerAdvancedThreatProtectionSettings** задайте дополнительные параметры защиты от угроз на сервере Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e9137-106">The **Update-AzSqlServerAdvancedThreatProtectionSettings** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="e9137-107">Чтобы включить на сервере расширенные параметры защиты от угроз, на сервере должны быть включены параметры аудита.</span><span class="sxs-lookup"><span data-stu-id="e9137-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="e9137-108">Чтобы использовать этот cmdlet, укажите параметры *ResourceGroupName* и ServerName для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="e9137-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="e9137-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e9137-109">EXAMPLES</span></span>

### <span data-ttu-id="e9137-110">Пример 1. Настройка дополнительных параметров защиты от угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="e9137-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="e9137-111">Эта команда задает дополнительные параметры защиты от угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="e9137-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="e9137-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9137-112">PARAMETERS</span></span>

### <span data-ttu-id="e9137-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9137-113">-DefaultProfile</span></span>
<span data-ttu-id="e9137-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e9137-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9137-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="e9137-115">-EmailAdmins</span></span>
<span data-ttu-id="e9137-116">Определяет, следует ли расширенные параметры защиты от угроз связываться с администраторами по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="e9137-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="e9137-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="e9137-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="e9137-118">Указывает массив типов обнаружения, которые нужно исключить из параметров.</span><span class="sxs-lookup"><span data-stu-id="e9137-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="e9137-119">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="e9137-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e9137-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="e9137-120">Sql_Injection</span></span>
- <span data-ttu-id="e9137-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="e9137-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="e9137-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="e9137-122">Access_Anomaly</span></span>
- <span data-ttu-id="e9137-123">Нет</span><span class="sxs-lookup"><span data-stu-id="e9137-123">None</span></span>

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

### <span data-ttu-id="e9137-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="e9137-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="e9137-125">Определяет список адресов электронной почты, на которые параметры отправляют оповещения, разделив их за semicolon.</span><span class="sxs-lookup"><span data-stu-id="e9137-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="e9137-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9137-126">-PassThru</span></span>
<span data-ttu-id="e9137-127">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e9137-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e9137-128">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e9137-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e9137-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9137-129">-ResourceGroupName</span></span>
<span data-ttu-id="e9137-130">Имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="e9137-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="e9137-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e9137-131">-RetentionInDays</span></span>
<span data-ttu-id="e9137-132">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="e9137-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="e9137-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e9137-133">-ServerName</span></span>
<span data-ttu-id="e9137-134">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="e9137-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e9137-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e9137-135">-StorageAccountName</span></span>
<span data-ttu-id="e9137-136">Имя используемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e9137-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="e9137-137">Поддиавные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="e9137-137">Wildcards are not permitted.</span></span> <span data-ttu-id="e9137-138">Этот параметр не является нужным.</span><span class="sxs-lookup"><span data-stu-id="e9137-138">This parameter is not required.</span></span> <span data-ttu-id="e9137-139">Если этот параметр не задан, используется учетная запись хранения, которая была определена ранее в параметрах advanced threat protection базы данных.</span><span class="sxs-lookup"><span data-stu-id="e9137-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="e9137-140">Если параметры обнаружения угроз в базе данных заданы впервые и этот параметр не задан, то при этом проектлет не будет работать.</span><span class="sxs-lookup"><span data-stu-id="e9137-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="e9137-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9137-141">-Confirm</span></span>
<span data-ttu-id="e9137-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e9137-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9137-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9137-143">-WhatIf</span></span>
<span data-ttu-id="e9137-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9137-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9137-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e9137-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9137-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9137-146">CommonParameters</span></span>
<span data-ttu-id="e9137-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9137-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9137-148">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9137-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9137-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9137-149">INPUTS</span></span>

### <span data-ttu-id="e9137-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e9137-150">System.String</span></span>

### <span data-ttu-id="e9137-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e9137-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e9137-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="e9137-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="e9137-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e9137-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e9137-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9137-154">OUTPUTS</span></span>

### <span data-ttu-id="e9137-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="e9137-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="e9137-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e9137-156">NOTES</span></span>

## <span data-ttu-id="e9137-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9137-157">RELATED LINKS</span></span>

[<span data-ttu-id="e9137-158">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="e9137-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
