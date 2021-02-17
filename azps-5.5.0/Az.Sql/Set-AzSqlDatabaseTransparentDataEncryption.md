---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: f2e9cc38faab0af87eb20b3a60d61ab679c435d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212420"
---
# <span data-ttu-id="33a3f-101">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="33a3f-101">Set-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="33a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="33a3f-103">Изменяет свойство TDE для базы данных.</span><span class="sxs-lookup"><span data-stu-id="33a3f-103">Modifies TDE property for a database.</span></span>

## <span data-ttu-id="33a3f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="33a3f-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33a3f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33a3f-105">DESCRIPTION</span></span>
<span data-ttu-id="33a3f-106">Для свойства Transparent Data Encryption (TDE) базы данных Azure SQL используется свойство **Set-AzSqlDataTransparentDataEncryption.**</span><span class="sxs-lookup"><span data-stu-id="33a3f-106">The **Set-AzSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="33a3f-107">Дополнительные сведения см. в теме "Прозрачное шифрование данных с помощью SQL Azure "База данных" https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (Microsoft Developer Network библиотеки).</span><span class="sxs-lookup"><span data-stu-id="33a3f-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="33a3f-108">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="33a3f-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="33a3f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="33a3f-109">EXAMPLES</span></span>

### <span data-ttu-id="33a3f-110">Пример 1. Включить TDE для базы данных</span><span class="sxs-lookup"><span data-stu-id="33a3f-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="33a3f-111">Эта команда включает TDE для базы данных Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="33a3f-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="33a3f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33a3f-112">PARAMETERS</span></span>

### <span data-ttu-id="33a3f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="33a3f-113">-DatabaseName</span></span>
<span data-ttu-id="33a3f-114">Имя базы данных, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33a3f-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="33a3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a3f-115">-DefaultProfile</span></span>
<span data-ttu-id="33a3f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="33a3f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33a3f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33a3f-117">-ResourceGroupName</span></span>
<span data-ttu-id="33a3f-118">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="33a3f-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="33a3f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="33a3f-119">-ServerName</span></span>
<span data-ttu-id="33a3f-120">Имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="33a3f-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="33a3f-121">-State</span><span class="sxs-lookup"><span data-stu-id="33a3f-121">-State</span></span>
<span data-ttu-id="33a3f-122">Определяет значение свойства TDE.</span><span class="sxs-lookup"><span data-stu-id="33a3f-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="33a3f-123">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="33a3f-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="33a3f-124">Включено</span><span class="sxs-lookup"><span data-stu-id="33a3f-124">Enabled</span></span> 
- <span data-ttu-id="33a3f-125">Отключено</span><span class="sxs-lookup"><span data-stu-id="33a3f-125">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33a3f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33a3f-126">-Confirm</span></span>
<span data-ttu-id="33a3f-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="33a3f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33a3f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33a3f-128">-WhatIf</span></span>
<span data-ttu-id="33a3f-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33a3f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33a3f-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="33a3f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33a3f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a3f-131">CommonParameters</span></span>
<span data-ttu-id="33a3f-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a3f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a3f-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33a3f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a3f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33a3f-134">INPUTS</span></span>

### <span data-ttu-id="33a3f-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span><span class="sxs-lookup"><span data-stu-id="33a3f-135">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.TransparentDataEncryptionStateType</span></span>

### <span data-ttu-id="33a3f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="33a3f-136">System.String</span></span>

## <span data-ttu-id="33a3f-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="33a3f-137">OUTPUTS</span></span>

### <span data-ttu-id="33a3f-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="33a3f-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="33a3f-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="33a3f-139">NOTES</span></span>

## <span data-ttu-id="33a3f-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33a3f-140">RELATED LINKS</span></span>

[<span data-ttu-id="33a3f-141">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="33a3f-141">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="33a3f-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="33a3f-142">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="33a3f-143">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="33a3f-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


