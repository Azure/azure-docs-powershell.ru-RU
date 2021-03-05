---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 1b045b97df1dbbc704f3288cf2075caa16f30bd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014723"
---
# <span data-ttu-id="c8ea8-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c8ea8-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="c8ea8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ea8-103">Возвращает состояние TDE для базы данных.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="c8ea8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8ea8-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8ea8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8ea8-105">DESCRIPTION</span></span>
<span data-ttu-id="c8ea8-106">Для базы данных Azure SQL состояние шифрования данных (TDE) используется для cmdlet **Get-AzSqlDataBaseTransparentDataEncryption.**</span><span class="sxs-lookup"><span data-stu-id="c8ea8-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="c8ea8-107">Дополнительные сведения см. в теме "Прозрачное шифрование данных с помощью SQL Azure "База данных" https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (Microsoft Developer Network библиотеки).</span><span class="sxs-lookup"><span data-stu-id="c8ea8-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="c8ea8-108">Этот cmdlet получает текущее состояние TDE, но шифрование и расшифровка могут быть длительными.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="c8ea8-109">Чтобы увидеть ход проверки шифрования, запустите Get-AzSqlDatabaseTransparentDataEncryptionActivity выполнения.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="c8ea8-110">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c8ea8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8ea8-111">EXAMPLES</span></span>

### <span data-ttu-id="c8ea8-112">Пример 1. Получить состояние TDE для базы данных</span><span class="sxs-lookup"><span data-stu-id="c8ea8-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="c8ea8-113">Эта команда получает состояние TDE для базы данных Database01 на сервере с именем server01.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="c8ea8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8ea8-114">PARAMETERS</span></span>

### <span data-ttu-id="c8ea8-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8ea8-115">-DatabaseName</span></span>
<span data-ttu-id="c8ea8-116">Имя базы данных, для которой этот cmdlet получает состояние TDE.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="c8ea8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8ea8-117">-DefaultProfile</span></span>
<span data-ttu-id="c8ea8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c8ea8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8ea8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8ea8-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8ea8-120">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c8ea8-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c8ea8-121">-ServerName</span></span>
<span data-ttu-id="c8ea8-122">Имя сервера, на котором размещена база данных, для которой этот cmdlet получает состояние TDE.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="c8ea8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8ea8-123">-Confirm</span></span>
<span data-ttu-id="c8ea8-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8ea8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8ea8-125">-WhatIf</span></span>
<span data-ttu-id="c8ea8-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8ea8-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8ea8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ea8-128">CommonParameters</span></span>
<span data-ttu-id="c8ea8-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ea8-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8ea8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ea8-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8ea8-131">INPUTS</span></span>

### <span data-ttu-id="c8ea8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c8ea8-132">System.String</span></span>

## <span data-ttu-id="c8ea8-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8ea8-133">OUTPUTS</span></span>

### <span data-ttu-id="c8ea8-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="c8ea8-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="c8ea8-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8ea8-135">NOTES</span></span>

## <span data-ttu-id="c8ea8-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8ea8-136">RELATED LINKS</span></span>

[<span data-ttu-id="c8ea8-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="c8ea8-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="c8ea8-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="c8ea8-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
