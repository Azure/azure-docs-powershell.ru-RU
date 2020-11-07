---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 3ec370f0e4865ed5695e4f0890f99b50709e9ad8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912449"
---
# <span data-ttu-id="8cab6-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="8cab6-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="8cab6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8cab6-102">SYNOPSIS</span></span>
<span data-ttu-id="8cab6-103">Задает дополнительные параметры защиты от угроз на сервере.</span><span class="sxs-lookup"><span data-stu-id="8cab6-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="8cab6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8cab6-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cab6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cab6-105">DESCRIPTION</span></span>
<span data-ttu-id="8cab6-106">Командлет **Update-AzSqlServerAdvancedThreatProtectionSetting** устанавливает дополнительные параметры защиты от угроз на сервере Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8cab6-106">The **Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="8cab6-107">Для включения расширенной защиты от угроз на сервере параметры аудита должны быть включены на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="8cab6-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="8cab6-108">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и ServerName для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="8cab6-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="8cab6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8cab6-109">EXAMPLES</span></span>

### <span data-ttu-id="8cab6-110">Пример 1: Настройка расширенных параметров защиты от угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="8cab6-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="8cab6-111">Эта команда задает расширенные параметры защиты от угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="8cab6-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="8cab6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8cab6-112">PARAMETERS</span></span>

### <span data-ttu-id="8cab6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cab6-113">-DefaultProfile</span></span>
<span data-ttu-id="8cab6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8cab6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cab6-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="8cab6-115">-EmailAdmins</span></span>
<span data-ttu-id="8cab6-116">Указывает, имеют ли дополнительные параметры защиты от угроз администраторам контакты с помощью электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8cab6-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="8cab6-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="8cab6-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="8cab6-118">Указывает массив типов обнаружения, исключаемых из параметров.</span><span class="sxs-lookup"><span data-stu-id="8cab6-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="8cab6-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8cab6-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8cab6-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="8cab6-120">Sql_Injection</span></span>
- <span data-ttu-id="8cab6-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="8cab6-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="8cab6-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="8cab6-122">Access_Anomaly</span></span>
- <span data-ttu-id="8cab6-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="8cab6-123">None</span></span>

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

### <span data-ttu-id="8cab6-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="8cab6-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="8cab6-125">Указывает список адресов электронной почты, разделенных точкой с запятой, по которым параметры отправляют оповещения.</span><span class="sxs-lookup"><span data-stu-id="8cab6-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="8cab6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cab6-126">-PassThru</span></span>
<span data-ttu-id="8cab6-127">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8cab6-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8cab6-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8cab6-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8cab6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cab6-129">-ResourceGroupName</span></span>
<span data-ttu-id="8cab6-130">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="8cab6-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="8cab6-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8cab6-131">-RetentionInDays</span></span>
<span data-ttu-id="8cab6-132">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="8cab6-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="8cab6-133">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="8cab6-133">-ServerName</span></span>
<span data-ttu-id="8cab6-134">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="8cab6-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="8cab6-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8cab6-135">-StorageAccountName</span></span>
<span data-ttu-id="8cab6-136">Указывает имя учетной записи хранения, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="8cab6-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="8cab6-137">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="8cab6-137">Wildcards are not permitted.</span></span> <span data-ttu-id="8cab6-138">Этот параметр не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8cab6-138">This parameter is not required.</span></span> <span data-ttu-id="8cab6-139">Если этот параметр не указан, командлет будет использовать учетную запись хранения, которая была ранее определена как часть параметров расширенной защиты от угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="8cab6-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="8cab6-140">Если при первом определении параметров обнаружения угроз базы данных этот параметр не указан, командлет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="8cab6-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="8cab6-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cab6-141">-Confirm</span></span>
<span data-ttu-id="8cab6-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8cab6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cab6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cab6-143">-WhatIf</span></span>
<span data-ttu-id="8cab6-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8cab6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cab6-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8cab6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cab6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cab6-146">CommonParameters</span></span>
<span data-ttu-id="8cab6-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8cab6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cab6-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cab6-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cab6-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8cab6-149">INPUTS</span></span>

### <span data-ttu-id="8cab6-150">System. String</span><span class="sxs-lookup"><span data-stu-id="8cab6-150">System.String</span></span>

### <span data-ttu-id="8cab6-151">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8cab6-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8cab6-152">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="8cab6-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="8cab6-153">System. Nullable "1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8cab6-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8cab6-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cab6-154">OUTPUTS</span></span>

### <span data-ttu-id="8cab6-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="8cab6-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="8cab6-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="8cab6-156">NOTES</span></span>

## <span data-ttu-id="8cab6-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8cab6-157">RELATED LINKS</span></span>

[<span data-ttu-id="8cab6-158">Get-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="8cab6-158">Get-AzSqlServerThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="8cab6-159">Remove-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="8cab6-159">Remove-AzSqlServerThreatDetectionsettings</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="8cab6-160">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="8cab6-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
