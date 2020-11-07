---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 8d58085aa55958e6e0fc9658d814d4bc05006fd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728747"
---
# <span data-ttu-id="e1d2c-101">Set-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e1d2c-101">Set-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="e1d2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d2c-103">Настройка политики обнаружения угроз на сервере.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-103">Sets a threat detection policy on a server.</span></span>

## <span data-ttu-id="e1d2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1d2c-104">SYNTAX</span></span>

```
Set-AzSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1d2c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1d2c-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d2c-106">Командлет **Set-AzSqlServerThreatDetectionPolicy** устанавливает политику обнаружения угроз на сервере Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-106">The **Set-AzSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="e1d2c-107">Чтобы включить обнаружение угроз на сервере, на нем должна быть включена политика аудита.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="e1d2c-108">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и ServerName для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="e1d2c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1d2c-109">EXAMPLES</span></span>

### <span data-ttu-id="e1d2c-110">Пример 1: Настройка политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="e1d2c-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="e1d2c-111">Эта команда задает политику обнаружения угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="e1d2c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1d2c-112">PARAMETERS</span></span>

### <span data-ttu-id="e1d2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d2c-113">-DefaultProfile</span></span>
<span data-ttu-id="e1d2c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e1d2c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1d2c-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="e1d2c-115">-EmailAdmins</span></span>
<span data-ttu-id="e1d2c-116">Определяет, является ли политика обнаружения угроз контактными администраторами с помощью электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="e1d2c-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="e1d2c-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="e1d2c-118">Указывает массив типов обнаружения, исключаемых из политики.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="e1d2c-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e1d2c-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e1d2c-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="e1d2c-120">Sql_Injection</span></span>
- <span data-ttu-id="e1d2c-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="e1d2c-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="e1d2c-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="e1d2c-122">Access_Anomaly</span></span>
- <span data-ttu-id="e1d2c-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="e1d2c-123">None</span></span>

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

### <span data-ttu-id="e1d2c-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="e1d2c-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="e1d2c-125">Указывает список адресов электронной почты, разделенных точкой с запятой, по которым политика отправляет оповещения.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="e1d2c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1d2c-126">-PassThru</span></span>
<span data-ttu-id="e1d2c-127">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1d2c-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1d2c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d2c-129">-ResourceGroupName</span></span>
<span data-ttu-id="e1d2c-130">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="e1d2c-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e1d2c-131">-RetentionInDays</span></span>
<span data-ttu-id="e1d2c-132">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="e1d2c-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="e1d2c-133">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e1d2c-133">-ServerName</span></span>
<span data-ttu-id="e1d2c-134">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e1d2c-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e1d2c-135">-StorageAccountName</span></span>
<span data-ttu-id="e1d2c-136">Указывает имя учетной записи хранения, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="e1d2c-137">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-137">Wildcards are not permitted.</span></span> <span data-ttu-id="e1d2c-138">Этот параметр не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-138">This parameter is not required.</span></span> <span data-ttu-id="e1d2c-139">Если этот параметр не указан, командлет будет использовать учетную запись хранения, которая была ранее определена как часть политики обнаружения угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="e1d2c-140">Если политика обнаружения в базе данных thead не задана, а этот параметр не указан, командлет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="e1d2c-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1d2c-141">-Confirm</span></span>
<span data-ttu-id="e1d2c-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1d2c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1d2c-143">-WhatIf</span></span>
<span data-ttu-id="e1d2c-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1d2c-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1d2c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d2c-146">CommonParameters</span></span>
<span data-ttu-id="e1d2c-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1d2c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d2c-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1d2c-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d2c-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1d2c-149">INPUTS</span></span>

### <span data-ttu-id="e1d2c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e1d2c-150">System.String</span></span>

### <span data-ttu-id="e1d2c-151">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e1d2c-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e1d2c-152">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DetectionType []</span><span class="sxs-lookup"><span data-stu-id="e1d2c-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="e1d2c-153">System. Nullable "1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e1d2c-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e1d2c-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1d2c-154">OUTPUTS</span></span>

### <span data-ttu-id="e1d2c-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e1d2c-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="e1d2c-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1d2c-156">NOTES</span></span>

## <span data-ttu-id="e1d2c-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1d2c-157">RELATED LINKS</span></span>

[<span data-ttu-id="e1d2c-158">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e1d2c-158">Get-AzSqlServerThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="e1d2c-159">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e1d2c-159">Remove-AzSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="e1d2c-160">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="e1d2c-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
