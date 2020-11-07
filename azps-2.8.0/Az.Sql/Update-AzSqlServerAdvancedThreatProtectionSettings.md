---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 16fa9df22141b62f8a5b7ff3b6cad3ca05b1d406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906877"
---
# <span data-ttu-id="331e7-101">Update-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="331e7-101">Update-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="331e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="331e7-102">SYNOPSIS</span></span>
<span data-ttu-id="331e7-103">Задает дополнительные параметры защиты от угроз на сервере.</span><span class="sxs-lookup"><span data-stu-id="331e7-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="331e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="331e7-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSettings [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="331e7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="331e7-105">DESCRIPTION</span></span>
<span data-ttu-id="331e7-106">Командлет **Update-AzSqlServerAdvancedThreatProtectionSettings** устанавливает дополнительные параметры защиты от угроз на сервере Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="331e7-106">The **Update-AzSqlServerAdvancedThreatProtectionSettings** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="331e7-107">Для включения расширенной защиты от угроз на сервере параметры аудита должны быть включены на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="331e7-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="331e7-108">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и ServerName для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="331e7-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="331e7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="331e7-109">EXAMPLES</span></span>

### <span data-ttu-id="331e7-110">Пример 1: Настройка расширенных параметров защиты от угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="331e7-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="331e7-111">Эта команда задает расширенные параметры защиты от угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="331e7-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="331e7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="331e7-112">PARAMETERS</span></span>

### <span data-ttu-id="331e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="331e7-113">-DefaultProfile</span></span>
<span data-ttu-id="331e7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="331e7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="331e7-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="331e7-115">-EmailAdmins</span></span>
<span data-ttu-id="331e7-116">Указывает, имеют ли дополнительные параметры защиты от угроз администраторам контакты с помощью электронной почты.</span><span class="sxs-lookup"><span data-stu-id="331e7-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="331e7-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="331e7-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="331e7-118">Указывает массив типов обнаружения, исключаемых из параметров.</span><span class="sxs-lookup"><span data-stu-id="331e7-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="331e7-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="331e7-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="331e7-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="331e7-120">Sql_Injection</span></span>
- <span data-ttu-id="331e7-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="331e7-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="331e7-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="331e7-122">Access_Anomaly</span></span>
- <span data-ttu-id="331e7-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="331e7-123">None</span></span>

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

### <span data-ttu-id="331e7-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="331e7-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="331e7-125">Указывает список адресов электронной почты, разделенных точкой с запятой, по которым параметры отправляют оповещения.</span><span class="sxs-lookup"><span data-stu-id="331e7-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="331e7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="331e7-126">-PassThru</span></span>
<span data-ttu-id="331e7-127">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="331e7-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="331e7-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="331e7-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="331e7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="331e7-129">-ResourceGroupName</span></span>
<span data-ttu-id="331e7-130">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="331e7-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="331e7-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="331e7-131">-RetentionInDays</span></span>
<span data-ttu-id="331e7-132">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="331e7-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="331e7-133">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="331e7-133">-ServerName</span></span>
<span data-ttu-id="331e7-134">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="331e7-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="331e7-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="331e7-135">-StorageAccountName</span></span>
<span data-ttu-id="331e7-136">Указывает имя учетной записи хранения, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="331e7-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="331e7-137">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="331e7-137">Wildcards are not permitted.</span></span> <span data-ttu-id="331e7-138">Этот параметр не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="331e7-138">This parameter is not required.</span></span> <span data-ttu-id="331e7-139">Если этот параметр не указан, командлет будет использовать учетную запись хранения, которая была ранее определена как часть параметров расширенной защиты от угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="331e7-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="331e7-140">Если при первом определении параметров обнаружения угроз базы данных этот параметр не указан, командлет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="331e7-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="331e7-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="331e7-141">-Confirm</span></span>
<span data-ttu-id="331e7-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="331e7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="331e7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="331e7-143">-WhatIf</span></span>
<span data-ttu-id="331e7-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="331e7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="331e7-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="331e7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="331e7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="331e7-146">CommonParameters</span></span>
<span data-ttu-id="331e7-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="331e7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="331e7-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="331e7-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="331e7-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="331e7-149">INPUTS</span></span>

### <span data-ttu-id="331e7-150">System. String</span><span class="sxs-lookup"><span data-stu-id="331e7-150">System.String</span></span>

### <span data-ttu-id="331e7-151">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="331e7-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="331e7-152">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="331e7-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="331e7-153">System. Nullable "1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="331e7-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="331e7-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="331e7-154">OUTPUTS</span></span>

### <span data-ttu-id="331e7-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="331e7-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="331e7-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="331e7-156">NOTES</span></span>

## <span data-ttu-id="331e7-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="331e7-157">RELATED LINKS</span></span>

[<span data-ttu-id="331e7-158">Get-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="331e7-158">Get-AzSqlServerThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="331e7-159">Remove-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="331e7-159">Remove-AzSqlServerThreatDetectionsettings</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="331e7-160">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="331e7-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
