---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 632b7710a6055f40c6cdc6d87d4b2cf8e3e17eeb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077570"
---
# <span data-ttu-id="987e4-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="987e4-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="987e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="987e4-102">SYNOPSIS</span></span>
<span data-ttu-id="987e4-103">Возвращает состояние TDE для базы данных.</span><span class="sxs-lookup"><span data-stu-id="987e4-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="987e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="987e4-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="987e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="987e4-105">DESCRIPTION</span></span>
<span data-ttu-id="987e4-106">Командлет **Get-AzSqlDatabaseTransparentDataEncryption** получает состояние прозрачного шифрования данных (TDE) для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="987e4-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="987e4-107">Дополнительные сведения можно найти в разделе прозрачное шифрование данных с базой данных Azure SQL https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) в сетевой библиотеке разработчиков Microsoft).</span><span class="sxs-lookup"><span data-stu-id="987e4-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="987e4-108">Этот командлет получает текущее состояние TDE, но как шифрование, так и расшифровка могут быть долго выполняющимися операциями.</span><span class="sxs-lookup"><span data-stu-id="987e4-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="987e4-109">Чтобы просмотреть процесс проверки шифрования, запустите командлет Get-AzSqlDatabaseTransparentDataEncryptionActivity.</span><span class="sxs-lookup"><span data-stu-id="987e4-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="987e4-110">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="987e4-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="987e4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="987e4-111">EXAMPLES</span></span>

### <span data-ttu-id="987e4-112">Пример 1: получение состояния TDE для базы данных</span><span class="sxs-lookup"><span data-stu-id="987e4-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="987e4-113">Эта команда получает состояние TDE для базы данных с именем Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="987e4-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="987e4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="987e4-114">PARAMETERS</span></span>

### <span data-ttu-id="987e4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="987e4-115">-DatabaseName</span></span>
<span data-ttu-id="987e4-116">Указывает имя базы данных, для которой этот командлет получает состояние TDE.</span><span class="sxs-lookup"><span data-stu-id="987e4-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="987e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987e4-117">-DefaultProfile</span></span>
<span data-ttu-id="987e4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="987e4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="987e4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="987e4-119">-ResourceGroupName</span></span>
<span data-ttu-id="987e4-120">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="987e4-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="987e4-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="987e4-121">-ServerName</span></span>
<span data-ttu-id="987e4-122">Указывает имя сервера, на котором размещается база данных, для которой этот командлет получает состояние TDE.</span><span class="sxs-lookup"><span data-stu-id="987e4-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="987e4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="987e4-123">-Confirm</span></span>
<span data-ttu-id="987e4-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="987e4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="987e4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="987e4-125">-WhatIf</span></span>
<span data-ttu-id="987e4-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="987e4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="987e4-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="987e4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="987e4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987e4-128">CommonParameters</span></span>
<span data-ttu-id="987e4-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="987e4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987e4-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="987e4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987e4-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="987e4-131">INPUTS</span></span>

### <span data-ttu-id="987e4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="987e4-132">System.String</span></span>

## <span data-ttu-id="987e4-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="987e4-133">OUTPUTS</span></span>

### <span data-ttu-id="987e4-134">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="987e4-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="987e4-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="987e4-135">NOTES</span></span>

## <span data-ttu-id="987e4-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="987e4-136">RELATED LINKS</span></span>

[<span data-ttu-id="987e4-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="987e4-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="987e4-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="987e4-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
