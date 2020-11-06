---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 7c71e9390ca28b48127a2f977e04eba645ae962f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570031"
---
# <span data-ttu-id="cea95-101">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cea95-101">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="cea95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cea95-102">SYNOPSIS</span></span>
<span data-ttu-id="cea95-103">Настройка политики обнаружения угроз на сервере.</span><span class="sxs-lookup"><span data-stu-id="cea95-103">Sets a threat detection policy on a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cea95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cea95-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cea95-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cea95-105">DESCRIPTION</span></span>
<span data-ttu-id="cea95-106">Командлет **Set-AzureRmSqlServerThreatDetectionPolicy** устанавливает политику обнаружения угроз на сервере Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cea95-106">The **Set-AzureRmSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="cea95-107">Чтобы включить обнаружение угроз на сервере, на нем должна быть включена политика аудита.</span><span class="sxs-lookup"><span data-stu-id="cea95-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="cea95-108">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и ServerName для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="cea95-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="cea95-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cea95-109">EXAMPLES</span></span>

### <span data-ttu-id="cea95-110">Пример 1: Настройка политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="cea95-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="cea95-111">Эта команда задает политику обнаружения угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="cea95-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="cea95-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cea95-112">PARAMETERS</span></span>

### <span data-ttu-id="cea95-113">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="cea95-113">-EmailAdmins</span></span>
<span data-ttu-id="cea95-114">Определяет, является ли политика обнаружения угроз контактными администраторами с помощью электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cea95-114">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="cea95-115">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="cea95-115">-ExcludedDetectionType</span></span>
<span data-ttu-id="cea95-116">Указывает массив типов обнаружения, исключаемых из политики.</span><span class="sxs-lookup"><span data-stu-id="cea95-116">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="cea95-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cea95-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cea95-118">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="cea95-118">Sql_Injection</span></span>
- <span data-ttu-id="cea95-119">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="cea95-119">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="cea95-120">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="cea95-120">Access_Anomaly</span></span>
- <span data-ttu-id="cea95-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="cea95-121">None</span></span>

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

### <span data-ttu-id="cea95-122">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="cea95-122">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="cea95-123">Указывает список адресов электронной почты, разделенных точкой с запятой, по которым политика отправляет оповещения.</span><span class="sxs-lookup"><span data-stu-id="cea95-123">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="cea95-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cea95-124">-PassThru</span></span>
<span data-ttu-id="cea95-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="cea95-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cea95-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cea95-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cea95-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cea95-127">-ResourceGroupName</span></span>
<span data-ttu-id="cea95-128">Указывает имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="cea95-128">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="cea95-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="cea95-129">-RetentionInDays</span></span>
<span data-ttu-id="cea95-130">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="cea95-130">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="cea95-131">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="cea95-131">-ServerName</span></span>
<span data-ttu-id="cea95-132">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="cea95-132">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="cea95-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cea95-133">-StorageAccountName</span></span>
<span data-ttu-id="cea95-134">Указывает имя учетной записи хранения, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="cea95-134">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="cea95-135">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="cea95-135">Wildcards are not permitted.</span></span> <span data-ttu-id="cea95-136">Этот параметр не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="cea95-136">This parameter is not required.</span></span> <span data-ttu-id="cea95-137">Если этот параметр не указан, командлет будет использовать учетную запись хранения, которая была ранее определена как часть политики обнаружения угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="cea95-137">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="cea95-138">Если политика обнаружения в базе данных thead не задана, а этот параметр не указан, командлет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="cea95-138">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="cea95-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cea95-139">-Confirm</span></span>
<span data-ttu-id="cea95-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cea95-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cea95-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cea95-141">-WhatIf</span></span>
<span data-ttu-id="cea95-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cea95-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cea95-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cea95-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cea95-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea95-144">-DefaultProfile</span></span>
<span data-ttu-id="cea95-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cea95-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cea95-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea95-146">CommonParameters</span></span>
<span data-ttu-id="cea95-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cea95-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea95-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cea95-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea95-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cea95-149">INPUTS</span></span>

###  
<span data-ttu-id="cea95-150">Вы не можете передавать входные данные в этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cea95-150">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="cea95-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cea95-151">OUTPUTS</span></span>

### <span data-ttu-id="cea95-152">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="cea95-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="cea95-153">Этот командлет возвращает объект **ServerThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="cea95-153">This cmdlet returns a **ServerThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="cea95-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="cea95-154">NOTES</span></span>

## <span data-ttu-id="cea95-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cea95-155">RELATED LINKS</span></span>

[<span data-ttu-id="cea95-156">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cea95-156">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="cea95-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cea95-157">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="cea95-158">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="cea95-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
