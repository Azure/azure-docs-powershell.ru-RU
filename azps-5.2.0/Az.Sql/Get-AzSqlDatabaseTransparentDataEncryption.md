---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 632b7710a6055f40c6cdc6d87d4b2cf8e3e17eeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417620"
---
# <span data-ttu-id="1d6ed-101">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="1d6ed-101">Get-AzSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="1d6ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="1d6ed-103">Возвращает состояние TDE для базы данных.</span><span class="sxs-lookup"><span data-stu-id="1d6ed-103">Gets the TDE state for a database.</span></span>

## <span data-ttu-id="1d6ed-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1d6ed-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d6ed-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d6ed-105">DESCRIPTION</span></span>
<span data-ttu-id="1d6ed-106">Для базы данных Azure SQL состояние шифрования данных (TDE) используется для cmdlet **Get-AzSqlDataBaseTransparentDataEncryption.**</span><span class="sxs-lookup"><span data-stu-id="1d6ed-106">The **Get-AzSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="1d6ed-107">Дополнительные сведения см. в теме "Прозрачное шифрование данных с помощью SQL Azure "База данных" https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (Microsoft Developer Network библиотеки).</span><span class="sxs-lookup"><span data-stu-id="1d6ed-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="1d6ed-108">Этот cmdlet получает текущее состояние TDE, но шифрование и расшифровка могут быть длительными.</span><span class="sxs-lookup"><span data-stu-id="1d6ed-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="1d6ed-109">Чтобы увидеть ход проверки шифрования, запустите Get-AzSqlDatabaseTransparentDataEncryptionActivity выполнения.</span><span class="sxs-lookup"><span data-stu-id="1d6ed-109">To see the encryption scan progress, run the Get-AzSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>
<span data-ttu-id="1d6ed-110">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="1d6ed-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1d6ed-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1d6ed-111">EXAMPLES</span></span>

### <span data-ttu-id="1d6ed-112">Пример 1. Получить состояние TDE для базы данных</span><span class="sxs-lookup"><span data-stu-id="1d6ed-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="1d6ed-113">Эта команда получает состояние TDE для базы данных Database01 на сервере с именем server01.</span><span class="sxs-lookup"><span data-stu-id="1d6ed-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="1d6ed-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d6ed-114">PARAMETERS</span></span>

### <span data-ttu-id="1d6ed-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d6ed-115">-DatabaseName</span></span>
<span data-ttu-id="1d6ed-116">Имя базы данных, для которой этот cmdlet получает состояние TDE.</span><span class="sxs-lookup"><span data-stu-id="1d6ed-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="1d6ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d6ed-117">-DefaultProfile</span></span>
<span data-ttu-id="1d6ed-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1d6ed-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d6ed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d6ed-119">-ResourceGroupName</span></span>
<span data-ttu-id="1d6ed-120">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="1d6ed-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1d6ed-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1d6ed-121">-ServerName</span></span>
<span data-ttu-id="1d6ed-122">Имя сервера, на котором размещена база данных, для которой этот cmdlet получает состояние TDE.</span><span class="sxs-lookup"><span data-stu-id="1d6ed-122">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="1d6ed-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d6ed-123">-Confirm</span></span>
<span data-ttu-id="1d6ed-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d6ed-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d6ed-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d6ed-125">-WhatIf</span></span>
<span data-ttu-id="1d6ed-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d6ed-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d6ed-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1d6ed-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d6ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d6ed-128">CommonParameters</span></span>
<span data-ttu-id="1d6ed-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d6ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d6ed-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d6ed-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d6ed-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d6ed-131">INPUTS</span></span>

### <span data-ttu-id="1d6ed-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1d6ed-132">System.String</span></span>

## <span data-ttu-id="1d6ed-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d6ed-133">OUTPUTS</span></span>

### <span data-ttu-id="1d6ed-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="1d6ed-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="1d6ed-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1d6ed-135">NOTES</span></span>

## <span data-ttu-id="1d6ed-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d6ed-136">RELATED LINKS</span></span>

[<span data-ttu-id="1d6ed-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="1d6ed-137">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="1d6ed-138">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="1d6ed-138">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)
