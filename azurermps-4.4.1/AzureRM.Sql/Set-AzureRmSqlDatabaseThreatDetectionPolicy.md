---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 746a9a9908865047d5b904b5b47b71ca9c30fbd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562012"
---
# <span data-ttu-id="f66c5-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f66c5-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="f66c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f66c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f66c5-103">Задает политику обнаружения угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="f66c5-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f66c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f66c5-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f66c5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f66c5-105">DESCRIPTION</span></span>
<span data-ttu-id="f66c5-106">Командлет **Set-AzureRmSqlDatabaseThreatDetectionPolicy** устанавливает политику обнаружения угроз в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f66c5-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="f66c5-107">Чтобы включить обнаружение угроз для базы данных, необходимо включить в этой базе данных политику аудита.</span><span class="sxs-lookup"><span data-stu-id="f66c5-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>

<span data-ttu-id="f66c5-108">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* , *ServerName* и *DatabaseName* , чтобы идентифицировать базу данных.</span><span class="sxs-lookup"><span data-stu-id="f66c5-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="f66c5-109">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="f66c5-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f66c5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f66c5-110">EXAMPLES</span></span>

### <span data-ttu-id="f66c5-111">Пример 1: Настройка политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="f66c5-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="f66c5-112">Эта команда задает политику обнаружения угроз для базы данных с именем Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="f66c5-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="f66c5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f66c5-113">PARAMETERS</span></span>

### <span data-ttu-id="f66c5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f66c5-114">-DatabaseName</span></span>
<span data-ttu-id="f66c5-115">Указывает имя базы данных, в которой задана политика.</span><span class="sxs-lookup"><span data-stu-id="f66c5-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="f66c5-116">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="f66c5-116">-EmailAdmins</span></span>
<span data-ttu-id="f66c5-117">Определяет, является ли политика обнаружения угроз контактными администраторами с помощью электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f66c5-117">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="f66c5-118">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="f66c5-118">-ExcludedDetectionType</span></span>
<span data-ttu-id="f66c5-119">Указывает массив типов обнаружения, исключаемых из политики.</span><span class="sxs-lookup"><span data-stu-id="f66c5-119">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="f66c5-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f66c5-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f66c5-121">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="f66c5-121">Sql_Injection</span></span> 
- <span data-ttu-id="f66c5-122">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="f66c5-122">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="f66c5-123">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="f66c5-123">Access_Anomaly</span></span> 
- <span data-ttu-id="f66c5-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="f66c5-124">None</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f66c5-125">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="f66c5-125">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="f66c5-126">Указывает список адресов электронной почты, разделенных точкой с запятой, по которым политика отправляет оповещения.</span><span class="sxs-lookup"><span data-stu-id="f66c5-126">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="f66c5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f66c5-127">-PassThru</span></span>
<span data-ttu-id="f66c5-128">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f66c5-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f66c5-129">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f66c5-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f66c5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f66c5-130">-ResourceGroupName</span></span>
<span data-ttu-id="f66c5-131">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="f66c5-131">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f66c5-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f66c5-132">-RetentionInDays</span></span>
<span data-ttu-id="f66c5-133">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="f66c5-133">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="f66c5-134">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f66c5-134">-ServerName</span></span>
<span data-ttu-id="f66c5-135">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f66c5-135">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="f66c5-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f66c5-136">-StorageAccountName</span></span>
<span data-ttu-id="f66c5-137">Указывает имя учетной записи хранения, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="f66c5-137">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="f66c5-138">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="f66c5-138">Wildcards are not permitted.</span></span> <span data-ttu-id="f66c5-139">Этот параметр не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f66c5-139">This parameter is not required.</span></span> <span data-ttu-id="f66c5-140">Если этот параметр не указан, командлет будет использовать учетную запись хранения, которая была ранее определена как часть политики обнаружения угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="f66c5-140">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="f66c5-141">Если определена политика обнаружения угроз базы данных в первый раз и этот параметр не указан, командлет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="f66c5-141">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="f66c5-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f66c5-142">-Confirm</span></span>
<span data-ttu-id="f66c5-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f66c5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f66c5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f66c5-144">-WhatIf</span></span>
<span data-ttu-id="f66c5-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f66c5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f66c5-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f66c5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f66c5-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f66c5-147">-DefaultProfile</span></span>
<span data-ttu-id="f66c5-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f66c5-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f66c5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f66c5-149">CommonParameters</span></span>
<span data-ttu-id="f66c5-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f66c5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f66c5-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f66c5-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f66c5-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f66c5-152">INPUTS</span></span>

###  
<span data-ttu-id="f66c5-153">Вы не можете передавать входные данные в этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f66c5-153">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="f66c5-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f66c5-154">OUTPUTS</span></span>

### <span data-ttu-id="f66c5-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f66c5-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="f66c5-156">Этот командлет возвращает объект **model. DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="f66c5-156">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="f66c5-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="f66c5-157">NOTES</span></span>

## <span data-ttu-id="f66c5-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f66c5-158">RELATED LINKS</span></span>

[<span data-ttu-id="f66c5-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f66c5-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="f66c5-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f66c5-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="f66c5-161">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f66c5-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


