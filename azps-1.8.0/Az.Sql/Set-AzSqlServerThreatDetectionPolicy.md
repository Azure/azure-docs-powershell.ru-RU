---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 49b484c17b595a8f676a089f8627b70a1f34c471
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399504"
---
# <span data-ttu-id="76f4e-101">Set-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="76f4e-101">Set-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="76f4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="76f4e-103">Задает политику обнаружения угроз на сервере.</span><span class="sxs-lookup"><span data-stu-id="76f4e-103">Sets a threat detection policy on a server.</span></span>

## <span data-ttu-id="76f4e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76f4e-104">SYNTAX</span></span>

```
Set-AzSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76f4e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76f4e-105">DESCRIPTION</span></span>
<span data-ttu-id="76f4e-106">Cmdlet **Set-AzSqlServerThreatDetectionPolicy** задает политику обнаружения угроз на сервере Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="76f4e-106">The **Set-AzSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="76f4e-107">Чтобы включить обнаружение угроз на сервере, на этом сервере должна быть включена политика аудита.</span><span class="sxs-lookup"><span data-stu-id="76f4e-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="76f4e-108">Чтобы использовать этот cmdlet, укажите параметры *ResourceGroupName* и ServerName для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="76f4e-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="76f4e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76f4e-109">EXAMPLES</span></span>

### <span data-ttu-id="76f4e-110">Пример 1. Настройка политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="76f4e-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="76f4e-111">Эта команда задает политику обнаружения угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="76f4e-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="76f4e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76f4e-112">PARAMETERS</span></span>

### <span data-ttu-id="76f4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f4e-113">-DefaultProfile</span></span>
<span data-ttu-id="76f4e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="76f4e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76f4e-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="76f4e-115">-EmailAdmins</span></span>
<span data-ttu-id="76f4e-116">Указывает, будет ли политика обнаружения угроз связываться с администраторами по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="76f4e-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="76f4e-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="76f4e-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="76f4e-118">Указывает массив типов обнаружения, которые нужно исключить из политики.</span><span class="sxs-lookup"><span data-stu-id="76f4e-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="76f4e-119">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="76f4e-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76f4e-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="76f4e-120">Sql_Injection</span></span>
- <span data-ttu-id="76f4e-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="76f4e-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="76f4e-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="76f4e-122">Access_Anomaly</span></span>
- <span data-ttu-id="76f4e-123">Нет</span><span class="sxs-lookup"><span data-stu-id="76f4e-123">None</span></span>

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

### <span data-ttu-id="76f4e-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="76f4e-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="76f4e-125">Определяет список адресов электронной почты, на которые политика отправляет оповещения, разделив их за semicolon.</span><span class="sxs-lookup"><span data-stu-id="76f4e-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="76f4e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76f4e-126">-PassThru</span></span>
<span data-ttu-id="76f4e-127">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="76f4e-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="76f4e-128">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="76f4e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="76f4e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f4e-129">-ResourceGroupName</span></span>
<span data-ttu-id="76f4e-130">Имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="76f4e-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="76f4e-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="76f4e-131">-RetentionInDays</span></span>
<span data-ttu-id="76f4e-132">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="76f4e-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="76f4e-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="76f4e-133">-ServerName</span></span>
<span data-ttu-id="76f4e-134">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="76f4e-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="76f4e-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="76f4e-135">-StorageAccountName</span></span>
<span data-ttu-id="76f4e-136">Имя используемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="76f4e-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="76f4e-137">Поддиавные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="76f4e-137">Wildcards are not permitted.</span></span> <span data-ttu-id="76f4e-138">Этот параметр не является нужным.</span><span class="sxs-lookup"><span data-stu-id="76f4e-138">This parameter is not required.</span></span> <span data-ttu-id="76f4e-139">Если этот параметр не задан, используется учетная запись хранения, которая была определена ранее в политике обнаружения угроз базы данных.</span><span class="sxs-lookup"><span data-stu-id="76f4e-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="76f4e-140">Если база данных определена впервые и этот параметр не задан, при этом будет сбой cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f4e-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="76f4e-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76f4e-141">-Confirm</span></span>
<span data-ttu-id="76f4e-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="76f4e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76f4e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76f4e-143">-WhatIf</span></span>
<span data-ttu-id="76f4e-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f4e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76f4e-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="76f4e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76f4e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f4e-146">CommonParameters</span></span>
<span data-ttu-id="76f4e-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f4e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f4e-148">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76f4e-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f4e-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76f4e-149">INPUTS</span></span>

### <span data-ttu-id="76f4e-150">System.String</span><span class="sxs-lookup"><span data-stu-id="76f4e-150">System.String</span></span>

### <span data-ttu-id="76f4e-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="76f4e-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="76f4e-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="76f4e-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="76f4e-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="76f4e-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="76f4e-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76f4e-154">OUTPUTS</span></span>

### <span data-ttu-id="76f4e-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="76f4e-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="76f4e-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76f4e-156">NOTES</span></span>

## <span data-ttu-id="76f4e-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76f4e-157">RELATED LINKS</span></span>

[<span data-ttu-id="76f4e-158">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="76f4e-158">Get-AzSqlServerThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="76f4e-159">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="76f4e-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
